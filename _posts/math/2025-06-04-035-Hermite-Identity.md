---
layout: post
title: On A Proof of Hermite's Identity
tags: math,education,algebra
category: math
---

[Source](https://www.jstor.org/stable/2311413?read-now=1&oauth_data=eyJlbWFpbCI6InFpdS5taW5nZGEucGt1QG91dGxvb2suY29tIiwiaW5zdGl0dXRpb25JZHMiOltdLCJwcm92aWRlciI6Im1pY3Jvc29mdCJ9&seq=1#page_scan_tab_contents)

*Yoshio Matsuoka, Kagoshima University, Japan*

The following identity, due to Hermite, is well known :

$$
\lfloor x \rfloor + 
\lfloor x + \frac{1}{n} \rfloor + 
\lfloor x + \frac{2}{n} \rfloor + 
\cdots 
\lfloor x + \frac{n-1}{n} \rfloor
= \lfloor nx \rfloor
$$

where $x$ and $n$ denote any real number and any natural number resepectively and $\lfloor x \rfloor$ denotes, as usual, the greatest integer not execeeding $x$

We give another proof.

Let

$$
    f(x) = \lfloor nx \rfloor - 
    \lfloor x \rfloor - 
\lfloor x + \frac{1}{n} \rfloor -
\lfloor x + \frac{2}{n} \rfloor - 
\cdots 
\lfloor x + \frac{n-1}{n} \rfloor
$$

Then 

$$
    f(x + \frac{1}{n}) = \lfloor nx + 1 \rfloor
    - 
\lfloor x + \frac{1}{n} \rfloor -
\lfloor x + \frac{2}{n} \rfloor - 
\cdots 
\lfloor x + \frac{n-1}{n} \rfloor -
\lfloor x + \frac{n}{n} \rfloor = f(x)
$$

On the other hand, if $0\leqslant x < \frac{1}{n}$, we have $f(x) \equiv 0$. Therefore $f(x) \equiv 0$.
