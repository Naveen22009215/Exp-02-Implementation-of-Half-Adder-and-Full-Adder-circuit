# Exp-03-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER 

### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
### Program:
```
/*
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: P NAVEEN KUMAR
RegisterNumber:  212222230092
*/
```
### HALF ADDER:
```
module halfadd(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule
```
### FULL ADDER:
```
module fulladder(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum = ((a^b)^c);
assign carry = ((a&b)|(b&c)|(c&a));
endmodule
```


### Output:
### RTL:
## HALF ADDER:
![half adder](https://user-images.githubusercontent.com/119401470/230388010-5d6be371-cd20-400a-ba11-285f5ad27197.png)
## FULL ADDER:
![full adder](https://user-images.githubusercontent.com/119401470/230388104-e5cb6ad8-37f0-43f9-9ae1-8fd5ff8216dc.png)

### TIMING DIAGRAM:

## HALF ADDER:
![wave half](https://user-images.githubusercontent.com/119401470/230388215-8e10fb12-258e-459b-9355-164b394243cb.png)

## FULL ADDER:
![wave full](https://user-images.githubusercontent.com/119401470/230388329-f663c7d5-8a77-4491-b251-8932dc776396.png)



### TRUTH TABLE:
## HALF ADDER:
![image](https://user-images.githubusercontent.com/119401470/230388438-33f0f6df-4771-4385-af4c-ff693f767941.png)
 ## FULL ADDER:

![WhatsApp Image 2023-04-13 at 11 51 27](https://user-images.githubusercontent.com/119401470/231671910-9602cbd0-07a0-4a76-b0ae-ff65c32c125c.jpg)


### Result:
Thus, a half adder and full adder circuit is designed to verify its truth table in Quartus using Verilog programming.

