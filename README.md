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


full adder


![WhatsApp Image 2024-12-21 at 09 57 52_9f9bf009](https://github.com/user-attachments/assets/32d07900-7ea6-465c-85aa-765afd06e8e0)









full subtractor






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



```module fa(a,b,cin,sum,carry);

input a,b,cin;

output sum, carry;

assign sum=( (a ^ b)^cin);

assign carry= ( (a & b)| ( cin &(a ^ b )));

endmodule
```





```module fs(a,b,bin,difference,borrow);

input a,b, bin;

output difference, borrow;

assign difference= ( (a ^ b)^bin);

assign borrow= ((~a&b)|(bin&(~(a^b))));

endmodule
```








**RTL Schematic**



FULL ADDER



![Screenshot (55)](https://github.com/user-attachments/assets/bf6d695d-7a27-423e-9007-dd5d2b881db1)







FULL SUBTRACTOR







![Screenshot (75)](https://github.com/user-attachments/assets/0b348268-82e8-48e8-bd1e-59912be0da42)











**output**




FULL ADDER





![Screenshot (135)](https://github.com/user-attachments/assets/5053893b-a274-407d-af01-f82635224468)





FULL SUBTRACTOR







![Screenshot (136)](https://github.com/user-attachments/assets/6ad0536e-057c-47e4-bf2d-90b1307ef516)











**Result:**




Thus the Full Adder and Full Subtractor circuits are designed and the truth tables are verified using Quartus software.



