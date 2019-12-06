# Assemblyl Language Basics

## Overview

## Running assembly
```bash
nasm -f elf hello.asm
ld -m elf_i386 -s -o hello hello.o
./hello      
# Hello, world!
```