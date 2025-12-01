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

**FULL ADDER:**

<img width="585" height="663" alt="fa" src="https://github.com/user-attachments/assets/4b05924f-e504-4c67-98e7-9c7daad805ff" />

**FULL SUBTRACTOR:**

<img width="768" height="705" alt="fs" src="https://github.com/user-attachments/assets/a13f4ff3-41d9-4c1b-a213-63dbda2b20f8" />

**Procedure**
```
**Full Adder:**
1.Open Quartus II and create a new project.
2.Use schematic design entry to draw the full adder circuit. 
3.The circuit consists of XOR, AND, and OR gates. 
4.Compile the design, verify its functionality through simulation. 
5.Implement the design on the target device and program it.

**Full Subtractor:** 
1.Follow the same steps as for the full adder. 
2.Draw the full subtractor circuit using schematic design. 
3.The circuit includes XOR, AND, OR gates to perform subtraction. 
4.Compile, simulate, implement, and program the design similarly to the full adder.
```
**Program:**
```
module F_A_F_S(
    input A, B, Cin,
    input Bin,
    output SUM, CARRY,
    output DIFF, BORROW
);
    assign SUM   = A ^ B ^ Cin;
    assign CARRY = (A & B) | (B & Cin) | (Cin & A);
    assign DIFF   = A ^ B ^ Bin;
    assign BORROW = (~A & B) | (Bin & ~(A ^ B));
endmodule
```
Developed by: THANGAPAZHAM P
RegisterNumber: 25017581

**RTL Schematic**

<img width="1035" height="687" alt="image" src="https://github.com/user-attachments/assets/dda913db-de11-48d7-b16f-fdf3b707f4ca" />

**Output Timing Waveform**

<img width="1920" height="1080" alt="Screenshot (147)" src="https://github.com/user-attachments/assets/d576bef4-a3f7-4fa4-9a96-a665dd00e7aa" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



