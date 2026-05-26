* This project has been created as part of the 42 curriculum by vmeharia. *

# ft_printf

## Description
This project is a custom implementation of the C library function `printf(). The goal is 
to recreate its core functionality, allowing us to format and print data to the standard output while learning how to manage variadic functions in C[cite: 14, 95]. 

Unlike the original standard library function, this version does not implement buffer management[cite: 100]. It successfully handles the following mandatory conversion specifiers[cite: 101]:
* [cite_start]`%c`: Prints a single character[cite: 110].
* [cite_start]`%s`: Prints a string[cite: 111].
* [cite_start]`%p`: Prints a void pointer argument in hexadecimal format[cite: 112].
* [cite_start]`%d` / `%i`: Prints a decimal (base 10) integer[cite: 113, 114].
* [cite_start]`%u`: Prints an unsigned decimal (base 10) number[cite: 115].
* [cite_start]`%x`: Prints a number in hexadecimal (base 16) lowercase format[cite: 116].
* [cite_start]`%X`: Prints a number in hexadecimal (base 16) uppercase format[cite: 117].
* [cite_start]`%%`: Prints a percent sign[cite: 118].

## Instructions
[cite_start]This project is written in C and compiled into a static library named `libftprintf.a`[cite: 21, 94]. 

### Compilation
[cite_start]To compile the library, clone the repository and run `make` at the root of the directory[cite: 104]. [cite_start]The provided `Makefile` compiles the source files using `cc` with the mandatory flags `-Wall`, `-Wextra`, and `-Werror`[cite: 27]. [cite_start]It uses the `ar` command to create the library archive (the use of `libtool` is strictly forbidden)[cite: 103].

[cite_start]The `Makefile` includes the following rules[cite: 29]:
* `make` / `make all`: Compiles the library.
* `make clean`: Removes the object files.
* `make fclean`: Removes the object files and the `libftprintf.a` binary.
* `make re`: Fully recompiles the project.

### Usage
To use `ft_printf` in your own projects, include the header file in your C code:
```c
#include "ft_printf.h"
