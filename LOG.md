## ********************FAILED********************
### *****diff ./code/out/Ri/Ri.trace ./code/ref/Ri/Ri.trace*****
 ```73c73
< r 0=00000000 r 1=00000004 r 2=00000010 r 3=00003000 
---
> r 0=00000000 r 1=00000004 r 2=00000000 r 3=00003000 
82c82
< r 0=00000000 r 1=00000004 r 2=00000010 r 3=00003000 
---
> r 0=00000000 r 1=00000004 r 2=00000000 r 3=00003000 

```
### *****./riscv -d ./code/input/custom.input > ./code/out/custom.solution*****
 ```
```
### *****diff ./code/out/custom.solution ./code/ref/custom.solution*****
 ```4c4,9
< 0000100c: 
\ No newline at end of file
---
> 0000100c: mac	x12, x10, x11
> 00001010: addi	x11, x12, 0
> 00001014: addi	x10, x0, 1
> 00001018: ecall
> 0000101c: addi	x10, x0, 10
> 00001020: ecall

```
### *****timeout 60 ./riscv -r ./code/input/custom.input > ./code/out/custom.trace*****
 ```
```
### *****diff ./code/out/custom.trace ./code/ref/custom.trace*****
 ```27a28,73
> r 0=00000000 r 1=00000000 r 2=000effff r 3=00003000 
> r 4=00000000 r 5=00000000 r 6=00000000 r 7=00000000 
> r 8=00000000 r 9=00000000 r10=00000003 r11=00000005 
> r12=00000019 r13=00000000 r14=00000000 r15=00000000 
> r16=00000000 r17=00000000 r18=00000000 r19=00000000 
> r20=00000000 r21=00000000 r22=00000000 r23=00000000 
> r24=00000000 r25=00000000 r26=00000000 r27=00000000 
> r28=00000000 r29=00000000 r30=00000000 r31=00000000 
> 
> r 0=00000000 r 1=00000000 r 2=000effff r 3=00003000 
> r 4=00000000 r 5=00000000 r 6=00000000 r 7=00000000 
> r 8=00000000 r 9=00000000 r10=00000003 r11=00000019 
> r12=00000019 r13=00000000 r14=00000000 r15=00000000 
> r16=00000000 r17=00000000 r18=00000000 r19=00000000 
> r20=00000000 r21=00000000 r22=00000000 r23=00000000 
> r24=00000000 r25=00000000 r26=00000000 r27=00000000 
> r28=00000000 r29=00000000 r30=00000000 r31=00000000 
> 
> r 0=00000000 r 1=00000000 r 2=000effff r 3=00003000 
> r 4=00000000 r 5=00000000 r 6=00000000 r 7=00000000 
> r 8=00000000 r 9=00000000 r10=00000001 r11=00000019 
> r12=00000019 r13=00000000 r14=00000000 r15=00000000 
> r16=00000000 r17=00000000 r18=00000000 r19=00000000 
> r20=00000000 r21=00000000 r22=00000000 r23=00000000 
> r24=00000000 r25=00000000 r26=00000000 r27=00000000 
> r28=00000000 r29=00000000 r30=00000000 r31=00000000 
> 
> 25r 0=00000000 r 1=00000000 r 2=000effff r 3=00003000 
> r 4=00000000 r 5=00000000 r 6=00000000 r 7=00000000 
> r 8=00000000 r 9=00000000 r10=00000001 r11=00000019 
> r12=00000019 r13=00000000 r14=00000000 r15=00000000 
> r16=00000000 r17=00000000 r18=00000000 r19=00000000 
> r20=00000000 r21=00000000 r22=00000000 r23=00000000 
> r24=00000000 r25=00000000 r26=00000000 r27=00000000 
> r28=00000000 r29=00000000 r30=00000000 r31=00000000 
> 
> r 0=00000000 r 1=00000000 r 2=000effff r 3=00003000 
> r 4=00000000 r 5=00000000 r 6=00000000 r 7=00000000 
> r 8=00000000 r 9=00000000 r10=0000000a r11=00000019 
> r12=00000019 r13=00000000 r14=00000000 r15=00000000 
> r16=00000000 r17=00000000 r18=00000000 r19=00000000 
> r20=00000000 r21=00000000 r22=00000000 r23=00000000 
> r24=00000000 r25=00000000 r26=00000000 r27=00000000 
> r28=00000000 r29=00000000 r30=00000000 r31=00000000 
> 
> exiting the simulator

```
### *****timeout 60 ./riscv -r -e ./code/input/multiply.input > ./code/out/multiply.trace*****
 ```
```
### *****python3 part2_tester.py multiply*****
 ```
Starting multiply test
ERROR: instruction 6, register 18. Expected: 0x0000001b, Actual: 0x00000000
ERROR: instruction 7, register 8. Expected: 0x0000000d, Actual: 0x0000000e
ERROR: instruction 10, register 18. Expected: 0x00000036, Actual: 0x00000000
ERROR: instruction 11, register 8. Expected: 0x0000000c, Actual: 0x0000000e
ERROR: instruction 14, register 18. Expected: 0x00000051, Actual: 0x00000000
ERROR: instruction 15, register 8. Expected: 0x0000000b, Actual: 0x0000000e
ERROR: instruction 18, register 18. Expected: 0x0000006c, Actual: 0x00000000
ERROR: instruction 19, register 8. Expected: 0x0000000a, Actual: 0x0000000e
ERROR: instruction 22, register 18. Expected: 0x00000087, Actual: 0x00000000
ERROR: instruction 23, register 8. Expected: 0x00000009, Actual: 0x0000000e
ERROR: instruction 26, register 18. Expected: 0x000000a2, Actual: 0x00000000
ERROR: instruction 27, register 8. Expected: 0x00000008, Actual: 0x0000000e
ERROR: instruction 30, register 18. Expected: 0x000000bd, Actual: 0x00000000
ERROR: instruction 31, register 8. Expected: 0x00000007, Actual: 0x0000000e
ERROR: instruction 34, register 18. Expected: 0x000000d8, Actual: 0x00000000
ERROR: instruction 35, register 8. Expected: 0x00000006, Actual: 0x0000000e
ERROR: instruction 38, register 18. Expected: 0x000000f3, Actual: 0x00000000
ERROR: instruction 39, register 8. Expected: 0x00000005, Actual: 0x0000000e
ERROR: instruction 42, register 18. Expected: 0x0000010e, Actual: 0x00000000
ERROR: instruction 43, register 8. Expected: 0x00000004, Actual: 0x0000000e
ERROR: instruction 46, register 18. Expected: 0x00000129, Actual: 0x00000000
ERROR: instruction 47, register 8. Expected: 0x00000003, Actual: 0x0000000e
ERROR: instruction 50, register 18. Expected: 0x00000144, Actual: 0x00000000
ERROR: instruction 51, register 8. Expected: 0x00000002, Actual: 0x0000000e
ERROR: instruction 54, register 18. Expected: 0x0000015f, Actual: 0x00000000
ERROR: instruction 55, register 8. Expected: 0x00000001, Actual: 0x0000000e
ERROR: instruction 58, register 18. Expected: 0x0000017a, Actual: 0x00000000
ERROR: instruction 59, register 8. Expected: 0x00000000, Actual: 0x0000000e
ERROR: instruction 62, register 19. Expected: 0x00000001, Actual: 0x00000000
ERROR: instruction 63, register 2. Expected: 0x000efffb, Actual: 0x000effff
ERROR: instruction 67, register 19. Expected: 0x00000001, Actual: 0x00000000
ERROR: instruction 69, register 10. Expected: 0x00000001, Actual: 0x00000000
ERROR: instruction 71, register 11. Expected: 0x0000017a, Actual: 0x00000000
ERROR: instruction 74, register 10. Expected: 0x0000000a, Actual: 0x00000000
ERROR: reference trace finished before student trace
multiply test has failed.

```
### *****python3 part2_tester.py random*****
 ```
Starting random test
ERROR: instruction 6, register 8. Expected: 0xffffffff, Actual: 0x000000ff
ERROR: instruction 7, register 9. Expected: 0xfffff7ff, Actual: 0x0000f7ff
random test has failed.

```

