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

1. Open Quartus and create a new Verilog file.
2. Copy and paste the corrected code and save the file.
3. Compile the program to check for errors.
4. Generate the RTL schematic and timing diagram.
5. Simulate the design to verify the serial shift operation.
   
## PROGRAM
## Developed by: VASANTH N
## RegisterNumber: 24000697

        module exp10(clk, sin, q);
            input clk;
            input sin;
            output [3:0] q;
            reg [3:0] q;
        
            always @(posedge clk) begin
                q[0] <= sin;
                q[1] <= q[0];
                q[2] <= q[1];
                q[3] <= q[2];  
            end
        endmodule

      
        
**RTL LOGIC FOR SISO Shift Register**
![Screenshot 2024-12-20 105336](https://github.com/user-attachments/assets/2df98983-f090-44dc-8d37-7860f5a009ef)

**TIMING DIGRAMS FOR SISO Shift Register**
![Screenshot 2024-12-20 105400](https://github.com/user-attachments/assets/5d4c6ee9-0fa8-4568-81c6-dc1634a67e66)

**RESULTS**   
Thus the Serial-In-Out shift register is implemented and verified.
