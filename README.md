## Name: Nithilan S

## RegisterNumber: 23013463

# Exp-03 Implementation of Half Adder and Full Adder circuit

# Implementation of Half Adder and Full Adder circuit
## Aim:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
```
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
```
### Theory:
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

## Procedure
Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
## Program:
### Half Adder:
```
module halfadder (A, B, sum, carry);
input A, B;
output sum, carry;
xor (sum, A, B);
and (carry,A,B);
endmodule
```
### Full Adder:
```
module fulladder(A,B,C,sum,carry);
input A,B,C;
output sum,carry;
assign sum = ((A^B)^C)
assign carry = ((A&b)|(A&C)|(B&C));
endmodule
```
##  RTL realization:
### Half Adder:
![DE Experiment 3(ha) RTL output](https://github.com/nithilans060306/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147473026/6befc26f-5773-4a10-bfff-5c93e3ccb26d)
### Full Adder:
![DE Experiment 3(fa) RTL output](https://github.com/nithilans060306/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147473026/1713a4b2-d8e7-4f0f-b827-a0cbf7da26a3)
## Truthtable:
### Half Adder:
![DE Experiment 3(ha) Truth table](https://github.com/nithilans060306/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147473026/27844912-a622-4580-8f6d-d8b0ff12da61)
### Full Adder:
![DE Experiment 3(fa) Truth table](https://github.com/nithilans060306/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147473026/d086b31b-8129-48cb-a1c5-7faaa221ac07)
## Timing diagram:
### Half Adder:
![DE Experiment 3(ha) Waveform output](https://github.com/nithilans060306/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147473026/44638947-4f52-42e5-b737-bb081a01dd5a)
### Full Adder:
![DE Experiment 3(fa) Waveform output](https://github.com/nithilans060306/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147473026/9e82d07a-a613-461c-9045-7c81c0e3ac15)
### Result:
Thus a Half Adder and Full Adder is designed and its truthtables are verified in Quartus using
Verilog programming.
