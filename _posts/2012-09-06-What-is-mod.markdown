---
layout: post
title: What is % Mod ?
tags:
- MIT OCW Intro to Comp Science
- Programming
- 2012
---

When I first started to learn programming one of my first coding projects was one the old [MIT OCW Intro to Computer Science and Programming](http://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-00sc-introduction-to-computer-science-and-programming-spring-2011/) courses. The course itself has since then been drastically updated, and is much more accessible at this point. Back then the problem was to determine all the prime numbers between 1 and 100 using a simple piece of python code. 

Everything up to this point had been cake. Without too much stress or *mind-bending* I was cruising along the OCW programming course. This problem was difficult. I remember, at one point, almost crying in front of the computer because I was having serious issues knowing how to put together a solution to this problem.

The sad part is, I know what my problem was now, and it was such a simple one. I really didn't understand what **% Mod** meant. I understood that it had something to do with division, but the rest I think went in one ear and out the other. 

Mod, or %, is a symbol that provides with you a remainder. For example:

4 % 2 = 0
8 % 2 = 0
15 % 5 = 0

All of these equations result in zero, because when you **mod** 4 or 8 by two, the division is exact and there are no *remainders* leftover. This is the same for 15 % 5.

5 % 3 = 2
15 % 4 = 3

If you **mod** 5 by 3, well 3 only goes into 5 once with a remainder of 2. Subsequently if you **mod** 15 by 4, 4 goes into 15 3 times with a remainder of 3. 

Because I didn't understand this simple aspect, finding the best way to determine a prime number seemed, and I think I'm quoting myself here, 'so hard.' Because a prime number is something that isn't divisible by anything, when *moded* (is that a word?) it should always produce a remainder. I think you can see where this is going.
Basically using mod makes it very easy to identify prime numbers, because you would simply go through each number from 1 to 100, check if each of them produces a remainder when modded by each number of 1 through 100. If it does for each, then, as far as we can tell, it's a prime number.

Symbol-shock can be killer. Push through it anyways.  
   

