# Assemblly Language Basics

## Overview

## Running assembly

```sh
 nasm -felf64 hello.asm && ld hello.o && ./a.out
```


```bash
nasm -f elf hello.asm
ld -m elf_i386 -s -o hello hello.o
./hello
# Hello, world!
```



REF:
- https://cs.lmu.edu/~ray/notes/nasmtutorial/
- https://www.tutorialspoint.com/assembly_programming/assembly_environment_setup.htm