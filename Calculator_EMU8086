
                                  ;;;;;;;;;;;;;;;;;;;;;   Simple Hexa-Decimal Calculator ;;;;;;;;;;;;;;;;;;;;;
                   

.MODEL SMALL
.STACK 100H
.DATA   

mode db "Select a preferred mode:$"
fac db "Enter a Number for factorial (0-8):$"
n1 db "Enter the base number:$"
n2 db "Enter the exponent (0-5):$" 
a1 db "Enter First Digit for Number 1 (MSB):$"
a2 db "Enter Second Digit for Number 1 (LSB):$" 
a7 db "Enter a Number:$"
;;;; num1 = a1a2 
num1 dw ?
a3 db "Enter First Digit for Number 2 (MSB):$"
a4 db "Enter Second Digit for Number 2 (LSB):$" 
;;;; num2 = a3a4
num2 dw ? 
num3 dw ?
result dw ? 
remainder dw ?
quocient dw ?   
n db "Enter the value of N:$"
r db " Enter the value of R:$"  
result1 dw ? 
result2 dw ? 
result3 dw ?
cc dw ?                                                                                                                                               
av db "Enter Total Numbers (1-9):$"
avg dw ? 
res dw ? 
rem dw ?
yes db " The Result is (Hexa decimal) : $"  
rrr db " The Reaminder is (Hexadecimal) : $"
ind db "INVALID$"


num db ? 
count db ?
n10 dw ?  
n20 dw ?
ccc db num dup (?)
num10 dw ?
num20 dw ?  
answer dw ? 
hold dw ? 
avv db "Enter the Equation: $"


.CODE
    MAIN PROC
    MOV AX,@DATA
    MOV DS,AX 

    ;code here  
    
    lea dx,mode
    mov ah,9
    int 21h 
    
    mov ah,1
    int 21h
    mov bl,al 
    
    mov dl,0dh
    mov ah,2
    int 21h  
    mov dl,0ah
    mov ah,2
    int 21h 

    
    check1:
    
    cmp bl,21h
    je factorial_inp  
    
    cmp bl, 5Eh
    je power  
    
    cmp bl,2Bh
    je addition
    
    cmp bl,2Dh
    je substraction 
    
    cmp bl,2Ah
    je multiplication 
    
    cmp bl,2Fh
    je division
    
    cmp bl, 50h
    je permutation
    
    cmp bl, 43h
    je combination   
    
    cmp bl, 41H
    je Average         ; floor_avg   
    
    cmp bl, 45H
    je evaluate
    
    jmp exit
    
  
;;;;;;;;;;; Additon  


  addition:
     ;;;;number1
   lea dx,a1
   mov ah,9
   int 21h 
    
   mov ah,1
   int 21h 
   
   mov ah,0h
   sub al,30h
   mov num1,ax
   
   
   mov dl,0dh
   mov ah,2
   int 21h  
   mov dl,0ah
   mov ah,2
   int 21h 
   
   lea dx,a2
   mov ah,9
   int 21h 
    
   mov ah,1
   int 21h 
   sub al,30h
   mov ch,0
   mov cl,al
   
   mov dx,10d
   mov ax,num1
   mul dx
   add ax,cx
   
   mov num1,ax   ;;;;;; num1
     
   mov dl,0dh
   mov ah,2
   int 21h  
   mov dl,0ah
   mov ah,2
   int 21h 
   
        ;;;;number2
   lea dx,a3
   mov ah,9
   int 21h 
    
   mov ah,1
   int 21h 
   
   mov ah,0h
   sub al,30h
   mov num2,ax
   
   
   mov dl,0dh
   mov ah,2
   int 21h  
   mov dl,0ah
   mov ah,2
   int 21h 
   
   lea dx,a4
   mov ah,9
   int 21h 
    
   mov ah,1
   int 21h 
   sub al,30h
   mov ch,0
   mov cl,al
   
   mov dx,10d
   mov ax,num2
   mul dx
   add ax,cx
   
   mov num2,ax   ;;;;;; num2  
   
   mov ax,num1
   mov bx,num2
   add ax,bx
   mov result,ax
   jmp print  
   
