# VHDL7
A Synchronous Up Counter is a sequential logic circuit where all the flip-flops are triggered simultaneously by the same clock signal. <br>
The counter increases its count on each clock pulse, and a 4-bit counter can count from 0000 (0 in decimal) to 1111 (15 in decimal) before rolling back to 0000. <br>

`Aim:`
<br>
To design and simulate a 4-bit synchronous up counter using Verilog HDL and verify its functionality through simulation.

`Apparatus Required:`

-Xilinx Vivado (or any Verilog simulator).<br>
-PC/Laptop with required software tools.<br>

`Code Implementation:`

module up_counter(input clk, input reset, output reg [3:0] count);<br>
  always @(posedge clk or posedge reset) begin<br>
    if (reset)<br>
      count <= 4'b0000;<br>
    else<br>
      count <= count + 1;<br>
  end<br>
endmodule<br>

![WhatsApp Image 2024-10-15 at 18 36 29_425d71d5](https://github.com/user-attachments/assets/58871c3d-d298-4f15-bd52-864a21bd6f25)

`Output Waveform:`

![WhatsApp Image 2024-10-15 at 18 45 50_6a2f2dc1](https://github.com/user-attachments/assets/4213739c-f918-4df2-b1dc-48fe4d77d7e4)

`Result:`

The 4-bit synchronous up counter was successfully designed and simulated using Verilog HDL. <br>
<br>
The output matched the expected behavior based on the truth table of the counter, with the counter counting from 0000 to 1111 on each clock pulse and resetting afterward.<br>



