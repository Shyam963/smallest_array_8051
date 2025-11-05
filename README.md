# smallest_array_8051
## Aim:
To Write an assembly language program in 8051 to find the smallest number in an array of N elements using conditional jump instructions.

## APPARATUS REQUIRED
- Personal computer with Keil software
## ALGORITHM:
1.Start the program.

2.Load the starting address of the numbers into Register R0 (e.g., 30H).

3.Load the counter register R2 with the total number of elements (05H).

4.Clear the accumulator A to start summation from zero.

5.Add the value pointed to by R0 to the accumulator using indirect addressing (ADD A, @R0).

6.Increment R0 to point to the next number in memory.

7.Decrement the counter R2 and repeat the addition until all 5 numbers are added.

8.Store the final sum in memory location 35H

9.Stop program execution.

10.End the program.

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
<img width="1916" height="281" alt="image" src="https://github.com/user-attachments/assets/fd183916-78e5-45aa-bbef-b84c1e75d689" />


### Result
Thus the smallest number of the array is found using 8051 keil and output is shown

