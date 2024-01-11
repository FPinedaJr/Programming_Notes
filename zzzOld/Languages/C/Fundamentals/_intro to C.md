- C is a general-purpose programming language created by *Dennis Ritchie* at the Bell Laboratories in 1972.
- It is a very popular language, despite being old.
- C is strongly associated with UNIX, as it was developed to write the UNIX operating system.

## Why Learn C?

- It is one of the most popular programming language in the world.
- If you know C, you will have no problem learning other popular programming languages such as Java, Python, C++, C#, etc, as the syntax is similar.
- C is very fast, compared to other programming languages, like Java and Python.
- C is very versatile; it can be used in both applications and technologies.

## Difference between C and C++

- Basically C++ is an upgrade of C
- C++ was developed as an extension of C, and both languages have almost the same syntax
- C++ supports OOP
- C++ includes additional features compared to C, such as classes, objects, inheritance, polymorphism, templates, exceptions, and namespaces
- Most valid C code can be compiled and executed as C++ code, with some minor modifications
- However, not all C programs can be compiled as C++
- C and C++ both provide manual memory management

## More on C

```C
#include <stdio.h>

int main (void)
{
	printf("hello, world\n");
}
```
stdio.h means standard io.h, this is a header file hence the `.h`
To use the standard input/output such as mouse, you have to include the `<stdio.h>`, the standard I/O library.

CLI - command line interface

C uses compiler
The codes that you wrote in the IDE needs to be compiled so that the computer can understand it.
Hence you need an extra step of compiling the code before you can run it.
And everytime you changes something to your code, you need to recompile.

printf. f stands for formatted.

```C
#inlcude <cs50.h>
#include <stdio.h>

int main (void)
{
	string answer = get_string("What's your name? ");
	printf("Hello, %s\n", answer);
}
```
`#include <cs50.h>` tells your computer that your are using the get_string function, otherwise it will give you an error.
`%s` tells your computer to put  a string here.

arguments or parameters are just fancy way of saying inputs in a function.

tip: `ctrl+l` will clear your terminal in linux.
`cd..` will go to the parent directory. By the same reasoning
`./hello` means that you are explicitly telling the computer that you are working with the current directory.

`counter++;` and `counter += 1;` is the syntactic sugar of the same code `counter = counter + 1;`/