****************************************
## ********************SUCCESS********************
### *****./riscv -d ./code/input/R/R.input > ./code/out/R/R.solution*****
 ```
```
### *****diff ./code/out/R/R.solution ./code/ref/R/R.solution*****
 ```
```
### *****timeout 60 ./riscv -r ./code/input/R/R.input > ./code/out/R/R.trace*****
 ```
```
### *****diff ./code/out/R/R.trace ./code/ref/R/R.trace*****
 ```
```
### *****./riscv -d ./code/input/Ri/Ri.input > ./code/out/Ri/Ri.solution*****
 ```
```
### *****diff ./code/out/Ri/Ri.solution ./code/ref/Ri/Ri.solution*****
 ```
```
### *****timeout 60 ./riscv -r -v ./code/input/Ri/Ri.input > ./code/out/Ri/Ri.trace*****
 ```
```
### *****./riscv -d ./code/input/I/I.input > ./code/out/I/I.solution*****
 ```
```
### *****diff ./code/out/I/I.solution ./code/ref/I/I.solution*****
 ```
```
### *****./riscv -d ./code/input/I/L.input > ./code/out/I/L.solution*****
 ```
```
### *****diff ./code/out/I/L.solution ./code/ref/I/L.solution*****
 ```
```
### *****timeout 60 ./riscv -r ./code/input/I/I.input > ./code/out/I/I.trace*****
 ```
```
### *****diff ./code/out/I/I.trace ./code/ref/I/I.trace*****
 ```
```
### *****timeout 60 ./riscv -r ./code/input/I/L.input > ./code/out/I/L.trace*****
 ```
```
### *****diff ./code/out/I/L.trace ./code/ref/I/L.trace*****
 ```
```
### *****./riscv -d ./code/input/S/S.input > ./code/out/S/S.solution*****
 ```
```
### *****diff ./code/out/S/S.solution ./code/ref/S/S.solution*****
 ```
```
### *****timeout 60 ./riscv -r ./code/input/S/S.input > ./code/out/S/S.trace*****
 ```
```
### *****diff ./code/out/S/S.trace ./code/ref/S/S.trace*****
 ```
```
### *****./riscv -d ./code/input/SB/SB.input > ./code/out/SB/SB.solution*****
 ```
```
### *****diff ./code/out/SB/SB.solution ./code/ref/SB/SB.solution*****
 ```
```
### *****timeout 60 ./riscv -r ./code/input/SB/SB.input > ./code/out/SB/SB.trace*****
 ```
```
### *****diff ./code/out/SB/SB.trace ./code/ref/SB/SB.trace*****
 ```
```
### *****./riscv -d ./code/input/U/U.input > ./code/out/U/U.solution*****
 ```
```
### *****diff ./code/out/U/U.solution ./code/ref/U/U.solution*****
 ```
```
### *****timeout 60 ./riscv -r ./code/input/U/U.input > ./code/out/U/U.trace*****
 ```
```
### *****diff ./code/out/U/U.trace ./code/ref/U/U.trace*****
 ```
```
### *****./riscv -d ./code/input/UJ/UJ.input > ./code/out/UJ/UJ.solution*****
 ```
```
### *****diff ./code/out/UJ/UJ.solution ./code/ref/UJ/UJ.solution*****
 ```
```
### *****timeout 60 ./riscv -r ./code/input/UJ/UJ.input > ./code/out/UJ/UJ.trace*****
 ```
```
### *****diff ./code/out/UJ/UJ.trace ./code/ref/UJ/UJ.trace*****
 ```
```
### *****./riscv -d ./code/input/simple.input > ./code/out/simple.solution*****
 ```
```
### *****diff ./code/out/simple.solution ./code/ref/simple.solution*****
 ```
```
### *****./riscv -d ./code/input/multiply.input > ./code/out/multiply.solution*****
 ```
```
### *****diff ./code/out/multiply.solution ./code/ref/multiply.solution*****
 ```
```
### *****./riscv -d ./code/input/random.input > ./code/out/random.solution*****
 ```
```
### *****diff ./code/out/random.solution ./code/ref/random.solution*****
 ```
```
### *****timeout 60 ./riscv -r -e ./code/input/simple.input > ./code/out/simple.trace*****
 ```
```
### *****python3 part2_tester.py simple*****
 ```
Starting simple test
simple test has passed.

```
### *****timeout 60 ./riscv -r -e ./code/input/random.input > ./code/out/random.trace*****
 ```
```
