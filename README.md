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

### Procedure:

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.

### Program:

```
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by:  M.A.Vishal
RegisterNumber:212222230177
```

half adder:
```
module halfadder(a,b,s,c);
input a,b;
output s,c;
xor (s,a,b);
and (c,a,b);
endmodule
```

full adder:
```
module fulladder(a,b,ci,s,co);
input a,b,ci;
output s,co;
wire d,e,f;
xor (d,a,b);
xor (s,d,ci);
and (f,a,b);
or (co,e,f);
endmodule
```
Logic symbol & Truthtable:
### Output:
### RTL:
half adder:

![half adder](https://user-images.githubusercontent.com/118707079/230267534-15bb609f-e040-4342-859d-72dbf4e7beab.png)

full adder:

![full adder](https://user-images.githubusercontent.com/118707079/230267605-2bacd3c2-06f1-49e6-b54c-62b1ea05394c.png)

### TIMING DIAGRAM:
half adder:

![half](https://user-images.githubusercontent.com/118707079/230267692-c39c206d-aab2-4d49-8434-064d36356d4a.png)

full adder:

![full](https://user-images.githubusercontent.com/118707079/230267739-e1b8fdbf-e40a-47aa-9008-09189a2b5c50.png)

### TRUTH TABLE:
half adder:

![addhalf](https://user-images.githubusercontent.com/118707079/230267837-99507134-60e2-4f84-8848-c1c6a9f203f0.png)

full adder:

![addfull](https://user-images.githubusercontent.com/118707079/230267905-e7f2352f-78f3-491c-9de5-34cedad14519.png)

### Result:

Thus the Implementation of Half Adder and Full Adder circuit are studied and the truth table for different logic gates are verified.

