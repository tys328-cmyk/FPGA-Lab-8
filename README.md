ECE 128 Lab 8 – Sequential and Combinational Multipliers

Project Description

This project implements two multipliers in Verilog: a combinational multiplier and a sequential multiplier. The combinational multiplier forms all of the partial products and adds them in hardware at once, so the product depends only on the current inputs and no clock is needed. The sequential multiplier uses the shift-and-add method over multiple clock cycles, with registers for the operands and product and a control unit that starts the operation, counts the steps, and asserts a done signal when the product is ready. Each design has its own testbench, and a top module connects both designs to the Basys 3 board so the product can be shown on the LEDs or seven-segment display. The two designs are compared based on FPGA resource utilization.

Simulation

1. Open the project in Vivado.
2. Add the combinational multiplier or sequential multiplier module as a design source.
3. Add the corresponding testbench as a simulation source.
4. Set the testbench as the simulation top module.
5. Run Behavioral Simulation.
6. Verify from the waveform that the product matches the expected result for each pair of inputs. For the combinational multiplier, the product should change as soon as the inputs change. For the sequential multiplier, the product should be valid once the done signal goes high after start is asserted.

FPGA Implementation

1. Select the Basys 3 as the target FPGA board.
2. Select the top module as the top module for implementation.
3. Add the Basys 3 constraints file and assign the operands to switches, the clock, reset, and start signals to the board clock and buttons, and the product to the LEDs or seven-segment display.
4. Run Synthesis.
5. Run Implementation.
6. Generate the Bitstream.
7. Connect and power the Basys 3.
8. Open Hardware Manager and program the FPGA with the generated bitstream.
9. Enter different operand values on the switches and verify that the displayed product matches the expected result for both the combinational and sequential multipliers.
