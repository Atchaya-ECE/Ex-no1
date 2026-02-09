# Arithmetic-operation-using-8086
# 8086 Assembly Language Programs for Arithmetic Operations

## AIM

To write and execute Assembly Language Programs to perform arithmetic operations for the 8086 microprocessor.

---

## APPARATUS REQUIRED

* Personal Computer with MASM Software

---

## 1. ADDITION

#### Algorithm

1. Initialize memory location in HL register.
2. Store 1st data.
3. Increment HL to enter 2nd data.
4. Move 2nd number to accumulator.
5. Decrement HL.
6. Add value in memory with accumulator.
7. Store result.
8. Stop.


## FLOW CHART
<img width="707" height="1024" alt="image" src="https://github.com/user-attachments/assets/b5a7062d-e294-47cd-9683-a40de25e82de" />


#### Program

```asm
CODE SEGMENT
ASSUME CS:CODE, DS:CODE
ORG 1000H
MOV CL,00H
MOV AX,1234H
MOV BX,1234H
ADD AX,BX
JNC L1
INC CL
L1:MOV SI,1200H
MOV [SI],AX
MOV [SI+2],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|       1200🔢       01         12

|         1200                    |

#### Manual Calculations
![WhatsApp Image 2026-02-09 at 8 46 00 AM](https://github.com/user-attachments/assets/e2721889-c0de-4192-bb75-063002427acb)

(Add your calculation here)

---

## OUTPUT IMAGE FROM MASM SOFTWARE
![WhatsApp Image 2026-02-07 at 9 34 46 AM](https://github.com/user-attachments/assets/15ec6fdc-c06c-4bc5-a346-18df90037c0b)

## 2. SUBTRACTION

#### Algorithm

1. Initialize memory and store 1st data.
2. Increment to get 2nd data.
3. Move 2nd data to accumulator.
4. Subtract memory content.
5. Store result.

## FLOWCHART

<img width="578" height="797" alt="image" src="https://github.com/user-attachments/assets/564c3c7a-33ce-4a1c-8920-beb5c24b9b47" />


#### Program
```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
SUB AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```


#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|                         |                          |

#### Manual Calculations
![WhatsApp Image 2026-02-09 at 8 46 24 AM](https://github.com/user-attachments/assets/b5a90e54-96e0-4f95-859c-814a1dd24e40)

(Add your calculation here)

---


## OUTPUT SCREEN FROM MASM SOFTWARE
![WhatsApp Image 2026-02-07 at 9 34 18 AM (1)](https://github.com/user-attachments/assets/6afab344-dc27-4309-bdf1-deb1cfe96a3a)

## 3. MULTIPLICATION

#### Algorithm

1. Initialize memory and store operands.
2. Move operands to registers.
3. Multiply.
4. Store result.

##FLOWCHART

<img width="569" height="906" alt="image" src="https://github.com/user-attachments/assets/88be88ff-2896-4a88-b73d-84ccffd2fcf9" />



#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
MUL BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|                         |                          |

#### Manual Calculations
![WhatsApp Image 2026-02-09 at 8 46 47 AM](https://github.com/user-attachments/assets/3c49b1f2-5d70-4182-9385-c10a034c032c)

(Add your calculation here)

---

## OUTPUT SCREEN FROM MASM SOFTWARE
![WhatsApp Image 2026-02-07 at 9 34 18 AM (2)](https://github.com/user-attachments/assets/0eb05bc8-596d-42a1-9d1e-7d1e0c52cb43)

## 4. DIVISION

#### Algorithm

1. Load memory location of operands.
2. Perform division.
3. Store result.

   ## FLOWCHART
<img width="1065" height="802" alt="image" src="https://github.com/user-attachments/assets/25b4a483-0d42-494b-8639-1af3ea17191b" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
DIV BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|                         |                          |

#### Manual Calculations
![WhatsApp Image 2026-02-09 at 8 47 15 AM](https://github.com/user-attachments/assets/9d019e91-e0e2-4f18-b7d8-2e5058f581c7)

(Add your calculation here)

---
## OUTPUT FROM MASM SOFTWARE
![WhatsApp Image 2026-02-07 at 9 34 18 AM](https://github.com/user-attachments/assets/db6a9c59-4523-46a9-a492-d4a8a05fd386)



## RESULT
![WhatsApp Image 2026-02-09 at 8 47 47 AM](https://github.com/user-attachments/assets/c4dc98e7-b701-4134-9c1b-58a8577b8a48)

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

