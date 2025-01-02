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

**FULL ADDER**
![Screenshot 2025-01-02 220018](https://github.com/user-attachments/assets/fbbf9ae2-fccc-4eee-bf57-478698433585)

**FULL SUBSTRACTOR**
![Screenshot 2025-01-02 220133](https://github.com/user-attachments/assets/81b3cb7b-5cba-4493-b792-d075ef443323)

**Procedure**
write the detailed procedure here

1 type the program in quartes software.

2 compile and run rhe program .

3 generate the RTL schematic and save the logic diagram.

4 create nodes for inputs and outputs to generate the timing diagram .

5 for different input combinations generate the timing diagram

Program:

**FULL ADDER**

module fulladder(

input a,b,c,

output sum,carry);

wire w1,w2,w3;

assign sum=a^b^c; assign w1=a&b;

assign w2=b&c;

assign w3=c&a;

assign carry=w1|w2|w3;

endmodule

**FULL SUBRACTOR**

module fullsub(a,b,c,diff,borr);

input a,b,c;

output diff,borr;

wire w1,w2,w3,w4,w5,w6;

xor g1(diff,a,b,c);

and g2(w4,w1,b);

and g3(w5,w1,b);

nd g4(w6,b,c);

or g5(borr,w4,w5,w6);

endmodule

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by:D.Raju RegisterNumber:24003778
*/

**RTL Schematic**

**FULL ADDER**
![Screenshot 2025-01-02 214855](https://github.com/user-attachments/assets/99197db9-69e5-4cb7-a0d9-eb602ba01c51)

**FULL SUBSTRACTOR**

![Screenshot 2025-01-02 214912](https://github.com/user-attachments/assets/922338ef-231f-4a7b-8462-27cfde372e61)

**Output Timing Waveform**

**FULL ADDER**
![Screenshot 2025-01-02 214941](https://github.com/user-attachments/assets/868d791d-90ae-4427-911a-38ca58f594c5)

**FULL SUBSTRACTOR**

![Screenshot 2025-01-02 214958](https://github.com/user-attachments/assets/025d3312-e6bb-4e83-86cd-01556a2248dc)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



