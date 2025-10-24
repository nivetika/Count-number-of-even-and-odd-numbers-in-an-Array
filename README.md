# Count-number-of-even-and-odd-numbers-in-an-Array
## Aim
Write an assembly language program in 8051 to count the number of even and odd numbers in an array of 10 elements and display the counts.

## Apparatus Required
- Personal Computer  
- Keil µVision software  
---

## Algorithm
1. Initialize registers (R0–R3)
2. Read each element from memory
3. Use RRC to check LSB (Carry flag)
4. Increment even or odd counters
5. Store results at 50H and 51H
6. Stop execution
---

## Program
```
ORG 00H
LJMP MAIN


MAIN:
MOV R0,#30H
MOV R1,#00H
MOV R2,#00H
MOV R3,#0AH

LOOP:
MOV A,@R0
RRC A
JNC EVEN_COUNT
INC R2
SJMP NEXT

EVEN_COUNT:
INC R1

NEXT:
INC R0
DJNZ R3, LOOP

FINISH:
MOV 50H,R1
MOV 51H,R2
SJMP $

END
```

## OUTPUT

![WhatsApp Image 2025-10-24 at 10 36 29_2549436e](https://github.com/user-attachments/assets/54bec479-dd5b-40b3-b1b5-454300d62f45)

![WhatsApp Image 2025-10-24 at 10 36 44_206dad58](https://github.com/user-attachments/assets/2db033f5-dec7-4479-8dea-7f13f3e36b1e)


## RESULT
Thus to write an assembly language program in 8051 to count the number of even and odd numbers in an array of 10 elements and display the counts was done using keil software.

