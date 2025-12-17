# ft_printf
A custom implementation of the C `printf` function.

This project focuses on variadic functions, formatted output parsing, and low-level output handling using file descriptors.

ft_printf was an important milestone in understanding how formatted output works internally and how to design extensible, modular C code.

### Overview
`ft_printf` is a static library (`libftprintf.a`) that reimplements a subset of the standard C `printf` function.

It supports multiple format specifiers and handles formatted output using only low-level system calls (`write`), without relying on libc printf.

## This project strengthened my understanding of:
- Variadic arguments (`stdarg.h`)
- Format string parsing
- Number base conversions
- Memory-safe output handling
_ Modular C design

## Supported Conversions
- `%c`  – character
- `%s`  – string
- `%d` / `%i` – signed integer
- `%u`  – unsigned integer
- `%x` / `%X` – hexadecimal (lowercase / uppercase)
- `%p`  – pointer address
- `%%`  – literal percent sign

### Build
```bash
make
```

### This generates:
```txt
# libftprintf.a
```

### Usage
Include the header and link the library:

```c
include "ft_printf.h"

int main(void)
{
     ft_printf("Hello %s, number: %d\n", "world", 42);
     return (0);
 }
```

### Compile with:

```bash
cc main.c libftprintf.a
```

### Files

- `ft_printf.c`   – main printf logic and format parsing
- `ft_putchar.c`  – character output helper
- `ft_putstr.c`   – string output helper
- `ft_putnbr.c`   – signed number output
- `ft_putunbr.c`  – unsigned number output
- `ft_puthex.c`   – hexadecimal conversion and output
- `ft_voidptr.c`  – pointer address formatting

## Notes

- No buffering is used; all output is written directly via `write`
- The implementation prioritizes correctness and clarity over optimization
- This library was built to 42 project constraints and coding standards

## Author

Syed Ahmad
GitHub: https://github.com/AlwIkigai
