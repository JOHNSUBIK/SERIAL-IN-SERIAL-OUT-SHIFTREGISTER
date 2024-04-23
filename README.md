# SERIAL-IN-SERIAL-OUT-SHIFTREGISTER

**AIM:**

To implement  SISO Shift Register using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**SISO shift Register**

A Serial-In Serial-Out shift register is a sequential logic circuit that allows data to be shifted in and out one bit at a time in a serial manner. It consists of a cascade of flip-flops connected in series, forming a chain. The input data is applied to the first flip-flop in the chain, and as the clock pulses, the data propagates through the flip-flops, ultimately appearing at the output.

The logic circuit provided below demonstrates a serial-in serial-out (SISO) shift register. It comprises four D flip-flops that are interconnected in a sequential manner. These flip-flops operate synchronously with one another, as they all receive the same clock signal.

![image](https://github.com/naavaneetha/SERIAL-IN-SERIAL-OUT-SHIFTREGISTER/assets/154305477/e81c4072-37f9-46c6-8145-566764b74c3a)

Figure 01 4 Bit SISO Register

The synchronous nature of the flip-flops ensures that the shifting of data occurs in a coordinated manner. When the clock signal rises, the input data is sampled and stored in the first flip-flop. On subsequent clock pulses, the stored data propagates through the flip-flops, moving from one flip-flop to the next.
Each D flip-flop in the circuit has a Data (D) input, a Clock (CLK) input, and an output (Q). The D input represents the data to be loaded into the flip-flop, while the CLK input is connected to the common clock signal. The output (Q) of each flip-flop is connected to the D input of the next flip-flop, forming a cascade.

**Procedure**
1.Initialize the shift register to a known state (e.g., all zeros).
2.Input a bit serially into the shift register.
3.Shift the contents of the register one position to the right (or left). 
4.Output the shifted bit from the last stage of the register. 
5.Repeat steps 2-4 for each bit you want to input and shift.

**PROGRAM**
Program for flipflops and verify its truth table in quartus using Verilog programming.
```
Developed by: John Paul J
RegisterNumber:212223230093
```
```
module EXP10(clk, sin, q);
input clk;
input sin;
output [3:0] q;
reg [3:0] q;
always @(posedge clk)
begin
q[0] <= sin;
q[1] <= q[0];
q[2] <= q[1];
q[3] <= q[2];
end
endmodule
```

**RTL LOGIC FOR SISO Shift Register**
![324244027-2abb0e55-1c71-4c43-8fc9-5f3a335f7d54](https://github.com/JOHNSUBIK/SERIAL-IN-SERIAL-OUT-SHIFTREGISTER/assets/150279319/2580617d-e901-40e6-b8ff-b1f2185ba8bf)

**TIMING DIGRAMS FOR SISO Shift Register**
![324244048-b0182cc2-4c6c-4fca-9aed-811e977833cc](https://github.com/JOHNSUBIK/SERIAL-IN-SERIAL-OUT-SHIFTREGISTER/assets/150279319/703014d3-0883-4fb5-85d2-4f1b06b88cb3)

**RESULTS:**

SISO Shift Register using verilog and validating their functionality using their functional tables has successful execution of the program.
