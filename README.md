# Ratsub

Ratsub is a recursive graphics language for making images - recursive, fractal, IFS, tilings, reptiles, Bezier curves, plane-filling curves etc - easily, with very short programs.

See language tutorial and examples in the 3 PDF ebooks.

## Requirements 

ghostscript, flex, bison

## Installation

1. Copy the commands in ratsub_commands.txt to your .bash_profile in your home folder if using bash, or the equivalent for other shells. Restart the terminal to make the commands functional.

2. Copy the subdiv folder to your computer and cd to it. Enter:

```
make
```

### On error
At this point, some combinations of versions of C compiler, flex, and bison, produce an error message "implicit declaration of function 'yylex' is invalid in C99". See discussion [here](https://lists.gnu.org/r/bug-bison/2022-01/msg00002.html).

In that case, paste:

```
int yylex (void);
```

to near the top of the subdiv.tab.c file, then enter:

```
cc -o subdiv subdiv.tab.c lex.yy.c
```

### Usage

cd to the subdiv folder.

If your program is called myprog.sdv, enter e.g.

```
ratsub myprog 10
```

to produce the level 10 image, or

```
ratsub myprog 1 10
```

to see levels 1 to 10.

For a larger image, use "ratsubhd" instead of "ratsub" in the command.

See the 3 PDF ebooks for tutorial, language spec, and many example programs and images.

### More info

The subdiv compiler converts Ratsub code to PostScript .eps files.


The subdiv compiler is about 99% completed, there are still a few corners of the language spec not totally implemented yet. I rarely run into these when using it.

