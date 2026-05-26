*This project has been created as part of the 42 curriculum by vmeharia.*

## Description
This project is a custom implementation of the C library function `printf(). The goal is 
to recreate its core functionality, allowing us to format and print data to the standard
output while learning how to manage variadic functions in C. 

Unlike the original standard library function, this version does not implement buffer
management. It successfully handles the following mandatory conversion specifiers:
* [cite_start]`%c`: Prints a single character.
* [cite_start]`%s`: Prints a string.
* [cite_start]`%p`: Prints a void pointer argument in hexadecimal format.
* [cite_start]`%d` / `%i`: Prints a decimal (base 10) integer.
* [cite_start]`%u`: Prints an unsigned decimal (base 10) number.
* [cite_start]`%x`: Prints a number in hexadecimal (base 16) lowercase format.
* [cite_start]`%X`: Prints a number in hexadecimal (base 16) uppercase format.
* [cite_start]`%%`: Prints a percent sign.

## Instructions
This project is written in C and compiled into a static library named `libftprintf.a`. 

### Compilation
To compile the library, clone the repository and run `make` at the root of the directory.
The provided `Makefile` compiles the source files using `cc` with the mandatory flags
`-Wall`, `-Wextra`, and `-Werror`.

It uses the `ar` command to create the library archive (the use of `libtool` is strictly forbidden.

The `Makefile` includes the following rules:
* `make` / `make all`: Compiles the library.
* `make clean`: Removes the object files.
* `make fclean`: Removes the object files and the `libftprintf.a` binary.
* `make re`: Fully recompiles the project.

### Usage
To use `ft_printf` in your own projects, include the header file in your C code:
#include "ft_printf.h"
