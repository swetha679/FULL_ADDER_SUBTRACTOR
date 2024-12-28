# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II, USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

**Full Adder**

A full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)



**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in. It accepts three inputs: minuend, subtrahend, and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin




**Truthtable**




![WhatsApp Image 2024-12-21 at 09 57 52_9f9bf009](https://github.com/user-attachments/assets/32d07900-7ea6-465c-85aa-765afd06e8e0)








![WhatsApp Image 2024-12-21 at 09 58 11_1ce1389e](https://github.com/user-attachments/assets/cff18d1a-bad8-4caf-8df4-0b7cf0dbfbe6)








**Procedure**

1. Type the program in Quartus software.

2 . Compile and run the program.

3  . Generate the RTL schematic and save the logic diagram.

4. Create nodes for inputs and outputs to generate the timing diagram.

5 . For different input combinations generate the timing diagram.


**Program:**





developed by Swetha Nivasini B R 




registration number 24900367



module fa(a,b,cin,sum,carry);
input a,b,cin;

output sum, carry;

assign sum=( (a ^ b)^cin);

assign carry= ( (a & b)| ( cin &(a ^ b )));

endmodule





module fs(a,b,bin,difference,borrow);

input a,b, bin;

output difference, borrow;

assign difference= ( (a ^ b)^bin);

assign borrow= ((~a&b)|(bin&(~(a^b))));

endmodule



**RTL Schematic**






![image](https://github.com/user-attachments/assets/a604a058-38d8-4d16-935d-2d8bd2655eb3)










![image](https://github.com/user-attachments/assets/9d2bcb0e-7391-4f50-969b-867768bd9348)










**output**






![Screenshot (120)](https://github.com/user-attachments/assets/78a2b5c4-eb6e-4c6e-8205-248342b9531d)








![Screenshot (121)](https://github.com/user-attachments/assets/5be1c823-09be-4f8f-871b-c97f46710dac)










**Result:**




Thus the Full Adder and Full Subtractor circuits are designed and the truth tables are verified using Quartus software.