;;;;;;;;;;; Substraction

  substraction:
     ;;;;number1
   lea dx,a1
   mov ah,9
   int 21h 
    
   mov ah,1
   int 21h 
   
   mov ah,0h
   sub al,30h
   mov num1,ax
   
   
   mov dl,0dh
   mov ah,2
   int 21h  
   mov dl,0ah
   mov ah,2
   int 21h 
   
   lea dx,a2
   mov ah,9
   int 21h 
    
   mov ah,1
   int 21h 
   sub al,30h
   mov ch,0
   mov cl,al
   
   mov dx,10d
   mov ax,num1
   mul dx
   add ax,cx
   
   mov num1,ax   ;;;;;; num1
     
   mov dl,0dh
   mov ah,2
   int 21h  
   mov dl,0ah
   mov ah,2
   int 21h 
   
        ;;;;number2
   lea dx,a3
   mov ah,9
   int 21h 
    
   mov ah,1
   int 21h 
   
   mov ah,0h
   sub al,30h
   mov num2,ax
   
   
   mov dl,0dh
   mov ah,2
   int 21h  
   mov dl,0ah
   mov ah,2
   int 21h 
   
   lea dx,a4
   mov ah,9
   int 21h 
    
   mov ah,1
   int 21h 
   sub al,30h
   mov ch,0
   mov cl,al
   
   mov dx,10d
   mov ax,num2
   mul dx
   add ax,cx
   
   mov num2,ax   ;;;;;; num2  
   
   mov ax,num1
   mov bx,num2
   sub ax,bx
   mov result,ax
   jmp print
   
;;;;;;;;;;; Multiplication

 multiplication:
     ;;;;number1
   lea dx,a1
   mov ah,9
   int 21h 
    
   mov ah,1
   int 21h 
   
   mov ah,0h
   sub al,30h
   mov num1,ax
   
   
   mov dl,0dh
   mov ah,2
   int 21h  
   mov dl,0ah
   mov ah,2
   int 21h 
   
   lea dx,a2
   mov ah,9
   int 21h 
    
   mov ah,1
   int 21h 
   sub al,30h
   mov ch,0
   mov cl,al
   
   mov dx,10d
   mov ax,num1
   mul dx
   add ax,cx
   
   mov num1,ax   ;;;;;; num1
     
   mov dl,0dh
   mov ah,2
   int 21h  
   mov dl,0ah
   mov ah,2
   int 21h 
   
        ;;;;number2
   lea dx,a3
   mov ah,9
   int 21h 
    
   mov ah,1
   int 21h 
   
   mov ah,0h
   sub al,30h
   mov num2,ax
   
   
   mov dl,0dh
   mov ah,2
   int 21h  
   mov dl,0ah
   mov ah,2
   int 21h 
   
   lea dx,a4
   mov ah,9
   int 21h 
    
   mov ah,1
   int 21h 
   sub al,30h
   mov ch,0
   mov cl,al
   
   mov dx,10d
   mov ax,num2
   mul dx
   add ax,cx
   
   mov num2,ax   ;;;;;; num2  
   
   mov ax,num1
   mov bx,num2
   mul bx  
   mov result,ax
   jmp print   


;;;;;;;;;;;;;; Division           
  division:
     ;;;;number1
   lea dx,a1
   mov ah,9
   int 21h 
    
   mov ah,1
   int 21h 
   
   mov ah,0h
   sub al,30h
   mov num1,ax
   
   
   mov dl,0dh
   mov ah,2
   int 21h  
   mov dl,0ah
   mov ah,2
   int 21h 
   
   lea dx,a2
   mov ah,9
   int 21h 
    
   mov ah,1
   int 21h 
   sub al,30h
   mov ch,0
   mov cl,al
   
   mov dx,10d
   mov ax,num1
   mul dx
   add ax,cx
   
   mov num1,ax   ;;;;;; num1
     
   mov dl,0dh
   mov ah,2
   int 21h  
   mov dl,0ah
   mov ah,2
   int 21h 
   
        ;;;;number2
   lea dx,a3
   mov ah,9
   int 21h 
    
   mov ah,1
   int 21h 
   
   mov ah,0h
   sub al,30h
   mov num2,ax
   
   
   mov dl,0dh
   mov ah,2
   int 21h  
   mov dl,0ah
   mov ah,2
   int 21h 
   
   lea dx,a4
   mov ah,9
   int 21h 
    
   mov ah,1
   int 21h 
   sub al,30h
   mov ch,0
   mov cl,al
   
   mov dx,10d
   mov ax,num2
   mul dx
   add ax,cx
   
   mov num2,ax   ;;;;;; num2  
   
   mov ax,num1
   mov bx,num2
   div bx
   mov remainder,dx
   mov result, ax
   jmp print   
  
  
    
