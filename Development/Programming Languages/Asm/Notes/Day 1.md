![[kernel.excalidraw]]

**Interface** = **kernel**. 
**Kernel** = controlling **hardware** by using its **system calls**
**lib** that contains these **system calls** similar to **opengl**

envoke **system call** = **kernel** interupt program
what performs the task of system call = **driver**

function number/OPCODE
1 = exit (1 arg)
4 = write (3 args)

EAX=1 -> interupt -> exit
EAX=4 -> interupt -> write

EAX=4
`usigned int fd` = **file descriptor** -> stdint stdout
`char *buf`
`size_t count`

```
SECTION .data
hw db 'Hello World', 0Ah

SECTION .text
global _start

_start:
    mov     edx, 12     ; size_t count
    mov     ecx, hw     ; char *buf
    mov     ebx, 1      ; unsigned int fd 
    mov     eax, 4      ; write
    int     80h
```

