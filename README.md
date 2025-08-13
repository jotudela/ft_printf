# 🖋️ Ft_printf

The `ft_printf` project is one of three exercice of the second circle.

This project consists to recreating a litle part of the reel function printf.

Through this project, we revisit the basics of C such as :
- print a simple char
- print a string
- print numbers
- print in hexa-decimal format
- print adress
- print usigned munbers

And, the center of this project is to use `variable arguments`.

![](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

## 🛠️ Function prototype and requirements

Name of the function : ft_printf.

Prototype : `int    ft_print( const char* format, ... );`

Formats supported : `c s p d i u x X %`

Here, a litle explanation of each format :

| Specifier |
| Format Specifier | Description |
| c | write a single character |
| s | write a string |
| p | write writes an implementation-defined character sequence defining a pointer address |
| d | write a decimal number in base 10 |
| i | write a integer number in base 10 |
| u | write a unsigned number |
| x or X | writes an unsigned integer to hexadecimal representation |

![](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

### ⚙️ Usage

Step 1:

Run in your shell environment :
```bash
git clone https://github.com/jotudela/Libft.git
cd libft
make
```
Now you have `libft.a` which is a static library.

---

Step 2:

Next step is to import `libft.a` and `libft.h` at the root of your own project, and use
the functions linked to it.

There is a simple program called `test.c`:

```bash
//Include header form libft.h
#include "libft.h"

int main( void )
{
    //ft_putstr_fd is a function which take a string and a file descriptor as arguments.
    ft_putstr_fd("Hello World !", 1);
    return 0;
}
```

Step 3:

Once the file is builded, compile it with this :
```bash
gcc -Wall -Wextra -Werror libft.a test.c -o program
```

Step 4:

Run with this :
```bash
./program
```

And your terminal will print :
```bash
Hello World !
```

![](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

## 🤝 Contribution
Contributions are open, make a pull request or open an issue 🚀
