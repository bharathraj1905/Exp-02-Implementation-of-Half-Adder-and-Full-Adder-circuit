# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER 

### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
### 
Program:
```
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: b.barathraj
RegisterNumber:  212222230019

module ha(x,y,s,c);
input x,y;
output s,c;
xor(s,x,y);
and(c,x,y);
endmodule

module full_adder(x, y, z, s, c, x1, x2, x3);
input x,  y,z;
output s ,c, x1, x2, x3;
xor(x1, x, y);
xor(s, x1, z);
and(x2, x, y);
and(x3, x1, z);
or(c, x2, x3);
endmodule
   
```

### Output:
### RTL
![rtl ex3](https://user-images.githubusercontent.com/121490575/233250990-c1003098-7c51-4368-99e0-f9aac7cd3287.png)

![rtl ex3 2](https://user-images.githubusercontent.com/121490575/233251027-397dfd2f-19b9-4882-8507-87401e2cab06.png)

### TIMING DIAGRAM
![timing ex3 1](https://user-images.githubusercontent.com/121490575/233251085-a4f63937-81f5-4f13-ac4f-90e4748f08d7.png)

![timing ex3 2](https://user-images.githubusercontent.com/121490575/233251144-e6427271-374c-4206-8b9c-bf57e5151496.png)

### TRUTH TABLE 

![truth table 3 1](https://user-images.githubusercontent.com/121490575/233251398-244f0fc4-96e7-43fa-9f94-368f233cd1b7.png)

![truth table ex 3 2](https://user-images.githubusercontent.com/121490575/233251519-2fb55cec-ea08-458f-972f-c50a20d087e9.png)

### Result:
Therefore,half adder and full adder is verified
