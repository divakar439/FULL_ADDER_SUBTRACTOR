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
![WhatsApp Image 2024-11-22 at 10 55 29_737ce5a2](https://github.com/user-attachments/assets/c949c57c-28b3-4016-9054-58f55d34d25e)

![WhatsApp Image 2024-11-22 at 10 55 30_a1ed486c](https://github.com/user-attachments/assets/d04dc5f5-ef6e-4358-8287-81866494c6ee)



**Procedure**
1. Type the program in Quartus software.
 2. Compile and run the program.
 3. Generate the RTL schematic and save the logic diagram.
4. Create nodes for inputs and outputs to generate the timing diagram.
 5. For different input combinations generate the timing diagram.

**Program:**
```
module EXP4 (df, bo, a, b, bin);
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
 assign bo=w2|w3;
 endmodule
```

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber: 24005335
*/

**RTL Schematic**
![Screenshot 2024-11-22 102132](https://github.com/user-attachments/assets/a0b6ad28-e81c-42cc-88ba-fc5a7093f589)


**Output Timing Waveform**

![Screenshot 2024-11-22 102554](https://github.com/user-attachments/assets/761b6a19-d30f-46fd-8e95-1f17dee44f0d)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



