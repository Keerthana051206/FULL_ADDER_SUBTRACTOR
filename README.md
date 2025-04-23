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

<img width="224" alt="image" src="https://github.com/user-attachments/assets/0c452f6b-3351-4a95-a859-373423c6d16c" />


**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

<img width="257" alt="image" src="https://github.com/user-attachments/assets/c7c47669-ab11-49e4-82af-b52c772d3b52" />


Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**
FULL ADDER:
![Screenshot 2025-04-23 221041](https://github.com/user-attachments/assets/54da22bc-d51c-416b-9c10-32922eb16a14)

FULL SUBTRACTOR:
<img width="245" alt="image" src="https://github.com/user-attachments/assets/7d78999d-621e-4dfd-b96c-8ebe8bf8721b" />


**Procedure**
Full Adder:
1.Open Quartus II and create a new project.
2.Use schematic design entry to draw the full adder circuit.
3.The circuit consists of XOR, AND, and OR gates.
4.Compile the design, verify its functionality through simulation.
5.Implement the design on the target device and program it.
Full Subtractor:
1.Follow the same steps as for the full adder.
2.Draw the full subtractor circuit using schematic design.
3.The circuit includes XOR, AND, OR gates to perform subtraction.
4.Compile, simulate, implement, and program the design similarly to the full adder

Write the detailed procedure here

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: Keerthana C
RegisterNumber: 212224220047
*/

module fulladd_top(a,b,c,sum,carry,BO,DIFF);
input a,b,c;
output sum,carry,BO,DIFF;
assign sum=a^b^c;
assign carry= a&b | a&c | b&c;
wire a0;
not (a0,a);
assign BO= b&c | a0&c | a0&b;
assign DIFF=a^b^c;
endmodule

**RTL Schematic**
<img width="341" alt="image" src="https://github.com/user-attachments/assets/36bebb7c-8f39-4df9-8a4f-a63ef418030e" />

**Output Timing Waveform**
![Screenshot 2025-04-23 220322](https://github.com/user-attachments/assets/9b88a59e-2272-4193-a65d-9c8780fc3d17)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



