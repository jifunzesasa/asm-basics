# System calls
System calls are APIs for the interface between the user space and the kernel space. We have already used the system calls. sys_write and sys_exit, for writing into the screen and exiting from the program, respectively.

## Linux System Calls
You can make use of Linux system calls in your assembly programs. You need to take the following steps for using Linux system calls in your program −

## Put the system call number in the EAX register.
Store the arguments to the system call in the registers EBX, ECX, etc.
Call the relevant interrupt (80h).

The result is usually returned in the EAX register.
There are six registers that store the arguments of the system call used. These are the EBX, ECX, EDX, ESI, EDI, and EBP. These registers take the consecutive arguments, starting with the EBX register. If there are more than six arguments, then the memory location of the first argument is stored in the EBX register.

The following code snippet shows the use of the system call sys_exit −

```asm
mov	eax,1		; system call number (sys_exit)
int	0x80		; call kernel
```
The following code snippet shows the use of the system call sys_write −

```asm
mov	edx,4		; message length
mov	ecx,msg		; message to write
mov	ebx,1		; file descriptor (stdout)
mov	eax,4		; system call number (sys_write)
int	0x80		; call kernel

```
All the syscalls are listed in /usr/include/asm/unistd.h, together with their numbers (the value to put in EAX before you call int 80h).

The following table shows some of the system calls used in this tutorial −