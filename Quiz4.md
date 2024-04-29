```assembly
section .text
        global _start

_start:
        call _area

        mov eax, 1
        int 0x80
_area:
        mov eax, [x]
        add eax, [y]
        add eax, [z]
        mov [result], eax

        ret

segment .bss
        result resb 1

section .data
        x dd 5
        y dd 7
        z dd 3
```

