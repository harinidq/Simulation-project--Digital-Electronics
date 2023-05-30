# BCD TO GRAY CONVERTION USING VERLOG

# Equipments Required:
```
1.Hardware – PCs, Cyclone II , USB flasher
2.Software – Quartus prime
```
# THEORY
```
BCD (Binary-Coded Decimal) to Gray code conversion can be achieved by following a set of rules. Gray code is a binary numeral system where two successive values differ by only one bit. Here's the procedure to convert BCD to Gray code:

1.Write down the BCD number you want to convert.
2.Divide the BCD number into groups of four bits each, starting from the rightmost side. If the leftmost group has fewer than four bits, pad it with zeros on the left.
3.Convert each group of four bits into its equivalent Gray code using the following rules:
The leftmost bit of the Gray code group remains the same as the leftmost bit of the BCD group.
The second bit of the Gray code group is obtained by performing an XOR operation on the second bit of the BCD group and the leftmost bit of the BCD group.
The third bit of the Gray code group is obtained by performing an XOR operation on the third bit of the BCD group and the second bit of the BCD group.
The rightmost bit of the Gray code group is obtained by performing an XOR operation on the fourth bit of the BCD group and the third bit of the BCD group.
4.Concatenate the converted Gray code groups from left to right to obtain the final Gray code representation.
Let's take an example to illustrate the conversion:

BCD number: 1101 0110

Group 1: 1101 (leftmost group) Gray code group 1: 1101 (remains the same)

Group 2: 0110 Gray code group 2: 0101 (XOR operation: 0 XOR 1 = 1, 1 XOR 1 = 0, 1 XOR 0 = 1, 0 XOR 0 = 0)

Final Gray code: 1101 0101

Therefore, the Gray code representation of the BCD number 1101 0110 is 1101 0101.
```
# LOGIC DIAGRAM
![image](https://github.com/harinidq/Simulation-project--Digital-Electronics/assets/113497680/39669a03-4a7c-4dd2-8217-a708ef67d2e1)
# PROCEDURE:
```
1.Create a project with required entities.

2.Create a module along with respective file name.

3.Run the respective programs for the given boolean equations.

4.Run the module and get the respective RTL outputs.

5.Create university program(VWF) for getting timing diagram.

6.Give the respective inputs for timing diagram and obtain the results.
```
# NETLIST DIAGRAM
![image](https://github.com/harinidq/Simulation-project--Digital-Electronics/assets/113497680/e7682029-290b-4df0-aa3d-87d9141e385d)

# TIMING DIAGRAM
![image](https://github.com/harinidq/Simulation-project--Digital-Electronics/assets/113497680/f0b68697-0bc9-439f-a9c8-4f9d9a743ac9)
# PROGRAM
```
Program to Design and simulate BCD to gray converter using Verilog.
Developed by:  M.D.HARINI
RegisterNumber:  212222230043
module bcd(BCD, G);
input [3:0] BCD;
output [3:0] G;
reg[3:0]G;
always@(BCD)
begin
G[3]=BCD[3];
G[2]=BCD[3]^BCD[2];
G[1]=BCD[2]^BCD[1];
G[0]=BCD[1]^BCD[0];
end
endmodule
```
# RESULT :
Hence BCD to gray converter using Verilog has been designed and stimulated.
# REFERENCE
https://www.scribd.com/document/214003930/VERILOG-CODE-FOR-CODE-CONVERTERS
