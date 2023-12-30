## Name : Stephen raj.Y
## Register No: 212223230217
# Experiment--04-Half-Subtractor-and-Full-subtractor
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

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

## 1.Use module projname(input,output) to start the Verilog programming.
## 2.Assign inputs and outputs using the word input and output respectively.
## 3.Use defined keywords like wire,assign and required logic gates to represent the boolean expression.
## 4.Use each output to represent one for difference and the other for borrow.
## 5.End the verilog program using keyword endmodule


## Program:

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Program to design a half and full subtractor circuit and verify its truth table in quartus using Verilog programming.
```
module halfsub(a,b,difference,borrow);
input a,b;
output difference,borrow;
assign difference = (a^b);
assign borrow = (~a&b);
endmodule
module fullsub(a,b,c,difference,borrow);
input a,b,c;
output difference,borrow;
assign difference=(a^b^c);
assign borrow=(~a&(b^c)|(b&c));
endmodule
```

## Output:

## Truthtable:
## Half Subtractor:
![image](https://github.com/23002248/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/151701774/4dbce8bb-a15d-4dcd-9121-37ce896668fb)

## Full Subtractor :
![image](https://github.com/23002248/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/151701774/217a59f6-7297-400e-80bd-c9c8b64ceac8)

##  RTL realization
## Half Subtractor:
![image](https://github.com/23002248/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/151701774/785c2a47-cb19-467d-8752-a4272d24b11d)
## Full Subtractor :
![image](https://github.com/23002248/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/151701774/89be6df2-c069-4324-bda1-6be7351bcf20)

## Timing diagram :
## Half Subtractor:
![image](https://github.com/23002248/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/151701774/bebca649-14e3-4a89-bca7-373bd0f1fc71)
## Full Subtractor :
![image](https://github.com/23002248/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/151701774/ed718040-d22d-4542-828f-b5f84d9a0465)


## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
