Developed by: ROHIT JAIN D  
Reference Number: 22005894  


## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
- Hardware 
  - PCs , Cyclone II , USB flasher.
- Software  
  - Quartus prime  
  
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.  

## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits.  
It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow).  
To perform x - y, we have to check the relative magnitudes of x and y.
If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit.  
If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage.  
The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit.  
With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated
by the symbol D.  
The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.  
Diff = X'Y+XY' = X ⊕ Y  
Borrow = X'Y  

![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.  
Diff = A ⊕ B ⊕ Bin  
Borrow = A'Bin + A'B + BBin  
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)  

## Procedure
Write the detailed procedure here 
## Program:
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
```
HALF SUBTRACTOR:

module HalfSub(a,b,difference,borrow);
input a,b;
output difference,borrow;
assign difference=(a^b);
assign borrow=(~a&b);
endmodule

FULL SUBTRACTOR:

module FullSub(a,b,c,difference,borrow);
input a,b,c;
output difference,borrow;
assign borrow=(~a&(b^c)|(b&c));
assign difference=(a^b^c);
endmodule
```
## LOGIC GATES:  
<img width="145" height="145" alt="and-gate" src="https://user-images.githubusercontent.com/118707073/210804152-d3067756-db97-49b6-81f9-859224ab815e.png">          <img width="145" height="145" alt="or-gate" src="https://user-images.githubusercontent.com/118707073/210804186-b2fd26ff-4908-4580-b064-b49bb33c4b6b.png">             <img width="145" height="145" alt="not-gate" src="https://user-images.githubusercontent.com/118707073/210804437-c8289936-6877-4420-ac8e-b6de9497de25.png">            <img width="145" height="145" alt="xor-gate" src="https://user-images.githubusercontent.com/118707073/210804204-908a6987-8a7f-449d-b33b-42b08166e0d9.png">




# Output:

## Truthtable
- ## HALF SUBTRACTOR:
![WhatsApp Image 2023-01-05 at 19 53 36](https://user-images.githubusercontent.com/118707073/210802334-f7ee77a0-38db-4917-986a-e0c154cd17a8.jpg)
- ## FULL SUBTRACTOR:
![full-subtractor-truth-table](https://user-images.githubusercontent.com/118707073/210806829-e8faa983-2648-444c-8290-2b1082744d52.jpg)

##  RTL realization:
- ## HALF SUBTRACTOR:
![Screenshot_20230104_012842](https://user-images.githubusercontent.com/118707073/210792084-25ab0017-b381-4eb3-9d99-fb6c6fd40c8d.png)


- ## FULL SUBTRACTOR:
![Screenshot_20230105_075116](https://user-images.githubusercontent.com/118707073/210801886-6f94f3e4-50a2-4074-942c-1635968be9ed.png)


## Timing diagram 
- ## HALF SUBTRACTOR:
![Screenshot_20230105_071424](https://user-images.githubusercontent.com/118707073/210794248-a1ec9343-5e1a-4f43-94f7-21aec0586c7c.png)
- ## FULL SUBTRACTOR:
![Screenshot_20230105_075054](https://user-images.githubusercontent.com/118707073/210802008-99d86d7b-c012-460e-8ef5-fbcbb8c5f60b.png)





## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
