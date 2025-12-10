AIM:
To design a Full Adder and verify its truth table in Quartus using Verilog programming.
Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Full Adder
Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.
Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin
Carry = AB + ACin + BCin
 
Program:
```
module FullAdd (
    input  wire a, b, cin,   // Inputs
    output wire sum, carry   // Outputs
);

    // Logic equations
    assign sum   = a ^ b ^ cin;                  // XOR for sum
    assign carry = (a & b) | (b & cin) | (a & cin); // Majority function for carry

endmodule
```

Developed by:V Karthi RegisterNumber: 25017522 

RTL Schematic:
[FullAdd RTL.pdf](https://github.com/user-attachments/files/24073711/FullAdd.RTL.pdf)

Output Timing Waveform:
[FullAdd wave.pdf](https://github.com/user-attachments/files/24073712/FullAdd.wave.pdf)

Result: Thus, the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.
