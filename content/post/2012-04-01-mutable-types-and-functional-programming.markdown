---
author: juliank
comments: true
date: 2012-04-01 15:41:17+00:00
link: https://juliank.wordpress.com/2012/04/01/mutable-types-and-functional-programming/
slug: mutable-types-and-functional-programming
title: '[updated] Functional programming language for C programmers and friends'
wordpress_id: 541
categories:
- General
tags:
- '42'
- C
- functional
- functional programming
- mutable
- pure
- unique
- uniqueness type system
---

Just for you:


    
    <strong>module</strong> main {
        <strong>import</strong> std (range);
        <strong>import</strong> std.io (printf, IO);
     
        <em>/* print the Fahrenheit-Celcius table
            for fahr = 0, 20, ..., 300 */</em>
        <strong>function</strong> main(<strong>mutable</strong> IO io) {
            <strong>Int</strong> lower = 0;   <i>// lower bound</i>
            <strong>Int</strong> upper = 300; <i>// upper bound</i>
            <strong>Int</strong> step = 20;   <i>// step</i>
            <strong>for</strong> (<strong>Int</strong> fahr in range(lower, upper, step)) {
                <strong>Double</strong> celcius = 5 * (fahr - 32) / 9;
                std.io.printf(io, "%3d\t%6.1f\n", fahr, celcius);
            }
        }
    }



It does not really look like it, but this language is purely functional. It represents side effects using unique types. If you declare a mutable parameter, you basically declare a unique input parameter and a unique output parameter.

I'm also giving you a list implementation


    
    
    <strong>module</strong> std.container.list {
    
        <i>/** The standard singly-linked list type */</i>
        <strong>type</strong> List[E] {
            Nil;                    <i>/** empty list */</i>
            Node {
                E value;            <i>/** current value */</i>
                List[E] next;       <i>/** remaining list */</i>
            }
        }
    }
    



Thus are only excerpts from a document with tens of pages and the reference implementation of the standard library. The incomplete working draft for the language is attached: [JAK Programming Language Early Working Draft (28 pages)](https://juliank.files.wordpress.com/2012/04/jlang1.pdf).

**Update:** Fixed the link.
