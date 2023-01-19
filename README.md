 AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

 Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

Figure -02 FULL ADDER 

Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
 
Program:

Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

HALF ADDER  

module HalfAdder(a,b,sum,carry);  

input a,b;

output sum,carry;

xor(sum,a,b);

and(carry,a,b);

endmodule  

FULL ADDER  

module FullAdder(a,b,c,sum,carry);

input a,b,c;

output sum,carry;

assign sum = ((a^b)^c);

assign carry = ((a&b)|(b&c)|(c&a));

endmodule


Developed by: S.P. HARZHITA
RegisterNumber:  22006162

LOGIC SYMBOL


![LOGIC SYMBOL](https://user-images.githubusercontent.com/123094490/213497549-429ab698-c55a-451b-93eb-13c9e76618e3.png)



RTL REALIZATION

OUTPUT

HALF ADDER

![SS 1](https://user-images.githubusercontent.com/123094490/213497986-60d373e7-c441-45a7-bb2f-30e8c37187b2.png)

FULL ADDER


![SR 2](https://user-images.githubusercontent.com/123094490/213498473-03590de6-bbb3-4cc7-b7e7-36f3c36f2a4a.png)


RTL TIMING DIAGRAM

HALF ADDER

![SR 3](https://user-images.githubusercontent.com/123094490/213498681-c8c682aa-faa0-4d2d-b277-dbcb1a6e101c.png)

FULL ADDER

![SR 4](https://user-images.githubusercontent.com/123094490/213498788-4e213a5f-a7d7-4581-a805-d8f58e3ca51f.png)

 TRUTH TABLE

HALF ADDER

![SR 5](https://user-images.githubusercontent.com/123094490/213498971-ef18f982-929d-4413-b761-2a834d9b0cd2.png)


FULL ADDER
![SR 6](https://user-images.githubusercontent.com/123094490/213499045-743bcc43-cfbc-4142-ae69-bc3ed539cd69.png)


Result:
Thus the Implementation of Halfadder Fulladder Circuit are studied and the truthtable for different logic gates are verified
