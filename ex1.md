
# `01. Introduction`
*"Get comfortable with essentials"*

## `Ex 01. "Hello, World!"`
Write simple "Hello, World!" program, compile and run it.

```C
#include <stdio.h>

int main()
{
  printf("Hello, World");
  return 0;
}
```

```bash
$ gcc hello.c -o hello
```

**Questions:**
1. What does `#include` clause do?
1. Get to know what other standard libraries C has. Just know what is already written and you can just use it in the future. I just want you to know in the future if you will need some function to just remeber something like this *"Oh, wait, C has math library, maybe `exp()` is there?"*
1. What does `int main()` do?
1. Function return type, what is that?
1. What does `printf` do?
1. Why `return 0`, what would happen if replaced with `return 1`?


## `Ex 02. "My name is..."`
Write a program that asks you about your name and later prints it on the output.

For example:
``` bash
$ ./askname
Hello, what is your name?
<input your name here>
Oh, hello <name>, nice to meet you!
```

**Questions:**
1. What function do you use to get user input?
2. How do you store the input? (what is `char` and `char[]`)
3. How long is your buffer table and why?
4. What are ASCII characters? Check some basic properties, i.e. values of letters and numbers, and basic whitespace characters.

## `Ex 03. "Can you spell it?"`
Use previous program and modify it to write each character of input into separate line

For example:
```bash
$ ./spelling
Hello, what is your name?
Adam
A
d
a
m
```

**Questions:**
1. What function do you use to get the length of input? Did you write your own?
2. For spelling you could use `for` or `while` loop, try doing it with other one you already used.
3. For input `Adam` what is the value of `buffer[4]`? What is it? What would happen if it wasn't there?
4. If you haven't already, write your own function that calculates the length of input string.


## `Ex 04. "What type are you?"`
Write program that reads from input all the different types: `int`, `char`, `float` etc. (Check standard types in C docs) and then write it to the output.

For example:
```bash
$ ./types
Input int: <input_int>
Input float: <input_float>
...

You wrote:
<int> as int
<float> as float
...
```

**Questions:**
1. What does `&` do?
2. What does `*` do?

## `Ex 05. "You are not my type..."`
Using program from previous exercise mix some things around. I.e read values as previously but try to write them in other format, for example `int` as `float` and so one. Try as many as possible. 'Print as' is uderstood as using proper format string for `printf()`. You might have to cast some values to get results.

For example:
```bash
$ ./types
Input int: <input_int>
Input float: <input_float>
...

You wrote:
int <int> as int is <as_int>
int <int> as float is <as_float>
...
```

**Questions:**
1. Why some outputs are so strange?
2. Did you get any compilation errors? If not insert proper compiler flags to get some. What do those error mean?
3. What is casting? Explicit vs implicit, what are the differences?
