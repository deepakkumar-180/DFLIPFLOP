# DFLIPFLOP
AIM:

To implement D flipflop using verilog and validating their functionality using their functional tables

SOFTWARE REQUIRED: Quartus prime

THEORY

D Flip-Flop

D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.

1
This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable. The following table shows the state table of D flip-flop.

2
Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as Qt+1t+1 = D

3
Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.

PROGRAM:
```
module data_flip_flop (
    input  wire clk, rst, D,
    output reg  Q
);
    always @(posedge clk or posedge rst) begin
        if (rst)
            Q <= 1'b0;   // Reset
        else
            Q <= D;      // Capture D at clock edge
    end
endmodule
```
IMAGE: [GATE.pdf](https://github.com/user-attachments/files/24150612/GATE.pdf)


WAVEFORM: [WAVE.pdf](https://github.com/user-attachments/files/24150613/WAVE.pdf)


NAME: DEEPAKKUMAR S

REF NO : 25016457

RESULT: Thus the D flipflop using verilog and validating their functionality using their functional tables is verified
