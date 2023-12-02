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

Connect the supply (+5V) to the circuit.

Switch ON the main switch.

If the output is 1, then the led glows.

### Program:
/*
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

Developed by:  ANU RADHA .N

RegisterNumber:  23000217
*/

### HALF ADDER :
```
module halfadder (A,B,sum, carry );
input A,B;
output sum , carry;
xor(sum , A,B);
and (carry , A,B);
endmodule
```

### FULL ADDER :

```
module fulladder (a,b,c,sum,carry);
input a,b,c;
output sum ,carry ;
assign sum = ((a^b)^c);
assign carry = ((a&b)| (b&c)| (c&a));
endmodule
```

### Logic symbol & Truthtable : 

### HALF ADDER :

![Screenshot 2023-12-02 192630](https://github.com/ANU23000217/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/139117108/f13a5f8f-f684-4874-8f95-318b4757866d)


### FULL ADDER :
![Screenshot 2023-12-02 192643](https://github.com/ANU23000217/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/139117108/fd94c331-1953-4444-818a-290e96cbfca4)


   ### RTL realization :

### HALF ADDER :

![WhatsApp Image 2023-12-01 at 21 55 33_765f2d19](https://github.com/ANU23000217/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/139117108/bfea5564-8af3-4f87-8642-23ee76c2e41e)

### FULL ADDER :

![WhatsApp Image 2023-12-02 at 10 24 45_28595dce](https://github.com/ANU23000217/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/139117108/94ee18e9-d75e-4ea7-844e-c1ab5a3c3699)

### TIMING DIAGRAM :



### HALF ADDER :
![Screenshot 2023-12-02 191650](https://github.com/ANU23000217/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/139117108/c69bbb4d-ed49-4d4a-bb5c-b0456da4a9e0)

### FULL ADDER :
![Screenshot 2023-12-02 192519](https://github.com/ANU23000217/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/139117108/b5271747-ce2b-4e31-9cdb-53497bdcb152)



### Result:

Thus the Implementation of Half Adder and Full Adder circuit are studied and the truth
table for different logic gates are verified.
