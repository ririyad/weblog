---
author: rimonmostafiz
comments: true
date: 2017-08-29 21:39:00+00:00
layout: post
link: http://www.rimonmostafiz.com/uva-406-prime-cuts/
slug: uva-406-prime-cuts
title: UVa 406 - Prime Cuts
wordpress_id: 696
categories:
- uva
tags:
- idea
- prime-number
- problem-solving
---




 




**Problem Statement:**






[UVa 406 – Prime Cuts](http://uva.onlinejudge.org/external/4/406.html)


Before beginning I want to say the problem description seems quite awkward to me, for me it took a time to understand what is actually asked by the problem. but when I found out its very easy to code.







**
Solution Idea:**




First of all use [Sieve of Eratosthenes](http://wp.me/p94Vft-m) to generate primes between 1000. You will be given two numbers N and C, then you need to make a list of primes between 1 to N(inclusive). For this problem you need to consider 1 as a Prime. Now find out the size of the list. Let represent the size of the list with S. Now if size of the list is even then you need to print C*2 items. If the size of the list is odd then you need to print C*2 - 1 items. Consider K is the number of item you need to print.
Here comes the question form where should start printing form the list. The condition is if K>S then you need to print all primes form 1 to N, otherwise you should start form (S-K)/2 th position of the list and print next K items.



