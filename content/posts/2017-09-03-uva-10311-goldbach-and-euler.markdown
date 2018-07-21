---
author: rimonmostafiz
comments: true
date: 2017-09-03 00:21:00+00:00
layout: post
link: http://www.rimonmostafiz.com/uva-10311-goldbach-and-euler/
slug: uva-10311-goldbach-and-euler
title: UVa 10311 - Goldbach and Euler
wordpress_id: 695
categories:
- uva
tags:
- idea
- prime-number
- problem-solving
---




**Problem Statement:**




[UVa 10311 - Goldbach and Euler](https://uva.onlinejudge.org/external/103/p10311.pdf)




We can express the problem statement like: Given an integer N (0 < N ≤ 108).




we have to find(if exists) two number P1 and P2 where,









 	
  * P1 and P2 both prime

 	
  * P1 + P2 = n

 	
  * P1 < P2

 	
  * P2 - P1  is minimized




**Solution Idea:**







First of all we need to find prime numbers between [0:108]. We can use memory efficient C++ implementation of [Sieve Of Eratosthenes](http://wp.me/p94Vft-m) to generate prime numbers up to 108 and store it in an Array.




 




Now we have to find the P1 and P2, first idea come to mind is though we have the prime list of all number up to N we can normally iterate throw the prime list and find P1 and P2 = N - P1 and check if P2 is also a prime and if yes then we can calculate and minimized the P2 - P1. if couldn't manage to find some P1 for that P2 is a prime also we can say N is not the sum of two primes! Definitely this idea is going to work for finding P1 and P2 but you will end up with a TLE for this IDEA!


Since the Time limit of the problem 10 S, but we need to find P1 and P2 more efficiently.

If we consider N is an Odd Number, can't we find P1 and P2 more efficiently? Well, it turns out that for odd numbers we can find P1 and P2 in O(1)! If N is odd, then one of the two primes P1 and P2 has to be even, while the other one has to be odd. Can you get it? we know ODD = ODD + EVEN. If one of the primes has to be even, then that prime would have to be 2. So, if N is odd we simply check if N-2 is prime or not, and if it is, then we know that P1 = 2 and P2 = N - 2, otherwise there is no solution.


We have concluded that for Odd numbers we can found P1 and P2 easily, now we have one possible case remaining and that if N is Even. There’s one thing that we could do that would improve significantly the complexity of the algorithm we can iterate only over the prime numbers. Since we already have a array full of primes below 108, we can binary search the location of N/2 and go down from it. Since there are 5.8*106 primes up to 108. That would make for a worse case of  5.8*106 iterations instead of 108/2.




 




Now We have improved things but, can we do even better? The discussion found in the problem statement about Goldbach’s conjecture and Euler’s ideas that there is a conjecture that an even number can always be expressed as the sum of two primes, though its a conjecture but we can assume it’s true for our purposes. This means that we can be reasonably confident that the process of finding  P1 will succeed for most even numbers, hopefully quickly enough that it doesn’t have to check millions of primes. Note that I said most even numbers, because we need two distinct primes P1 and P2 remember? For example, 14 can be expressed as the sum of two primes 7+7 but not as the sum of two distinct primes.






