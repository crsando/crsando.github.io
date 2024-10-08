---
layout: post
title: 测试MathJax渲染数学公式
tags: math
category: posts
---

Github Docs 支持直接在Markdown里写数学公式，比如

$$
    E = mc^2
$$

或者更复杂一点的：

$$
    (x+1)^n = \sum_{i=0}^{n} \left( \frac {n!} { i ! \cdot (n-i) ! } x^i \right)
$$

也包括直接写inline的公式，例如这样 $a^2+b^2=c^2$

或者

$$
\begin{equation}
    e^{i\pi} + 1 = 0
\end{equation}
$$


还在研究当中，这里记录一点研究的内容


### Reference

- [MathJax](https://www.mathjax.org/)
- [Using MathJax on a Github Page?](https://stackoverflow.com/questions/34347818/using-mathjax-on-a-github-page)
- [Markdown + Mathjax => PDF](https://tex.stackexchange.com/questions/290617/markdown-mathjax-pdf)
- [How Can I Convert Github-Flavored Markdown To A PDF](https://superuser.com/questions/689056/how-can-i-convert-github-flavored-markdown-to-a-pdf)
- [Pandoc With Chinese (简体中文)](https://github-wiki-see.page/m/jgm/pandoc/wiki/Pandoc-With-Chinese-(%E7%AE%80%E4%BD%93%E4%B8%AD%E6%96%87))
- [pandoc does not recognize Chinese characters](https://tex.stackexchange.com/questions/341809/pandoc-does-not-recognize-chinese-characters)
- [Building A Math Blog With Github Pages](https://medium.com/@argszero.reg/building-a-math-blog-with-github-pages-jekyll-mathjax-and-utterances-a-diy-guide-f07727d33716)