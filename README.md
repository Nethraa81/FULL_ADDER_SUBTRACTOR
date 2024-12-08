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

![de tt 4](https://github.com/user-attachments/assets/31266a3c-a5d9-44b1-9415-f2ace12734bc)

![DE tt 4 1](https://github.com/user-attachments/assets/0f16021c-9d37-418c-8f90-a32eaf38cdec)

**Procedure**

1.Type the program in Quartus software.
   
2.Compile and run th image.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram.


**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 

Developed by:Nethraa N

RegisterNumber:24900193
*/

```
//full adder

module ex04(sum, cout, a, b, cin);

output sum;

output cout;

input a;

input b;

input cin;

//internal nets

wire sl,cl,c2;

//Instantiate logic gate primitives xor (sl,a,b);

and(cl,a,b);

xor (sum, sl, cin);

and(c2, sl, cin);

or(cout, c2,cl);

endmodule

Full subractor

module ex04a (df, bo, a, b, bin);

output df;

output bo;

input a;

input b;

input bin;

wire w1,w2, w3;

assign w1=a^b;

assign w2=(~a&b);

assign w3=(-w1&bin);

assign df-w1^bin;

assign bo-w2/w3;

endmodule
```
**RTL Schematic**

![Screenshot 2024-12-08 182641](https://github.com/user-attachments/assets/cf201a56-bb63-47db-8900-c846a933776b)

![Screenshot 2024-12-08 182656](https://github.com/user-attachments/assets/4c86eb76-2569-4219-9c14-1a4de9206bb4)

**Output Timing Waveform**

![Screenshot 2024-12-08 182836](https://github.com/user-attachments/assets/0cdb9c8a-7100-4326-be92-d45986e96ffe)

![Screenshot 2024-12-08 182855](https://github.com/user-attachments/assets/50373acb-2cc7-447b-bbee-c0d76eb382d5)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



