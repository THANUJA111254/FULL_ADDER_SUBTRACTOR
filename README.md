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
![image](https://github.com/user-attachments/assets/a3edd586-3549-4a06-a5dd-f745cff78236)


**Program**
(i)FULL ADDER
```
module faexp(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^cin);
assign carry=( (a & b)| ( cin &(a ^  b)));
endmodule
```
(ii)FULL SUBTRACTER
```
module fsexp(a, b,bin,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b ))));
endmodule
```
Write the detailed procedure here

**Procedure**
### 1.Type the program
### 2.Compile and run the program
### 3.Generate the RTL schematic and save the logic diagram.
### 4.Create nodes for inputs and outputs to generate the timing diagram
### 5.For different input combinations generate the timing diagrams

developed by:PANGA THANUJA
REF NO:24900052

**RTL Schematic**
![image](https://github.com/user-attachments/assets/994eb087-198f-4e10-a6e1-abb328801afc)
![image](https://github.com/user-attachments/assets/b2c2b71e-b683-4bfc-9db0-d46bec9c4174)



**Output Timing Waveform**
![image](https://github.com/user-attachments/assets/9e2f5254-b9c8-454f-b84e-6c1fdba6b20e)
![image](https://github.com/user-attachments/assets/a73163a3-2af9-4eda-9af2-0abb36876124)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



