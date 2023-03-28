# _printf - Custom Implementation of printf function

_printf is a custom implementation of the printf function in C programming language. It
supports a subset of the standard printf format specifiers, as well as some custom
specifiers. This implementation is designed to handle a variety of input formats and
provide output according to a format.

## Usage

To use the _printf function, first include the header file main.h in your C program:
 include "main.h"

Then, call the function with the desired format specifier and arguments:
int num = 42;
char str[] = "hello, world";
_printf("The answer is %d and the message is %s\n", num, str);
The above code will output:
The answer is 42 and the message is hello, world

## Supported Format Specifiers

_printf supports the following standard format specifiers:
● %c - prints a character
● %s - prints a null-terminated string
● %d or %i - prints a signed integer
● %u - prints an unsigned integer
● %o - prints an octal integer
● %x - prints a hexadecimal integer in lowercase letters
● %X - prints a hexadecimal integer in uppercase letters
● %p - prints a pointer address in hexadecimal
● %% - prints a literal % character

In addition to the standard specifiers, _printf supports the following custom specifiers:
● %b - prints an unsigned integer in binary
● %S - prints a string, escaping non-printable characters with their ASCII code value
in hexadecimal

### Flags, Field Width, and Precision

_printf supports several flags for formatting output, including:
● - to left-justify the output
● + to always show a sign (+ or -) for signed numbers
● 0 to pad the output with zeroes instead of spaces
● (space) to insert a space before a positive number (ignored when + is present)
● # to prefix non-zero hexadecimal and octal values with 0x and 0, respectively
It also supports specifying a field width and precision for output, as in the standard
printf function.

### Implementation Details

_printf uses a local buffer of 1024 characters to minimize calls to the write function. It
handles format specifiers, flags, field width, and precision using a combination of string
manipulation and conditional logic. It also performs argument type checking and
formatting based on the specified format specifier.

###  Authors

This _printf was developed by Amina Afolabi and Aishat Adeladun Adewoyin as
a project for ALX's Sofware Engineering course (Cohort 12).
