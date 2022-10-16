# printf

  A formatted output conversion C program completed as part of the low-level programming and algorithm track at ALX Software Engineering Program. The program is a pseudo- recreation of the C standard library function, `printf`.

## Dependencies

  The `printf` function was coded on an Ubuntu 14.04 LTS machine with `gcc` version 4.8.4.

## Usage
  To use the `printf` function, assuming the above dependencies have been installed, compile all `.c` files in the repository and include the header `main.h` with any main function.
Example `main.c`:

```
#include "main.h"

int main(void)
{
    _printf("Hello, World!");

    return (0);
}
```

Compilation:

`$ gcc *.c -o tester`

Output:

```
$ ./tester
Hello, World!
$
```

## Description

The function `printf` writes output to standard output. The function writes under the control of a `format` string that specifies how subsequent arguments (accessed via the variable-length argument facilities of `stdarg`) are converted for output.

Prototype: `int printf(const char *format, ...);`

## Return Value

Upon successful return, `printf` returns the number of characters printed (excluding the terminating null byte used to end output to strings). If an output error is encountered, the function returns `-1`.

## Format of the Arguement String

The `format` string argument is a constant character string composed of zero or more directives: ordinary characters (not `%`) which are copied unchanged to the output stream; and conversion specifications, each of which results in fetching zero or more subsequent arguments. Conversion specification is introduced by the character `%` and ends with a conversion specifier. In between the `%` character and conversion specifier, there may be (in order) zero or more flags, an optional minimum field width, an optional precision and an optional length modifier. The arguments must correspond with the conversion specifier, and are used in the order given.

### Flag Characters
The character `%` may be followed by zero or more of the following flags:

For `o` conversions, the first character of the output string is prefixed with `0` if it was not zero already.
For `x` converions, `0x` is prepended for non-zero numbers.
For `X` conversions, `0X` is prepeneded for non-zero numbers.

Example `main.c`:
```
main(void)
{
    _printf("%#x\n", 7);
}
```
Output:

`0x7`

**(space)**

  * A blank is left before a positive number or empty string produced by a signed conversion.

Example `main.c`:
```
int main(void)
{
    _printf("% d\n", 7);
}

```
Output:

`7`


**+**

  * A sign (+ or -) is always placed before a number produced by signed conversion.
  * Overrides a space flag.
  
Example `main.c`:
```

int main(void)
{
    _printf("%+d\n", 7);
}
```
Output:

`+7`

---

# Tasks

These are all the tasks of this project, the ones that are completed link to the corresponding files.

### [0. I'm not going anywhere. You can print that wherever you want to. I'm here and I'm a Spur for life](./_printf.c)
* Write a function that produces output according to format.
  - c : converts input into a character
  - s : converts input into a string

### [1. Education is when you read the fine print. Experience is what you get if you don't](./print_nums.c)
* Handle the following conversion specifiers:
  - d : converts input into a base 10 integer
  - i : converts input into an integer

### [2. With a face like mine, I do better in print](./conversion_specifiers.c)
* Handle the following conversion specifiers:
  - b : the unsigned int argument is converted to binary

### [3. What one has not experienced, one will never understand in print](./print_bases.c)
* Handle the following conversion specifiers:
  - u : converts the input into an unsigned integer
  - o : converts the input into an octal number
  - x : converts the input into a hexadecimal number
  - X : converts the input into a hexadecimal number with capital letters

### [4. Nothing in fine print is ever good news](./write_functions.c)
* Use a local buffer of 1024 chars in order to call write as little as possible.

### [5. My weakness is wearing too much leopard print](./print_custom.c)
* Handle the following custom conversion specifier:
  - S : prints the string
  - Non printable characters (0 < ASCII value < 32 or >= 127) are printed this way: \x, followed by the ASCII code value in hexadecimal (upper case - always 2 characters)

### [6. How is the world ruled and led to war? Diplomats lie to journalists and believe these lies when they see them in print](./print_specs.c)
* Handle the following conversion specifier:
  - p : int input is converted to a pointer address

### [7. The big print gives and the small print takes away](./flag.c)
* Handle the following flag characters for non-custom conversion specifiers:
  - \+ : adds a \+ in front of signed positive numbers and a \- in front of signed negative numbers
  - space : same as \+, but adds a space (is overwritten by \+)
  - \# : adds a 0 in front of octal conversions that don't begin with one, and a 0x or 0X for x or X conversions

### [8. Sarcasm is lost in print] (./length_modifiers.c)
* Handle the following length modifiers for non-custom conversion specifiers:
  - l : converts d, i, u, o, x, X conversions in short signed or unsigned ints
  - h : converts d, i, u, o, x, X conversions in long signed or unsigned ints

### [9. Print some money and give it to us for the rain forests] (./field_width.c)
* Handle the field width for non-custom conversion specifiers.

### [10. The negative is the equivalent of the composer's score, and the print the performance] (./precision.c)
* Handle the precision for non-custom conversion specifiers.

### [11. It's depressing when you're still around and your albums are out of print] (./0_flag_character.c)
* Handle the 0 flag character for non-custom conversion specifiers.

### [12. Every time that I wanted to give up, if I saw an interesting textile, print what ever, suddenly I would see a collection] (./the_flag.c)
* Handle the - flag character for non-custom conversion specifiers.

### [13. Print is the sharpest and the strongest weapon of our party](./print_custom.c)
* Handle the following custom conversion specifier:
  - r : prints the reversed string

### [14. The flood of print has turned reading into a process of gulping rather than savoring](./print_custom_R.c)
* Handle the following custom conversion specifier:
  - R : prints the rot13'ed string

### [15. * ] (./above_options.c)
* All the above options work well together.

---

### Authors
* **Itah Judah** - (https://github.com/Jhudharh)
* **Solomon Thompson** - (https://github.com/soulo-mon)