;;;;;;;;;;;POWER
  power:
   lea dx,n1
   mov ah,9
   int 21h 
    
   mov ah,1
   int 21h
   mov bl,al
   sub bl,30h 
    
   mov dl,0dh
   mov ah,2
   int 21h  
   mov dl,0ah
   mov ah,2
   int 21h 
   
   lea dx,n2
   mov ah,9
   int 21h 
    
   mov ah,1
   int 21h
   mov cl,al
   sub cl,30h
   mov dl,2h
   
   mov al,bl
   mov ah,0h
   
 
   cmp cl,0h
   je c_0 
   cmp cl,1h
   je c_1 
   jg other  
   
  other:
   cmp cl,5h
   jle calc_power
   jg exit

  calc_power:
  mul bl
  inc dl
  mov result,ax
  cmp dl,cl
  jg print
  jmp calc_power  
  
  c_1:
   mov result,ax
   jmp print 
   
  c_0:
   mov result,0h
   jmp print
  
  
   
    
;;;;;;;;; Factorial   
  factorial_inp:
  lea dx,fac
  mov ah,9
  int 21h

  mov ah,1
  int 21h
    
  sub al,30h
  mov ah,0
  mov cx,ax
  sub cx,1h
  cmp ax,1h 
  jle fac_1
  jg maxx_factorial
  
  fac_1:
   mov ax,1
   mov result,ax
   jmp print 
  
  maxx_factorial:
   cmp ax,9h
   jl factorial
  
  factorial:   
   mul cx
   sub cx,1h
   cmp cx,0h 
   mov result,ax
   je print 
   jmp factorial    
   
   
;;;;;;;;;;;;;;;; Combination 

  
Combination:
   lea dx,n
   mov ah,9
   int 21h 
    
   mov ah,1
   int 21h
   mov bl,al
   sub bl,30h
   mov bh,0
   mov num1,bx  
  
    
   mov dl,0dh
   mov ah,2
   int 21h  
   mov dl,0ah
   mov ah,2
   int 21h 
   
   lea dx,r
   mov ah,9
   int 21h 
    
   mov ah,1
   int 21h 
   mov cl,al
   sub cl,30h
   mov ch,0h 
   mov num2,cx
   
   mov cx,num2
   mov bx,num1 
   
   cmp bx,9h
   je exit
   cmp cx,9h
   je exit
   
   cmp cx,0h
   je zero
             
   cmp cx,bx
   je o1
   
  
   mov cx,num2
   mov bx,num1         
   sub bx,cx
   
   cmp bx,1h
   jl print_ind
   mov num3,bx 
   jmp cmb1 
   
  zero:
   mov dx,1
   mov result,dx
   jmp print
   
  o1:
   mov cx,1h
   mov result,cx
   jmp print   
    
   
 cmb1:  
   mov ax,num1
   mov cx,ax
   cmp ax,1
   je r1
   sub cx,1h
   cmp ax,1h 
   jle fac_12
   jg factorial2  


 r1:
   mov ax,1
   mov result1,ax
   jmp cmb2 
  
  
  
  fac_12:
   mov ax,1
   mov result1,ax
   jmp exit 
  
  factorial2:   
   mul cx
   sub cx,1h
   cmp cx,0h 
   mov result1,ax
   je cmb2 
   jmp factorial2
    
   
 cmb2: 
   mov ax,num2
   mov cx,ax
   cmp ax,1
   je r2
   sub cx,1h
   cmp ax,1h 
   jle fac_122
   jg factorial22    
   
  r2:
   mov ax,1
   mov result2,ax
   jmp cmb3 
  
   
   
  fac_122:
   mov ax,1
   mov result2,ax
   jmp exit 
  

  factorial22:   
   mul cx
   sub cx,1h
   cmp cx,0h 
   mov result2,ax
   je cmb3 
   jmp factorial22 
   
  cmb3: 
   mov ax,num3
   mov cx,ax 
   sub cx,1h
   cmp ax,1h 
   jle fac_1223
   jg factorial223    
   
  fac_1223:
   mov ax,1
   mov result3,ax
   jmp exit 
  

  factorial223:   
   mul cx
   sub cx,1h
   cmp cx,0h 
   mov result3,ax
   je calu 
   jmp factorial223  
   
  calu:
   mov dx,0
   mov ax,result1
   mov bx,result2
   div bx 
   mov cc,ax 
   mov cx,result3 
   mov ax,cc
   div cx 
   mov result,ax 
   jmp print
                
