---
title: "Fizzbuzz"
date: 2022-07-23T21:27:24-05:00
draft: false
author: "Manuel Alfaro"
description: "Resolviendo retos de programación"
tags: ["fizzbuzz","programación","C#","javascript","hackerrank"]
---

# FizzBuzz

Es un problema muy conocido y usado para realizar pruebas tecnicas en los
proceso de selección para programadores, existen ligeras variantes del mismo problema. usare
como muestra el que se encuentra en [HackerRank](https://www.hackerrank.com/challenges/fizzbuzz/problem) el cual dice lo siguiente:

> Write a short program that prints each number from 1 to 100 on a new line. <br />
For each multiple of 3, print "Fizz" instead of the number. <br />
For each multiple of 5, print "Buzz" instead of the number. <br />
For numbers which are multiples of both 3 and 5, print "FizzBuzz" instead of the number.

la traducción sería la siguiente

{{< admonition type=note title="Traducción" open=true >}}
Escribe un programa corto que imprima cada número del 1 al 100 en una nueva línea. <br/>
Para cada múltiplo de 3, imprime "Fizz" en lugar del número. <br/>
Para cada múltiplo de 5, imprime "Buzz" en lugar del número. <br/>
Para los números que son múltiplos de 3 y 5, imprime "FizzBuzz" en lugar del número.
{{< /admonition >}}


Para dicho problema planteo la siguiente solución escrita en _C#_


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


y si queremos hacerlo en _JavaScript_ sería de la siguiente forma

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



