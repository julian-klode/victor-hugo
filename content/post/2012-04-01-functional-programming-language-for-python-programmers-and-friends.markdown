---
author: juliank
comments: true
date: 2012-04-01 16:33:17+00:00
link: https://juliank.wordpress.com/2012/04/01/functional-programming-language-for-python-programmers-and-friends/
slug: functional-programming-language-for-python-programmers-and-friends
title: Functional programming language for Python programmers and friends
wordpress_id: 572
categories:
- General
tags:
- '42'
- functional
- functional programming
- mutable
- pure
- python
- unique
- uniqueness type system
---

Just for you, and this time in the Pythonesque rendering.

    
    <strong>module</strong> main:
        <strong>import</strong> std (range)
        <strong>import</strong> std.io (printf, IO)
    
        #<em> print the Fahrenheit-Celcius table for fahr = 0, 20, ..., 300</em>
        <strong>function</strong> main(<strong>mutable</strong> IO io):
            <strong>Int</strong> lower = 0    #<em> lower bound</em>
            <strong>Int</strong> upper = 300  #<em> upper bound</em>
            <strong>Int</strong> step = 20    #<em> step</em>
            <strong>for</strong> <strong>Int</strong> fahr in range(lower, upper, step):
                <strong>Double</strong> celcius = 5 * (fahr - 32) / 9
                std.io.printf(io, "%3d\t%6.1f\n", fahr, celcius)


It does not really look like it, but this language is purely functional. It represents side effects using unique types. If you declare a mutable parameter, you basically declare a unique input parameter and a unique output parameter.

I’m also giving you a list implementation

    
    <strong>module</strong> std.container.list:
    
        <em>## The standard singly-linked list type</em>
        <strong>type</strong> List[E]:
            Nil                     ##<em> empty list</em>
            Node:
                E value             ##<em> current value</em>
                List[E] next        ##<em> remaining list</em>
    <em> </em>


_
_And yes, both languages should be able to be represented using the same abstract syntax tree. The only change is the replacement of the opening curly brace by a colon, the removal of the closing curly bracket and semicolons, the replacement of C-style comments with Python-style comments and the requirement of indentation; oh and the for statement gets a bit lighter as well.