;;;;;;;;;;;;;;;; Permutation 

  
Permutation:
   lea dx,n
   mov ah,9
   int 21h 
    
   mov ah,1
   int 21h
   mov bl,al
   sub bl,30h
   mov bh,0
   mov num1,bx  
  
    
   mov dl,0dh
   mov ah,2
   int 21h  
   mov dl,0ah
   mov ah,2
   int 21h 
   
   lea dx,r
   mov ah,9
   int 21h 
    
   mov ah,1
   int 21h 
   mov cl,al
   sub cl,30h
   mov ch,0h 
   mov num2,cx
   
   mov cx,num2
   mov bx,num1 
   
   cmp bx,9h
   je exit 
   cmp cx,9h
   je exit
   
   cmp cx,0h
   je zero
   
   cmp bx,cx
   jl print_ind
  
   mov cx,num2
   mov bx,num1         
   sub bx,cx
   

   mov num3,bx 
   jmp pmb1 
   

 pmb1:  
   mov ax,num1
   mov cx,ax
   cmp ax,1
   je rr1
   sub cx,1h
   cmp ax,1h 
   jle faac_12
   jg faactorial2  


 rr1:
   mov ax,1
   mov result1,ax
   jmp cmb2 
  
  
  
  faac_12:
   mov ax,1
   mov result1,ax
   jmp exit 
  
  faactorial2:   
   mul cx
   sub cx,1h
   cmp cx,0h 
   mov result1,ax
   je pmb3 
   jmp faactorial2
    
  pmb3: 
   mov ax,num3
   mov cx,ax 
   sub cx,1h
   cmp ax,1h 
   jle faac_1223
   jg faactorial223    
   
  faac_1223:
   mov ax,1
   mov result3,ax 
   jmp calu1
    
  faactorial223:   
   mul cx
   sub cx,1h
   cmp cx,0h 
   mov result3,ax
   je calu1 
   jmp faactorial223  
   
  calu1:

   mov ax,result1 
   mov cx,result3 
   div cx 
   mov result,ax 
   jmp print    
   
   
;;;;;;;;;;;;;Evaluate 
evaluate:  
    lea dx,av
    mov ah,9
    int 21h
  
    mov ah,1
    int 21h 
    
    mov ah,0
    sub ax,30h
    mov num,al
    
    mov dl,0dh
    mov ah,2
    int 21h  
    mov dl,0ah
    mov ah,2
    int 21h
    
    lea dx,avv
    mov ah,9
    int 21h 
    
    
    mov si,0
    mov ch,0  
    mov cl,num     
    
    take_in:
    
      mov ah,1
      int 21h
      mov bl,al 
      mov ccc[si],bl 
      inc si
    loop take_in   
                   
       
    mov ch,0 
    mov cl,num 
    mov si,0 
    mov ah,2 
    mov bl,2Ah
    mov count,0h
    
    find1:
     mov dl, ccc[si]  
     inc si 
     add count,1h 
     cmp dl,bl
     je found 
    loop find1  
    
    
    found:
     mov bl, count
     add bl,0h 
     mov bh,0
     mov n10,bx
     sub bx,2h
     mov n20,bx
  
    
     
    mov si,0
    mov ch,0
    mov cl,num
    
    blehh:  
     cmp si,n20
     je aeh
     jmp ohh
  

    aeh:
      mov al,ccc[si]
      mov ah,0
      mov bx,ax
      sub bx,30h
      add si,2
      mov al,ccc[si]
      mov ah,0
      sub ax,30h
      mul bx
      push ax
      inc si
      sub cx,2
      
    ohh:
      mov al,ccc[si]
      mov ah,0 
      sub ax,30h
      push ax
      inc si    
      
    loop blehh  
     
      
      
    mov ch,0
    mov cl,num 
    sub cx,1h

    
    oy:  
     pop dx 
     add dx,30h 
     ;mov ah,2
     ;int 21h
     
     cmp dx, 30h
     jge number   
     jl wow 
     
    wow: 
     cmp dx, 2Dh
     je minus
     jl plus 
     
    loop oy 
     

