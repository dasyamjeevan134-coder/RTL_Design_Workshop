# Day 1 – Good MUX

## 📑 Index

1. [Objective](#objective)
2. [Design](#design)
3. [Simulation](#simulation)
4. [Synthesis](#synthesis)
5. [Results](#results)
6. [What I Learned](#what-i-learned)
7. [Conclusion](#conclusion)

---

## Objective

In this experiment, I designed and verified a simple 2:1 Multiplexer
(MUX) using Verilog. The design was first simulated to verify its
functional behavior and then synthesized using Yosys to observe how
the RTL design is converted into a gate-level implementation.

---

## Design

The Good MUX has two data inputs, one select input, and one output.

- `i0` – First data input
- `i1` – Second data input
- `sel` – Select input
- `y` – Output

The operation of the MUX is:

- When `sel = 0`, `y = i0`
- When `sel = 1`, `y = i1`

The Verilog RTL describes this behavior using an `always` block.

---

## Simulation

After writing the RTL, I simulated the Good MUX using a Verilog
simulation environment. Different combinations of `i0`, `i1`, and
`sel` were applied through the testbench.

The generated waveform was viewed using GTKWave. The waveform contains
the signals `i0`, `i1`, `sel`, and `y`.

The waveform confirms that the output `y` follows the selected input
correctly.

### GTKWave Simulation Result

![Good MUX Waveform](./goodmuxtbwaveform.png)

---

## Synthesis

After successful simulation, I synthesized the Good MUX RTL using
Yosys.

The synthesized design was mapped to the Sky130 standard cell library.
The generated netlist and block diagram show how the MUX functionality
is represented at the gate level.

### Yosys Synthesized Block Diagram

![Good MUX Netlist and Block Diagram](./goodmuxnetlistandblockdiagram.png)

---

## Results

The Good MUX was successfully simulated and synthesized.

The GTKWave output verified the functional behavior of the MUX for
different input and select combinations.

The Yosys synthesis result generated the corresponding gate-level
implementation and block diagram, showing the mapping of the RTL
design to a standard cell from the Sky130 library.

---

## What I Learned

From this experiment, I learned:

- How to design a 2:1 MUX using Verilog RTL.
- How to create and use a testbench for functional verification.
- How to simulate a Verilog design.
- How to generate and analyze waveform outputs using GTKWave.
- How to synthesize RTL using Yosys.
- How RTL logic is converted into a gate-level netlist.
- How a synthesized design can be represented using standard cells.
- How to observe the relationship between RTL code and synthesized hardware.

---

## Conclusion

The Good MUX was successfully designed, simulated, and synthesized.
The simulation waveform verified that the output correctly follows the
selected input. The Yosys synthesis result demonstrated the conversion
of the RTL MUX into a gate-level implementation using the Sky130
standard cell library.

This experiment provided a practical understanding of the basic
RTL-to-gate-level digital design flow.

---

### 🔝 Back to Index

[Back to Index](#-index)
