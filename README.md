# High-Performance-Computer-Architecture

There are two types of Instruction Available in this program

1. Assume a simplified MIPS processor with the following floating point instructions:

```
1. add.d FRdest, FRsrc1, FRsrc2      ;Floating Point Addition Double
2. add.s FRdest, FRsrc1, FRsrc2      ;Floating Point Addition Single
3. l.d   FRdest, address             ;Load Floating Point Double
4. l.s   FRdest, address             ;Load Floating Point Single
5. s.d   FRsrc, address              ;Store Floating Point Double
6. s.s   FRsrc, address              ;Store Floating Point Single
```

2. Assume the following integer instructions are available:

```
1. add.uIRdest, IRsrc1, IRsrc2        ;Integer Addition (32-bits)
2. add.iIRdest, IRsrc1, Immediate     ;Integer Addition with Immediate (16-bits)
3. sub.uIRdest, IRsrc1, IRsrc2        ;Integer Subtraction(32-bits)
4. sub.iIRdest, IRsrc1, Immediate     ;Integer Subtractionwith Immediate (16-bits)
5. bne          IRsrc1, IRsrc2,Loop   ;branch to Loop if IRsrc1!=IRsrc2
6. beqzIRsrc1,  Loop                  ;branch to Loop if IRsrc1=0
7. lwIRdest,    address               ;Load Integer Word
8. swIRsrc,     address               ;StoreInteger Word
9. mv           IRdest, IRsrc         ;Integer data movement
10. or          IRdest, IRsrc1, IRsrc2;Integer OR operation(32-bits)
```
# Testing Instruction
The below instruction is the testing instruction on which we perform the operations Unschedule strategy, Scheduled strategy, Loop unrolling and Unscheduled, Loop Unrolling and Scheduled.
```
L.D F0,0(R1)
ADD.D F4,F0,F2
S.D F4,0(R1)
L.D F0,0(R1)
L.D F4,0(R3)
ADD.D F6,F4,F0
S.D F6,0(R1)
ADD.I R1,R1,#-8
ADD.I R3,R3,#-8
BNE R1,R2,Loop
```
# Section 1
The function that takes an assembly code (input.txt) written using the 
above instructions. 
It prints the data dependencies present in the input code and create a new file.

# Section 2
This function that takes an assembly code (input.txt) written using the 
above instructions. It can produce assembly code (output.txt).
This considers all the data dependencies that we found above.
1. Unscheduled strategy 
2. Scheduled strategy 
3. Loop Unrolling and Unscheduled 
4. Loop Unrolling and Scheduled. 