number:
  sub dx,30h
  mov num10,dx
 

     
plus:
  pop dx 
  sub dx,30h
  mov num20,dx 
  mov ax, num10
  mov bx, num20
  add ax,bx 
  add ax,30h
  push ax


minus: 
  pop dx 
  sub dx,30h
  mov num2,dx 
  mov bx, num10
  mov ax, num20
  sub ax,bx 
  add ax,30h
  push ax
 
 
 jmp exit
         

          

                   
;;;;;;;;;;; Average

  average: 
   lea dx,av
   mov ah,9
   int 21h 
    
   mov ah,1
   int 21h 
   
   mov ah,0
   sub al,30h
   mov avg,ax
   
   
   mov dl,0dh
   mov ah,2
   int 21h  
   mov dl,0ah
   mov ah,2
   int 21h 
    
    
   mov bx,0
   mov cx,avg  
   sub cx,1
   jmp l1
 
   
  l1:
    
   mov dl,0dh
   mov ah,2
   int 21h  
   mov dl,0ah
   mov ah,2
   int 21h
    
   lea dx,a7
   mov ah,9
   int 21h 
    
   mov ah,1
   int 21h 
   
   mov ah,0h
   sub al,30h
   mov num1,ax   
    
   mov ah,1
   int 21h 
   sub al,30h
   mov ch,0
   mov cl,al
   
   mov dx,10d
   mov ax,num1
   mul dx
   add ax,cx 
    
   mov cx,avg
   sub cx,1
   add result,ax  
   inc bx
   cmp bx,cx
   jle l1 
   mov ax, result
   mov cx, avg
   div cx
   mov result,ax 
   mov remainder,dx 
   jmp print
   jmp print_r
   
   
print_r:  

  mov dl,0dh
  mov ah,2
  int 21h  
  mov dl,0ah
  mov ah,2
  int 21h
  
  lea dx,rrr
  mov ah,9
  int 21h
  
  mov bx, remainder  
  mov res, bx
  jmp print1
   
   
print:  

  mov dl,0dh
  mov ah,2
  int 21h  
  mov dl,0ah
  mov ah,2
  int 21h
  
  lea dx,yes
  mov ah,9
  int 21h
  
  mov bx, result  
  mov res, bx
  jmp print1
 
    
         
print1: 
  
    mov ax,res
    mov dx,0
    mov cx,1000h
    div cx
    
    mov rem,dx
    mov dl,al
    
    cmp dl,9h
    jg pchar1
    jle pnum1
 
    
print2:    
    mov ax,rem
    mov dx,0 
   
    mov cx,100h
    div cx
    
    mov rem,dx
    mov dl,al
    cmp dl,9h
    jg pchar2 
    jle pnum2  

           
print3:              
    mov ax,rem
    mov dx,0
    mov cx,10h
    div cx
    
    mov rem,dx
    mov dl,al
    cmp dl,9h
    jg  pchar3 
    jle pnum3
    
print4:    
    
    mov ax,rem
    mov dx,0
    mov cx,1h
    div cx
    
    mov rem,dx
    mov dl,al
    cmp dl,9h
    jg pchar4
    jle pnum4

            
 pchar1:
  add dl,37h 
  mov ah,2
  int 21h
  jmp print2
 
  
 pnum1:
  add dl,30h 
  mov ah,2
  int 21h
  jmp print2  
  
  
 pchar2:
  add dl,37h 
  mov ah,2
  int 21h
  jmp print3
 
  
 pnum2:
  add dl,30h 
  mov ah,2
  int 21h
  jmp print3
  
  
 pchar3:
  add dl,37h 
  mov ah,2
  int 21h
  jmp print4
 
  
 pnum3:
  add dl,30h 
  mov ah,2
  int 21h
  jmp print4
 
 
  
 pchar4:
  add dl,37h 
  mov ah,2
  int 21h
  jmp exit
 
  
 pnum4:
  add dl,30h 
  mov ah,2
  int 21h
  jmp exit
  
 print_ind:  
  mov dl,0dh
  mov ah,2
  int 21h  
  mov dl,0ah
  mov ah,2
  int 21h
  
  lea dx,yes
  mov ah,9
  int 21h
  
  lea dx,ind
  mov ah,9
  int 21h
   
  jmp exit
  

   
    
 exit:
    MAIN ENDP
END MAIN


 exit:
    MAIN ENDP
END MAIN
