---
layout: post
title: Try CUDA on Ubuntu(WSL2)
tags: posts
category: posts
last_updated: 2025-01-01
---

最近想尝试一下用**whisper.cpp**来给一些Youtube上的视频/音频转Transcript，做一些笔记。

这里记录一下探索过程

# Ubuntu on WSL2

之前一直在WSL2上用Debian，但是感觉确实里面的软件老了一些，而且CUDA官方提供的包是Ubuntu-WSL2的，所以安装一个

安装直接

```bash
wsl --install -d Ubuntu
```

不过我这里出现卡顿了，所以后面关了窗口直接进入

```bash
wsl -d Ubuntu
```

默认登陆进入root，设置新用户

```bash
adduser twando
```

然后加入sudo

```bash
usermod -aG sudo twando
```

然后设置一下默认登录的账户，修改```/etc/wsl.conf```

```ini
[user]
default=username
```

# Install CUDA

参考[CUDA on WSL User Guide](https://docs.nvidia.com/cuda/wsl-user-guide/index.html)

对于在WSL2使用CUDA，其实主要的driver都在windows-side

在Linux-side中，只需要装一个toolkit，类似于一个token，告诉系统有就可以了。

直接使用包安装最方便

```
wget https://developer.download.nvidia.com/compute/cuda/repos/wsl-ubuntu/x86_64/cuda-wsl-ubuntu.pin
sudo mv cuda-wsl-ubuntu.pin /etc/apt/preferences.d/cuda-repository-pin-600
wget https://developer.download.nvidia.com/compute/cuda/12.6.3/local_installers/cuda-repo-wsl-ubuntu-12-6-local_12.6.3-1_amd64.deb
sudo dpkg -i cuda-repo-wsl-ubuntu-12-6-local_12.6.3-1_amd64.deb
sudo cp /var/cuda-repo-wsl-ubuntu-12-6-local/cuda-*-keyring.gpg /usr/share/keyrings/
sudo apt-get update
sudo apt-get -y install cuda-toolkit-12-6
```

安装完之后加入到PATH（在```.bashrc```中添加）

```bash
export PATH=/usr/local/cuda-12.6/bin${PATH:+:${PATH}}
```

# Test CUDA

先clone一下

```bash
git clone https://github.com/NVIDIA/cuda-samples.git
```

直接

```bash
cd <sample_dir>
make
```

> 好像不太行。。。WSL2的版本不够。。。

# 在Mac上测试whisper.cpp

先吧文件格式处理一下（只接受16kHZ的wav文件）

```bash
ffmpeg -i /path/to/input-file.mp3 -ar 16000 /path/to/output-file.wav
```

正常用homebrew装```ffmpeg```， 弄好git，

```bash
git clone https://github.com/ggerganov/whisper.cpp.git
```

直接```make```即可，然后下载模型文件


```bash
cd models
bash ./download-ggml-model.sh small
```

弄transcript的时候使用```whisper-cli```，用`-f`指定稳健，用`-l zh`指定是中文（或者`-l auto`）

不过测试了一下，貌似没有用成Metal GPU，不知道啥问题，还得研究一下。