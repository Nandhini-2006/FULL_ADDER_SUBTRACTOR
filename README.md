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
full adder
![Screenshot 2024-12-26 200959](https://github.com/user-attachments/assets/d26344ea-1d0c-4ffd-a9b0-067c2a04b43a)
full subractor
![Screenshot 2024-12-26 201056](https://github.com/user-attachments/assets/8faa7ef1-7a48-4331-87d5-60e9637119f7)

**Procedure**

Write the detailed procedure here

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:
*/
 module exp4(a,b,c,sum,carry);
 input a,b,c;
 output sum,carry;
 xor(sum,a,b,c);
 assign carry=a&b | b&c | a&c;
 endmodule

module exp4(diff,carry,a,b,c);
input a,b,c;
output diff,carry;
xor(diff,a,b,c);
assign carry= (~a)&c | (~a)&b | (b&c);
endmodule

**RTL Schematic**
![Screenshot 2024-12-26 200033](https://github.com/user-attachments/assets/bb3623fd-aaad-431e-a51d-c62bf80f05a7)

![Screenshot 2024-12-26 200810](https://github.com/user-attachments/assets/302e6d10-9ae3-4ec5-a91c-da8c6482a929)

**Output Timing Waveform**
![Screenshot 2024-12-26 200504](https://github.com/user-attachments/assets/a4f8494c-3a7c-476a-b0db-be07d78be63d)
![Screenshot 2024-12-26 200906](https://github.com/user-attachments/assets/e0754809-88ed-49c4-afe6-ef4030e105cb)

**Result:**
NANDHINI N 24002003
Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



