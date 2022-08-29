---
title: "Fizzbuzz"
date: 2022-07-23T21:51:28-05:00
draft: false
author: "Manuel Alfaro"
description: "Resolviendo retos de programación"
tags: ["fizzbuzz","programación","C#","javascript","hackerrank"]
---

# FizzBuzz

The FizzBuzz problem is a classic test given in coding interviews. The task is simple: print integers 1 to N. For example we can find one example in [HackerRank](https://www.hackerrank.com/challenges/fizzbuzz/) with the next description:

> Write a short program that prints each number from 1 to 100 on a new line. <br />
For each multiple of 3, print "Fizz" instead of the number. <br />
For each multiple of 5, print "Buzz" instead of the number. <br />
For numbers which are multiples of both 3 and 5, print "FizzBuzz" instead of the number.

A way for solve this problem in C# language


```c#
using System;
using System.Collections.Generic;
using System.IO;
class Solution {
    static void Main(String[] args) {
        /* Enter your code here. Read input from STDIN. Print output to STDOUT. Your              class should be named Solution */
        for(byte i = 1; i <= 100; i++)
        {
            string response = string.Empty;
            
            if(i % 3 == 0)
                response += "Fizz";
                
            if(i % 5 == 0)
                response += "Buzz";
                
            if(string.IsNullOrEmpty(response))
                response = i.ToString();
                            
            Console.WriteLine(response);
        }
        
    }
}
```


And for JavaScript:


```js
process.stdin.resume();
process.stdin.setEncoding("ascii");
process.stdin.on("data", function (input) {
    for (let i=1; i<=100; i++) {
        let response = "";
        
        if (i%3 === 0)
            response += "Fizz";
        if (i%5 === 0) {
            response += "Buzz";}
        if (response === "")
            response = i;   
            
        console.log(response);
    }
});
```


This solution is one of many ways