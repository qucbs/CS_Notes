In order to run hello.c on the system, the individual C statements must be translated by other programs into a sequence of low-level machine-language instructions.

These instructions are then packaged in a form called an <span style="color:rgb(173, 66, 255)">executable object program</span> and stored as a binary disk file. Object programs are also referred to as executable object files. 

On a Unix system, the translation from source file to object file is performed by a <span style="color:rgb(173, 66, 255)">compiler driver</span>:

![[Coding/CS_Notes/Images/image.png]]

**Preprocessing phase:**
The preprocessor (cpp) modifies the original C program according to directives that begin with the ‘#’ character. For example, the `#include <stdio.h>` command in line 1 of hello.c tells the preprocessor to read the contents of the system header file stdio.h and insert it directly into the program text.

**Compilation phase:**
The compiler (cc1) translates the text file hello.i into the text file hello.s, which contains an assembly-language program.

**Assembly phase:**
Next, the assembler (as) translates hello.s into machine language instructions, packages them in a form known as a relocatable object program, and stores the result in the object file hello.o.

**Linking phase:**
Notice that our hello program calls the printf function, which is part of the standard C library provided by every C compiler. The printf function resides in a separate precompiled object file called printf.o, which must somehow be merged with our hello.o program. The linker (ld) handles this merging. The result is the hello file, which is an executable object file (or simply executable) that is ready to be loaded into memory and executed by the system. 









