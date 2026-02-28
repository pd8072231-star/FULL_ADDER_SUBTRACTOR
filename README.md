# FULL_ADDER_SUBTRACTOR

DEVELOPED BY P.DHARSHINI.
REGISTER NUMBER:25010127.

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

<img width="861" height="501" alt="image" src="https://github.com/user-attachments/assets/63ad0767-1f95-42e0-b06c-67fc9ce501bb" />


**Procedure**

Write the detailed procedure here
1.Create a new project in Quartus II and open a Block Diagram/Schematic file.
2.Place logic symbols and connect inputs A, B, Cin and outputs Sum, Cout for full adder;inputs A,Bin and outputs diff ,borrow out for full subtractor.
3.Implement logic: Sum = A ⊕ B ⊕ Cin, Cout = AB + Cin(A ⊕ B); Diff = A ⊕ B ⊕ Bin ,Borrow out = A'Bin + A'B + BBin.
4.Compile and simulate to verify the output waveform.

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

Developed by:P.Dharshini
RegisterNumber:25010127

*/

FULL ADDER:
```
module exp_3a(A,B,C,sum,carry);
input A,B,C;
output sum,carry;
assign sum=A^B^C;
assign carry=((A&B)|(A&C)|(B&C));
endmodule
```
FULL SUBTRACTOR:
```
module exp_3b(A,B,C,dif,bor);
input A,B,C;
output dif,bor;
assign dif=A^B^C;
assign bor=(~A&C)|(~A&B)|(B&C);
endmodule
```

**RTL Schematic**
FULL ADDER:
<img width="1920" height="1080" alt="Screenshot (580)" src="https://github.com/user-attachments/assets/73601607-bd08-45f3-9ca9-e71aa3e8c8b4" />
FULL SUBTRACTOR:
<img width="1920" height="1080" alt="Screenshot (582)" src="https://github.com/user-attachments/assets/9d8585d0-9cfa-4654-bc24-cc81ceecff8a" />



**Output Timing Waveform**
FULL ADDER:
<img width="1920" height="1080" alt="Screenshot (581)" src="https://github.com/user-attachments/assets/4c8d001a-7067-4395-8986-576954309eaf" />
FULL SUBTRACTOR:
<img width="1920" height="1080" alt="Screenshot (583)" src="https://github.com/user-attachments/assets/9a1f5765-b5cc-4869-871c-4dbb5317ee6d" />



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



