# SERIAL-IN-SERIAL-OUT-SHIFTREGISTER

**AIM:**

To implement  SISO Shift Register using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY:**

**SISO shift Register:**

A Serial-In Serial-Out shift register is a sequential logic circuit that allows data to be shifted in and out one bit at a time in a serial manner. It consists of a cascade of flip-flops connected in series, forming a chain. The input data is applied to the first flip-flop in the chain, and as the clock pulses, the data propagates through the flip-flops, ultimately appearing at the output.

The logic circuit provided below demonstrates a serial-in serial-out (SISO) shift register. It comprises four D flip-flops that are interconnected in a sequential manner. These flip-flops operate synchronously with one another, as they all receive the same clock signal.

![image](https://github.com/naavaneetha/SERIAL-IN-SERIAL-OUT-SHIFTREGISTER/assets/154305477/e81c4072-37f9-46c6-8145-566764b74c3a)

Figure 01 4 Bit SISO Register

The synchronous nature of the flip-flops ensures that the shifting of data occurs in a coordinated manner. When the clock signal rises, the input data is sampled and stored in the first flip-flop. On subsequent clock pulses, the stored data propagates through the flip-flops, moving from one flip-flop to the next.
Each D flip-flop in the circuit has a Data (D) input, a Clock (CLK) input, and an output (Q). The D input represents the data to be loaded into the flip-flop, while the CLK input is connected to the common clock signal. The output (Q) of each flip-flop is connected to the D input of the next flip-flop, forming a cascade.

**Procedure:**
```
1.Set Up Project: Open Quartus Prime, create a new project, and add a new Verilog file.
2.Write Optimized Code: Implement the Verilog code using efficient shift operations.
3.Compile Code: Save and compile the code, fixing any errors during compilation.
4.Create Test Bench: Develop a test bench to generate clock signals and input data.
5.Simulate Design: Run functional simulation and observe timing diagrams.
6.Validate and Document: Confirm the output matches expected results, capture screenshots, and record observations.
```

**PROGRAM**
```
Developed by: Sushiendar M
RegisterNumber: 212223040217
module serialinserialoutregister(clk, sin, q);
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

**RTL LOGIC FOR SISO Shift Register:**
![image](https://github.com/user-attachments/assets/12a5ca17-4e84-4188-a885-97d246c427ac)


**TIMING DIGRAMS FOR SISO Shift Register:**
![image](https://github.com/user-attachments/assets/7bec7c08-6280-4c1e-91f3-f5964a199b71)


**RESULTS:**
The SISO shift register was successfully implemented using optimized Verilog code in Quartus Prime. Functional simulation confirmed that the register shifts data serially on each clock pulse. The RTL diagram and timing waveforms validated the circuit's synchronous data propagation. This streamlined approach confirmed efficient and accurate SISO shift register operation as expected.
