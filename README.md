# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
1.Hardware – PCs, Cyclone II , USB flasher

2.Software – Quartus prime
### Theory:
Adders are digital circuits that carry out addition of numbers.

### Half Adder:
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB
#### Figure -01 HALF ADDER:
![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

### Full Adder:
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin
#### Figure -02 FULL ADDER:

![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

### Procedure:

1.Connect the supply (+5V) to the circuit

2.Switch ON the main switch

3.If the output is 1, then the led glows.
### Program:
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

Developed by: Tejaswini.G

RegisterNumber:  212222230157
### Half Adder:
```
module halfadd(A,B,C,S);
input A,B;
output S,C;
xor(S,A,B);
and(C,A,B);
endmodule
```
### Full Adder:
```
module fulladd(a,b,ci,s,co);
input a,b,ci;
output s,co;
wire d,e,f;
xor(d,a,b);
xor(s,d,ci);
and(e,ci,d);
and(f,a,b);
or(co,e,f);
endmodule
```
### Output:
### Logic symbol & Truthtable:
### Half adder:
![h l](https://user-images.githubusercontent.com/121222763/231431089-0c6a2805-9a1c-455e-bc5b-51be5443e79b.png)
![f t](https://user-images.githubusercontent.com/121222763/231431199-8294fd1b-7e9d-476d-9f8a-c80a77d7dc08.png)
### Full adder:
![f l](https://user-images.githubusercontent.com/121222763/231431265-0524ffce-37a9-4e07-a5ba-d951de1c21be.png)
![f 1 t](https://user-images.githubusercontent.com/121222763/231431296-4749519f-df54-4157-9935-fdb0548840d3.png)

### RTL realization:
### Half adder:
![half adder](https://user-images.githubusercontent.com/121222763/231431560-68fa604c-f960-4e2a-b7b4-713a8869d853.png)
### Full adder:
![full hader](https://user-images.githubusercontent.com/121222763/231431620-81f87715-4e28-4c5a-b859-87c182514d36.png)

### TIMING DIAGRAM:
### Half adder:
![hal wa](https://user-images.githubusercontent.com/121222763/231431948-516bc73f-4a38-4896-83ce-4dbddd79301d.png)
### Full adder:
![f w](https://user-images.githubusercontent.com/121222763/231432034-021a21d8-9d19-4cea-81d2-960d16064795.png)

### Result:
Thus the half adder and full adder are studied and the truth table for different logic gates are verified.
