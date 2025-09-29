# Welcome to Assignment 04
This document is made to compare formatting between C and Python.

## Integer Formatting
### C99 printf
An example using printf to print an integer with width, padding, and sign:
```
#include <stdio.h>

int main()
{
    int n = 42;
    printf("%5d\n", n); // width 5, right-aligned
    printf("%+5d\n", n); // width 5, show sign
    printf("%05d\n", n); // width 5, pad with zeros
    return 0;
}
```
Output:
```
   42
  +42
00042
```
### Python print
An example using oldstyle % formatting:
```
n = 42
print("%5d" % n) # width 5, right-aligned
print("%+5d" % n) # width 5, show sign
print("%05d" % n) # width 5, pad with zeros
```
An example using f-strings:
```
n = 42
print(f"{n:5}") # width 5, right-aligned
print(f"{n:+5}") # width 5, show sign
print(f"{n:05}") # width 5, pad with zeros
```
Output:
```
   42
  +42
00042
```

## Float Formatting
### C99 printf
An example using printf to print a float with 2 decimal places, fixed width, and scientific notation:
```
#include <stdio.h>

int main()
{
    float f = 3.14159;
    printf("%8.2f\n", f); // width 8, 2 decimals
    printf("%08.2f\n", f); // pad with zeros
    printf("%e\n", f); // scientific notation
    return 0;
}
```
Output:
```
    3.14
00003.14
3.141590e+00
```
### Python print
An example using oldstyle % formatting:
```
f = 3.14159
print("%8.2f" % f)
print("%08.2f" % f)
print("%e" % f)
```
An example using f-strings:
```
f = 3.14159
print(f"{f:8.2f}")
print(f"{f:08.2f}")
print(f"{f:e}")
```
Output:
```
    3.14
00003.14
3.141590e+00
```

## String Formatting
### C99 printf
An example of left and right alignment with width: 
```
#include <stdio.h>

int main()
{
    char *s = "Hello";
    printf("%-10s!\n", s); // left-aligned, width 10
    printf("%10s!\n", s); // right-aligned, width 10
    return 0;
}
```
Output:
```
Hello     !
     Hello!
```
### Python print
An example of using oldstyle % formatting: 
```
s = "Hello"
print("%-10s!" % s)
print("%10s!" % s)
```
An example using f-strings:
```
s = "Hello"
print(f"{s:<10}!")
print(f"{s:>10}!")
print(f"{s:^10}!")
```
Output:
```
Hello     !
     Hello!
  Hello   !
```

## Tables
one table comparing output of C99 printf and Python print for each type <br>
collumns: type, example code (C), example code (python), output

| Type | Example Code (C) | Example Cpde (Python) | Output |
|--|--|--|--|
| int | `printf("%5d", 42);` | `"%5d" % 42` | `   42` |
| int | `printf("%+5d", 42);` | `"%+5d" % 42` | `  +42` |
| int | `printf("%05d", 42);` | `"%05d" % 42` | `00042` |
| float | `printf("%8.2f", 3.14159);` | `"%8.2f" % 3.14159` | `    3.14` |
| float | `printf("%e", 3.14159);` | `"%e" % 3.14159` | `3.141590e+00` |
| string | `printf("%-10s!", "Hello");` | `"%-10s" % "Hello"` | `Hello     !` |
| string | `printf("%10s!", "Hello");` | `"%10s" % "Hello"` | `     Hello!` |

![](https://upload.wikimedia.org/wikipedia/commons/thumb/1/15/Cat_August_2010-4.jpg/1200px-Cat_August_2010-4.jpg)

## Links
C99 printf reference: https://en.cppreference.com/w/c/io/fprintf <br>
Python old-style % formatting: https://docs.python.org/3/library/stdtypes.html#printf-style-string-formatting <br>
Python f-strings: https://docs.python.org/3/reference/lexical_analysis.html#f-strings

