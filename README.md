# intro-c
Introduction to C programming language

## Foreword
This short introduction to C programming language is meant to be high-paced course to grasp key concepts of this kind and unforgiving language.
It does not explain most basic concepts of programming, but rather explains in what form they are present in C.
Also this course is not focused on optimal
and high-performance code wiriting. It you are looking for this, go look somewhere else.

## Organisation
Course is grouped into several list of tasks and exercises, each with some questions to answer. Those questions relate to key concepts of particular exercise. If you do not understand something or think "I will never need this..." - don't, those concepts are so essential that it is almost always present in some form or other. Extra questions will be marked as such.

Oh.. for developer environment I'll just use gcc on some linux distro. If you use Windows then it's actually your problem.

## Exercises


### `01. Introduction`
*"Get comfortable with essentials"*

#### "Hello, World!"
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


#### "My name is..."
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

#### "Can you spell it?"
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


#### What type are you?
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

#### You are not my type...
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


#### I'm pointing at...
Declare table of `int` of fixed length, length read from input (via malloc and on stack)
