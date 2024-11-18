# FULL_ADDER_SUBTRACTOR



 # AIM:  

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

 # Equipments Required:  

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

  # Full Adder and Full Subtractor  

 # Figure -1 FULL ADDER  

 # Full Adder  

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

#  Figure -2 FULL Subtractor  

 # Full Subtractor  

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin



 # Procedure  


#  Full Adder:  


1.Open Quartus II and create a new project.
2.Use schematic design entry to draw the full adder circuit. 
3.The circuit consists of XOR, AND, and OR gates. 
4.Compile the design, verify its functionality through simulation. 
5.Implement the design on the target device and program it.

 # Full Subtractor:   

1.Follow the same steps as for the full adder. 
2.Draw the full subtractor circuit using schematic design. 
3.The circuit includes XOR, AND, OR gates to perform subtraction. 
4.Compile, simulate, implement, and program the design similarly to the full adder.

 # Program:  

/  Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. /

  Implementation-of-Full-Adder-and-Full-subtractor-circuit  
``` 
Developed by: EZHIL SREE J
RegisterNumber: 212223230056
```

## Full_adder
```
module fulladd_top(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
wire w1,w2,w3,w4;       
xor(w1,a,b);
xor(sum,w1,cin);        
and(w2,a,b);
and(w3,b,cin);
and(w4,cin,a);
or(carry,w2,w3,w4);
endmodule 
```
## Full_subtractor
```
module fullsub_top(a,b,Bin,BO,DIFF);
input a,b,Bin;
output BO,DIFF;
assign DIFF = a ^ b ^ Bin;
assign BO = (a & b) | ((a ^ b) & Bin);
endmodule
```
 # Truthtable  

#  FULL ADDER:  

![DE E-4 truthtable](https://github.com/04Varsha/FULL_ADDER_SUBTRACTOR/assets/149035374/7116d2bf-8e90-4e96-bfd5-d62af11a317a)

#  FULL SUBTRACTOR:  

![image](https://github.com/user-attachments/assets/0782e03b-ce96-4cc0-b05a-b11c21e14969)

 # RTL Schematic  

 # FULL ADDER:  

![image](https://github.com/user-attachments/assets/d2735de8-e6e6-4ad5-a754-115f3aea7616)

#  FULL SUBTRACTOR:  

![image](https://github.com/user-attachments/assets/1a4cd9cf-8026-4f4a-b78a-2374be2ecdc0)


#  Output Timing Waveform  

# FULL ADDER:
![image](https://github.com/user-attachments/assets/12396e7b-7b47-4137-9aa7-b7d38e54fd7d)


#  FULL SUBTRACTOR  
![image](https://github.com/user-attachments/assets/9debf92f-c87f-45bc-b147-fccbf5c2b190)

#  Result:  

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



