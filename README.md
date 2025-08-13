# 🖋️ Ft_printf

The `ft_printf` project is one of three exercice of the second circle.

This project consists to recreating a litle part of the reel function printf.

Through this project, we revisit the basics of C such as :
- print a simple char
- print a string
- print numbers
- print in hexa-decimal format
- print address
- print usigned munbers

And, the center of this project is to use `variable arguments`.

![](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

## 🛠️ Function prototype and requirements

Name of the function : ft_printf.

Prototype : `int    ft_print( const char* format, ... );`

Formats supported : `c s p d i u x X %`

Here, a litle explanation of each format :

| Format Specifier | Description |
|------------------|-------------|
| %                | % followed by another % character writes % to the screen. |
| c                | writes a single character. |
| s                | writes a character string. |
| p                | writes an implementation-defined character sequence defining a pointer address. |
| d or i           | writes a signed integer to decimal representation. |
| u                | writes an unsigned integer to decimal representation. |
| x or X           | writes an unsigned integer to hexadecimal representation. |


![](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

### ⚙️ Usage

Step 1:

Run in your shell environment :
```bash
git clone https://github.com/jotudela/ft_printf.git
cd ft_printf
make
```
Now you have `libftprintf.a` which is a static library.

---

Step 2:

Next step is to import `libftprintf.a` and `ft_printf.h` at the root of your own project, and use
the ft_printf linked to it.

There is a simple program called `test.c`:

```bash
//Include header form ft_printf.h
#include "ft_printf.h"
#include <stdio.h>

int main(void)
{
    char c = 'a';
    char *str = "Hello World !";
    int p = 42;
    int d = 66;
    int i = 21;
    unsigned int u = 32;

    // Test with my ft_printf
    ft_printf("FT : %%, ");
    ft_printf("%c, ", c);
    ft_printf("%s, ", str);
    ft_printf("%p, ", (void *)&p);
    ft_printf("%d, ", d);
    ft_printf("%i, ", i);
    ft_printf("%u, ", u);
    ft_printf("%x, %X\n", 0xFF, 0xFF);

    // Test with printf standard
    printf("STD : %%, ");
    printf("%c, ", c);
    printf("%s, ", str);
    printf("%p, ", (void *)&p);
    printf("%d, ", d);
    printf("%i, ", i);
    printf("%u, ", u);
    printf("%x, %X\n", 0xFF, 0xFF);

    return 0;
}
```

---

Step 3:

Once the file is builded, compile it with this :
```bash
gcc -Wall -Wextra -Werror libftprintf.a test.c -o program
```

---

Step 4:

Run with this :
```bash
./program
```

And your terminal will print :
```bash
%, a, Hello World !, address of variable p, 66, 21, 32, ff, FF
```

My final grade :

![](imgs/100_percent.png)

![](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

## 🤝 Contribution
Contributions are open, make a pull request or open an issue 🚀
