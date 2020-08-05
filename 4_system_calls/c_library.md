# Using a C Library
Writing standalone programs with just system calls is cool, but rare. We would like to use the good stuff in the C
library.
Remember how in C execution “starts” at the function main ? That’s because the C library actually has the _start
label inside itself! The code at _start does some initialization, then it calls main , then it does some