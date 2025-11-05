# smallest_array_8051
## Aim:
To Write an assembly language program in 8051 to find the smallest number in an array of N elements using conditional jump instructions.

## APPARATUS REQUIRED
- Personal computer with Keil software
## ALGORITHM:
1.Start the program.

2.Load the TMOD register with 01H to select Timer 0 .

3.Load the TH0 and TL0 registers with initial values 0FCH and 066H respectively to get approximately 1 ms delay.

4.Set the TR0 bit to start Timer 0.

5.Continuously check the TF0 (Timer 0 overflow flag) until it becomes 5.

6.When TF0 = 5, the delay is completed.

7.Clear TR0 to stop the timer.

8.Clear TF0 for future use.

9.End the program.

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

