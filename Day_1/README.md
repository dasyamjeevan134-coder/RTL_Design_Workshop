# Day 1 - Good MUX

Day 1 focuses on understanding the design, simulation, and synthesis of a good Multiplexer (MUX) using RTL design techniques.

In this session, I worked with a properly designed MUX and observed its behavior through RTL simulation and synthesis.

The design was simulated using Verilog and the waveform was observed using GTKWave. The RTL design was also synthesized using Yosys to analyze the generated netlist and block diagram.

---

# Index

1. [Objective](#1-objective)
2. [Theory](#2-theory)
3. [Good MUX](#3-good-mux)
4. [RTL Simulation](#4-rtl-simulation)
5. [Synthesis](#5-synthesis)
6. [Netlist and Block Diagram](#6-netlist-and-block-diagram)
7. [Overall Learning](#7-overall-learning)
8. [Conclusion](#8-conclusion)

---

# 1. Objective

The main objective of Day 1 was to understand how a Multiplexer can be designed using RTL and how the RTL description is converted into hardware during synthesis.

The main concepts covered were:

- Multiplexer (MUX)
- RTL design
- Combinational logic
- Select signals
- Input and output signals
- RTL simulation
- Waveform analysis using GTKWave
- RTL synthesis using Yosys
- Netlist generation
- Block diagram analysis
- Verification of MUX functionality

---

# 2. Theory

## Multiplexer

A Multiplexer, commonly called a MUX, is a combinational digital circuit that selects one input from multiple input signals and transfers the selected input to a single output.

The selection of the input is controlled by select lines.

For a 2:1 MUX:

- There are 2 input signals.
- There is 1 select signal.
- There is 1 output signal.

The operation of a 2:1 MUX can be represented as:

| Select | Output |
|--------|--------|
| 0 | Input 0 |
| 1 | Input 1 |

The Boolean expression for a 2:1 MUX is:

```text
Y = (~S & I0) | (S & I1)
```

where:

- `I0` = First input
- `I1` = Second input
- `S` = Select signal
- `Y` = Output

A good MUX design should assign the output correctly for every possible value of the select signal.

---

# 3. Good MUX

## What I designed

In this experiment, I worked with a properly designed Multiplexer.

The MUX was described using RTL coding techniques to implement combinational logic.

The select signal determines which input is connected to the output.

When the select signal is `0`, the first input is selected.

When the select signal is `1`, the second input is selected.

The design provides a complete assignment for the output, so unintended latch inference is avoided.

## Working

The operation of the MUX is:

```text
If select = 0:
    output = input 0

If select = 1:
    output = input 1
```

Therefore, the output always follows the selected input.

## Result

The Good MUX design correctly selects the required input according to the select signal.

---

# 4. RTL Simulation

## Simulation

The RTL design was simulated to verify the functional behavior of the MUX.

The simulation waveform was observed using GTKWave.

The input signals, select signal, and output signal were checked for different combinations.

The waveform confirms that the output follows the selected input.

### GTKWave Simulation Result

![Good MUX Waveform](./goodmuxtbwaveform.png)

## Waveform Analysis

When the select signal changes, the output changes according to the selected input.

For example:

- When `select = 0`, the output follows input `I0`.
- When `select = 1`, the output follows input `I1`.

This confirms the correct functional behavior of the MUX.

## File

- `goodmux waveform.png` - GTKWave simulation waveform

---

# 5. Synthesis

After verifying the RTL functionality through simulation, the design was synthesized using Yosys.

Synthesis converts the RTL description into a gate-level representation of the hardware.

Yosys analyzes the RTL and generates the corresponding hardware implementation.

The synthesized design was checked to verify that the intended MUX functionality was preserved.

---

# 6. Netlist and Block Diagram

The synthesized netlist and block diagram were observed to understand how the MUX RTL was converted into hardware.

The block diagram shows the input signals, select signal, multiplexer logic, and output connection.

### Netlist and Block Diagram Result

![Good MUX Netlist and Block Diagram](./goodmux%20netlist%20and%20blockdiagram.png)

## Result

The synthesized circuit represents the required MUX functionality using hardware logic.

The netlist helps show the actual logic structure generated from the RTL description.

The block diagram provides a graphical representation of the synthesized circuit.

## File

- `goodmux netlist and blockdiagra.png` - Yosys netlist and block diagram

---

# 7. Overall Learning

Through the Day 1 Good MUX experiment, I understood the following:

- What a Multiplexer is.
- How a MUX selects one input from multiple inputs.
- How select signals control a MUX.
- How to design a MUX using RTL.
- How combinational logic is represented in Verilog.
- How to verify MUX functionality using simulation.
- How to observe RTL waveforms using GTKWave.
- How the output changes according to the select signal.
- How RTL code is synthesized using Yosys.
- How a synthesized netlist represents the hardware.
- How to analyze a synthesized block diagram.
- The relationship between RTL code and synthesized hardware.
- The importance of complete assignments in combinational logic.
- How a properly designed MUX avoids unintended latch inference.

---

# 8. Conclusion

Day 1 helped me understand the basic concept and implementation of a Multiplexer using RTL design.

I designed a Good MUX and verified its functionality through RTL simulation using GTKWave. The waveform confirmed that the output correctly follows the input selected by the select signal.

The design was then synthesized using Yosys, and the generated netlist and block diagram were analyzed to understand the corresponding hardware implementation.

Overall, Day 1 provided a basic understanding of MUX design, RTL simulation, waveform analysis, synthesis, netlist generation, and the conversion of RTL code into digital hardware.
