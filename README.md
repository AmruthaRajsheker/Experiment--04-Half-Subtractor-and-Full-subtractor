# Experiment--04-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
 Hardware – PCs, Cyclone II , USB flasher
 Software – Quartus prime
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor Full Subtractor
## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Procedure
1.Use module projname(input,output) to start the Verilog programmming.

2.Assign inputs and outputs using the word input and output respectively.

3.Use defined keywords like wire,assign and required logic gates to represent the boolean expression.

4.Use each output to represent one for difference and the other for borrow.

5.End the verilog program using keyword endmodule.

## Program:
```
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: AMRUTHA RAJSHEKER
RegisterNumber:  212222110003

Half Subtractor Program:

module HalfSubtractor(A,B,Difference,Borrow);
input A,B;
output Difference,Borrow;
assign Difference = (A ^ B);
assign Borrow = (~A & B);
endmodule

Full Subtractor Program:

## Output:
module FullSubtractor(A,B,C,Difference,Borrow);
input A,B,C;
output Difference,Borrow;
assign Difference = (~A &(B ^ C) | (B & C));
assign Borrow = ( A^B^C);
endmodule

```
## Output:


## Truthtable
![image](https://user-images.githubusercontent.com/119475943/232224571-91414480-368c-461d-8ff4-3e375ead4735.png)

##  RTL realization
HALF SUBTRACTOR
![image](https://user-images.githubusercontent.com/119475943/232224776-dba41032-d946-475c-a1c9-36c19e516085.png)

FULL SUBTRACTOR
![image](https://user-images.githubusercontent.com/119475943/232224785-057ad4d4-81cb-4833-b82b-9cdf97724f04.png)


## Timing diagram 
Half Subtractor: 

![image](https://user-images.githubusercontent.com/119475943/232224810-a377383a-0ebe-4caa-8f3f-ff120c05e090.png)

Full Subtractor: 
![image](https://user-images.githubusercontent.com/119475943/232224816-63420229-ec19-4bc0-9a22-9a4482c579b7.png)

## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
