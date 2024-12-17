# Ratsub

Ratsub is a recursive graphics language for making images - recursive, fractal, IFS, tilings, reptiles, Bezier curves, plane-filling curves etc - easily, with very short programs.

See ratsub.pdf for a tutorial and language spec, and the other two PDFs for many example programs and images.

## Requirements 

ghostscript, flex, bison

## Installation

1. Copy the subdiv folder to your computer and cd to it. Enter:

```
make
```

2. Copy the commands in ratsub_commands.txt to your .bash_profile in your home folder if using bash, or the equivalent for other shells. Restart the terminal to make the commands functional.


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

The subdiv compiler converts Ratsub code to PostScript .eps files, which ghostscript renders as PNG images.


The subdiv compiler is about 99% completed, there are still a few corners of the language spec not totally implemented yet. I rarely run into these when using it.

