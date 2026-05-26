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

Then, compile your project along with the compiled libftprintf.a library.Algorithm and Data StructureArchitecture & Parsing: The core algorithm relies on a linear parser loop that iterates through the format string character by character. When a % character is encountered, the algorithm pauses, evaluates the immediately following character as a conversion specifier, and routes the execution to a dedicated helper function designed for that specific data type.  Data Structures: No complex data structures (like linked lists or trees) were used for the mandatory scope. Instead, the project strictly utilizes the va_list type provided by the <stdarg.h> library to sequentially extract variadic arguments off the stack. State tracking (such as the total count of printed characters) is maintained using simple integer counters passed by value or reference, ensuring a minimal memory footprint and strict compliance with the requirement that all heap-allocated memory be properly freed.  ResourcesThe following resources were referenced during the development of this project:  Manual Pages: man 3 printf, man 3 stdargDocumentation: Official IEEE Std 1003.1 (POSIX) specifications for printf behavior.AI Usage: AI was utilized strictly as an interactive tutor to clarify the conceptual mechanics of the <stdarg.h> macros (e.g., va_start, va_arg, va_end) and to troubleshoot compilation flags. No code generation was used to solve the actual routing logic or mathematical conversions, preserving the integrity of the foundational learning process.  
