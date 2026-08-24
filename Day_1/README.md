# Day 1 – Good MUX

## 📑 Index

1. [Objective](#objective)
2. [Theory](#theory)
3. [Design](#design)
4. [Simulation](#simulation)
5. [Synthesis](#synthesis)
6. [Results](#results)
7. [What I Learned](#what-i-learned)
8. [Conclusion](#conclusion)

---

## Objective

In this experiment, I designed and verified a simple 2:1 Multiplexer
(MUX) using Verilog RTL.

The design was simulated to verify its functionality and then
synthesized to observe the corresponding hardware implementation.

---

## Theory

A Multiplexer (MUX) is a combinational digital circuit used to select
one input from multiple input signals and pass the selected input to
a single output.

A 2:1 MUX consists of:

- Two data inputs: `i0` and `i1`
- One select input: `sel`
- One output: `y`

The operation is:

- When `sel = 0`, the output `y` follows `i0`.
- When `sel = 1`, the output `y` follows `i1`.

The Boolean expression for a 2:1 MUX is:

```text
y = (~sel & i0) | (sel & i1)

The same functionality can be represented in Verilog using the ternary operator:

y = sel ? i1 : i0;

Truth Table

sel	y

0	i0
1	i1



---

Design

The 2:1 MUX was designed using Verilog HDL at the RTL level.

The RTL design describes the required functionality of the MUX before synthesis.

The basic design contains two inputs, one select signal and one output.

i0 ─────┐
                │
                │
             ┌──▼───┐
        i1 ─►│  MUX │────► y
             └──┬───┘
                │
               sel

The select signal determines which input is passed to the output.


---

Simulation

The RTL design was simulated using a testbench to verify the functionality of the MUX.

Different combinations of i0, i1, and sel were applied during simulation.

The output y was observed to ensure that it follows the selected input.

Testbench Waveform



The waveform verifies that:

sel = 0 → y = i0

sel = 1 → y = i1


Therefore, the simulation confirms the correct operation of the 2:1 MUX.


---

Synthesis

After successful RTL simulation, the MUX design was synthesized.

Synthesis converts the RTL description into a hardware-level representation. The synthesized design can be analyzed using the generated netlist and block diagram.

Netlist and Block Diagram



The synthesis result represents the hardware implementation generated from the RTL MUX design.


---

Results

The 2:1 MUX was successfully simulated and synthesized.

The simulation waveform verified that the output correctly follows the selected input.

The synthesized netlist and block diagram showed the corresponding hardware implementation of the MUX.


---

What I Learned

From this experiment, I learned:

The basic concept and working of a 2:1 Multiplexer.

How to describe a MUX using Verilog RTL.

How the select signal controls the output.

How to perform RTL simulation.

How to analyze simulation waveforms.

The basic RTL-to-synthesis flow.

How to understand a synthesized netlist and block diagram.

How RTL code is converted into hardware.



---

Conclusion

The 2:1 Good MUX was successfully designed using Verilog RTL.

The simulation waveform verified the correct functionality of the design, where the output follows i0 when sel = 0 and follows i1 when sel = 1.

The design was also synthesized successfully, and the generated netlist and block diagram provided the hardware representation of the MUX.

This experiment helped in understanding the basic RTL design, simulation, verification and synthesis flow.


---

🔝 Back to Index

Back to Index

This version uses your **exact Day 1 filenames**:

`goodmuxtbwaveform.png`  
`goodmux netlist and blocksdiagram.png`
