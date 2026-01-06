# alterkage
A minimal digital mirror where you meet yourself.

.model small
.stack 100h
.code

main proc
    mov ah, 1        ; input a character
    int 21h
    sub al, 48       ; ASCII to number
    mov cl, al       ; store input in CL

print:
    mov dl, cl
    add dl, 48       ; number to ASCII
    mov ah, 2
    int 21h

    add cl, 3        ; gap of 3
    cmp cl, 9
    jle print        ; loop while <= 9

    mov ah, 4Ch
    int 21h
main endp
end main


mov bl,1
mov cl, 9
lebel a
cmpblcl
jl leb b
jmp leb c
leb b
mov dlbl
add dl48
movah2
int2
int 21h
add bl3
jmpleva
lebc
