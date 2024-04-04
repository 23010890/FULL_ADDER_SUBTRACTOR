# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**
![full adder](https://github.com/23010890/FULL_ADDER_SUBTRACTOR/assets/154983666/58db3be7-8a17-468c-aa8e-c62a47d565f9)
![full subtractor truth table](https://github.com/23010890/FULL_ADDER_SUBTRACTOR/assets/154983666/5dc72b12-1405-4a45-b2b7-e792aa05d3b6)



**Procedure**
```
1.Use module projname(input,output) to start the Verilog programming.
 2.Assign inputs and outputs using the word input and output respectively.
 3.Use defined keywords like wire,assign and required logic gates to represent the boolean expression.
 4.Use each output to represent one for difference and the other for borrow. 5.End the verilog program using keyword endmodule
```
**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: DHARSHINI S
RegisterNumber:212223110010
*/
```
module fulladd(df, bo, a, b, bin);

output df;
output bo;
input a;
input b;
input bin;
      wire w1,w2,w3;
      assign w1=a^b;
      assign w2=(~a&b);
      assign w3=(~w1&bin);
      assign df=w1^bin;
      assign bo=w2/w3;
endmodule/*

/* module fullsub(diff, bout, a, b, bin);
output diff,bout;
input a,b,bin;
// Internal nets
wire dl, bl, b2;
// Instantiate logic gate primitives
xor (d1, a, b);
and (b1, ~a, b);
xor (diff, d1, bin);
and (b2, ~dl, bin);
or (bout, b2, b1);
endmodule */
```
**RTL Schematic**
![full adder circuit](https://github.com/23010890/FULL_ADDER_SUBTRACTOR/assets/154983666/e9449b8f-7071-4191-913d-c896e575df7b)
![full subtractor circuit](https://github.com/23010890/FULL_ADDER_SUBTRACTOR/assets/154983666/d0cdf0ec-4278-45f8-b324-e6e6fa778486)

**Output Timing Waveform**
![full adder timing](https://github.com/23010890/FULL_ADDER_SUBTRACTOR/assets/154983666/ad30406a-4925-47ae-a481-e6236525629f)
![full subtractor timing](https://github.com/23010890/FULL_ADDER_SUBTRACTOR/assets/154983666/ef5c8d54-14fe-4051-b09a-ac40c0403a61)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



