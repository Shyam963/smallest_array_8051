# smallest_array_8051
## Aim:
To Write an assembly language program in 8051 to find the smallest number in an array of N elements using conditional jump instructions.
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
<img width="1920" height="1080" alt="Screenshot 2025-10-23 195720" src="https://github.com/user-attachments/assets/96c18255-5382-4395-b743-cd26ef899144" />
<img width="1920" height="1080" alt="Screenshot 2025-10-23 195714" src="https://github.com/user-attachments/assets/a6e3a060-6730-4bcf-bddf-55a64c61624f" />

### Result
Thus the smallest number of the array is found using 8051 keil and output is shown

