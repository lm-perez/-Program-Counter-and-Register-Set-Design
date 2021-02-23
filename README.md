# Program-Counter-and-Register-Set-Design
The objective is to implement, test and simulate: the 32-bit and 1-bit Register Set required for the 32-bit CPU, and the 32-bit Program Counter (PC) required for the 32-bit CPU.

**Design and Implementation**

There are five components: a 1-bit register, 32-bit register, an adder, a 2-to-1 multiplexer and a program counter. The components   will be implemented using VHDL and their corresponding codes are attached in the appendix. The components will be simulated using     Quartus II and the implementation of the components will be correct if the outputs in all the simulations correspond to the truth     tables of the components

**I: 1-Bit Register**
The 1-bit register is basically used as a storage or memory unit. Each bit in a register is implemented by a flip-flop that has the inputs: clock (clk), input data (d), load (ld), and clear (clr), and have the 1-bit output (q). To change the value stored in the register, the input data must be ‘1,’ and the load and clock has to be high. When all conditions are met, the data and output of the 1-bit register will be changed. However, when the clear input is high, the data in the register will be reset to 0. 

**II: 32-Bit Register**
The 32-bit register has the same functions and conditions of the 1-bit register. The difference between a 32-bit register and a 1-bit register is that a 32-bit register stores 32-bits while the 1-bit register stores 1-bit, resulting in the 32-bit having at least 32 flip flops.

**III: Adder**
The adder is one of the components in the program counter. It has an input (A) and an output (B). The functional simulation shows the input and the output in hexadecimal. The adder is also not dependent on a clock input. The adder in this lab adds the input value (A) with number 4 and the result is the output (B).

**IV: 2-to-1 Multiplexer**
The 2-to-1 multiplexer consists of three inputs: s, w0, and w1; and one output (f). The input signal ‘s’ is the select signal. The output is dependent on the select signal. If ‘s’ = 0, then the output is the value of ‘w0’. If ‘s’ = 1, then the output is the value of ‘w1’. Similar to the adder, it is not dependent on a clock signal.

**V: Program Counter**
The program counter is made up of the components: a 32-bit register, an adder, and a 2-to-1 multiplexer. It has the inputs: clock (clk), input data (d), clear (clr), load (ld), and increment (inc). Similar to the 1-bit register, the clock, clear and load inputs function the same way; whereas the increment input causes the adder to increment the input data by 4 when it is high.
