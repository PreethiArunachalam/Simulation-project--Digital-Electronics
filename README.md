# TITTLE
IMPLEMENT EX NOR GATE USING NAND GATE ONLY

# THEORY
### Step:1
In the implementation of EX NOR gate using NAND gate we can consider a and b are input wires and y is an output wire.

### Step:2
The output y wire is assigned to the output of the final NAND gate which is implemented using the two intermediate NAND gates nand2 and nand3.

### Step:3
The two inputs a and b are connected to the first NAND gate nand1. 

### Step:4
The ~ operator is used to negate the output of the NAND gates to implement the logical negation.

# LOGIC DIAGRAM

![image](https://github.com/PreethiArunachalam/Simulation-project--Digital-Electronics/assets/120115840/9704ede0-2758-4c2d-8393-6422878b7cb6)

# NETLIST DIAGRAM

![image](https://github.com/PreethiArunachalam/Simulation-project--Digital-Electronics/assets/120115840/f3aff621-c881-47e2-9961-dd63bd825f67)

# TIMING DIAGRAM

![image](https://github.com/PreethiArunachalam/Simulation-project--Digital-Electronics/assets/120115840/3f618f08-f32d-46e6-8b3c-85fb9a9bdf62)

# PROGRAM
```
module ass1(a,b,y);
input a,b;
output y;
wire nand1, nand2, nand3;
assign nand1 = ~(a & b);
assign nand2 = ~(a & nand1);
assign nand3 = ~(b & nand1);
assign y = ~(nand2 & nand3);
endmodule
```
# REFERENCE
Thus the implementation of Ex Nor gate using Nand gate is obtained. 
