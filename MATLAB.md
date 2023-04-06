**Introduction**:
 ======
MATLAB is a high-level programming language that is widely used for numerical computation and data analysis. It has a simple and intuitive syntax that makes it easy to learn and use. It is particularly useful for engineers and scientists who need to perform complex calculations and data analysis.

**Syntax and Semantics**:
======
MATLAB has a simple and intuitive syntax that is easy to learn and use. It uses English-like commands to perform calculations and manipulate data. MATLAB supports many built-in functions that can perform complex calculations with a single line of code. MATLAB also allows the user to define their own functions and scripts. Syntax and semantics are fundamental concepts in programming languages, including MATLAB. Syntax refers to the set of rules that define how to write valid commands or expressions in a language. In other words, it's about the grammar and structure of the language. Semantics, on the other hand, refers to the meaning of those commands or expressions. In other words, it's about what the code actually does.
For example:
```MATLAB
% Define a function to calculate the factorial of a number
function result = factorial(n)
    if n == 0
        result = 1;
    else
        result = n * factorial(n-1);
    end
end

% Calculate the factorial of 5 using the defined function
factorial(5)
```

MATLAB has a vast collection of built-in functions, covering a wide range of mathematical, scientific, engineering, and graphical tasks. 
Here are a few examples:
1) sqrt(x): This function returns the square root of the input argument x. For example:
```MATLAB
>> sqrt(9)
ans = 3
```  
2) sin(x): This function returns the sine of the input argument x, which is assumed to be in radians. For example:
```MATLAB
>> sin(pi/2)
ans =
     1
```  
3) sum(x): This function returns the sum of all the elements in the input argument x. For example:
```MATLAB
>> A = [1 2 3; 4 5 6; 7 8 9];
>> sum(A)
ans =
    12    15    18
```  
4) max(x): This function returns the maximum element in the input argument x. For example:
```MATLAB
>> A = [1 2 3; 4 5 6; 7 8 9];
>> max(A)
ans =
     7     8     9
```  
5) rand(n): This function generates a matrix of size n-by-n with random elements between 0 and 1. For example:
```MATLAB
>> rand(2)
ans =
    0.8147    0.1270
    0.9058    0.9134
```  
While these built-in functions can be extremely useful, it's important to use them appropriately and understand their underlying semantics. For example, the use of the 'rand' function can easily lead to non-reproducible results if not seeded appropriately, while the 'polyfit' function can easily overfit noisy data if the polynomial order is too high. Understanding the underlying semantics of these functions can help avoid common pitfalls and produce more reliable and accurate results.
Overall, learning MATLAB syntax and semantics is essential for using the language effectively and efficiently. By understanding the basic building blocks, exploring less common components, and considering the language from different perspectives, students in CS2613 can develop a comprehensive understanding of MATLAB that will serve them well in their future studies and careers.


------
Racket provides a rich set of built-in data types and structures, including lists, vectors, hash tables, and sets. It also provides a comprehensive set of 
libraries for working with files, networking, databases, and graphical user interfaces. The libraries are well-documented and easy to use, and they provide a solid 
foundation for developing complex software systems. We will discuss some of the data structures and libraries as follows:

**Lists**: Racket has built-in support for linked lists, which can be created using the cons function and manipulated using functions such as car, cdr, and append. For example:
```racket
(define my-list (list 1 2 3))  ; creates a list
(car my-list)                  ; returns 1
(cdr my-list)                  ; returns (2 3)
(append my-list (list 4 5))    ; returns (1 2 3 4 5)
```

**Hash Tables**: Racket also supports hash tables, which can be created using the make-hash function and manipulated using functions such as hash-set!, hash-ref, and hash-keys. 
For example:
```racket
(define my-hash (make-hash))    ; creates a hash table
(hash-set! my-hash "key" "value") ; set a value for a key
(hash-ref my-hash "key" #f)      ; returns "value"
(hash-keys my-hash)              ; returns '("key")
```

**Strings**: Racket has a built-in string data type, which can be created using double quotes and manipulated using functions such as string-append, string-ref, and string-length. 
For example:
```racket
(define my-string "hello")             ; creates a string
(string-append my-string " world")     ; returns "hello world"
(string-ref my-string 1)               ; returns #\e (the second character)
(string-length my-string)              ; returns 5
```

**Vectors**: Vectors are similar to lists, but they provide constant-time access to individual elements. They are created using the vector keyword and are enclosed in square brackets. For example:
```racket
(define my-vector (vector 1 2 3 4))    ; creates a vector
```
When discussing built-in libraries we have to mention:
**Math Library**: The math library provides a range of mathematical functions, such as sqrt, log, sin, cos, and more.

**File I/O Library**: The file I/O library provides functions for reading and writing files, such as open-input-file, open-output-file, read-line, write-line, and more.

**Web Library**: The web library provides functions for working with web-based protocols, such as http, ftp, and smtp.

**GUI Library**: The GUI library provides functions for creating graphical user interfaces, such as windows, buttons, text boxes, and more.

We will use an example to show the use of Math library in Racket:
```racket
#lang racket

(require math)

(define num 16)
(define sqrt-num (sqrt num))

(displayln sqrt-num)
```
In this example, we require the math library, then define a number and compute its square root using the sqrt function. Finally, we display the result using the 'displayln' function.

**Supported Paradigms**:
======
Racket supports a wide range of programming paradigms, including object-oriented, functional, and procedural programming. It also supports declarative
and imperative programming styles, and it allows the programmer to choose between static and dynamic typing. Racket provides powerful features such as polymorphism 
and inheritance, which make it easy to write complex software systems.

To write functions in Racket, we can split it into multiple ways of writing. Each way of writing the function has an advantage over the other depending on the type of task needed to be done.

**Normal Functions**:
These functions are mostly used for simple functions and would only depend on the parameters passed in to the function. Normal Functions or pure functions may prove to have a higher level of obscurity which would prove difficult to the user reading the code.

**Recursion Functions**:
Using recursion functions normally in any language in the beginning is quite frightening but having a good amount of experience with recursions made writing recursions here not as difficult as well. Recursions can also sometimes lead to the code being less optimized.

**Referential Transparency**

**First-class Functions**:
First-class functions are basically using functions and passing that function to another function as a parameter.

Racket also supports Functional Reactive Programming and Language Oriented Programming which uses macros.

**Functional Reactive Programming**:
It is used for reactive programming which uses the building blocks of functional programming. Functional Reactive Programming is used for GUI's which is used for designing the functions

**Language Oriented Programming**:
This is a very abstract programming type as we basically create a new language and use that language to solve the problem/task. Rackets supports a wide variety of Language Oriented Programming to help the users.

**Under the Hood**:
======
Racket is a compiled language that uses a virtual machine to execute programs. It supports both just-in-time and ahead-of-time compilation, which allows it to 
achieve high performance. Racket manages memory automatically, using a garbage collector to reclaim unused memory. Racket provides excellent support for interfacing 
with other languages, and it can be used to write programs that interact with hardware.

**Conclusion**:
======
In this journal, we have explored the various aspects of the Racket programming language from the perspective of the four quadrants of the framework. 
Racket is a powerful and flexible language that provides a solid foundation for developing complex software systems. By learning about its syntax, data structures, 
supported paradigms, and underlying implementation, we can become better programmers and use the language more effectively.
