# smallest_array_8051
## Aim:
To Write an assembly language program in 8051 to find the smallest number in an array of N elements using conditional jump instructions.

## APPARATUS REQUIRED
- Personal computer with Keil software

## Program:
```
ORG 0000H
MOV R0, #30H
MOV R1, #04H
MOV A, @R0
MOV B, A
DEC R1
INC R0
NEXT:
MOV A, @R0
CJNE A, B, CHECK
SJMP SKIP
CHECK:
JNC SKIP
MOV B, A
SKIP:
INC R0
DJNZ R1, NEXT
MOV 40H, B
HERE: SJMP HERE
END

```
### Output
<img width="1919" height="1006" alt="Screenshot 2025-11-05 100515" src="https://github.com/user-attachments/assets/64cc939f-45cf-466d-99b2-630c39344a4c" />
<img width="1919" height="287" alt="Screenshot 2025-11-05 100510" src="https://github.com/user-attachments/assets/b3ac345b-cc5c-4af3-953e-e45aa4fad36c" />


### Result
Thus the smallest number of the array is found using 8051 keil and output is shown

