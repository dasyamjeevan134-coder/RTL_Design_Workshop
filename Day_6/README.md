# RTL Design Workshop – Day 6

## Pre-Synthesis and Post-Synthesis Simulation

---

## Index

1. [Introduction](#1-introduction)
2. [Objective](#2-objective)
3. [Design Description](#3-design-description)
4. [Pre-Synthesis Simulation](#4-pre-synthesis-simulation)
5. [Synthesis](#5-synthesis)
6. [Post-Synthesis Simulation](#6-post-synthesis-simulation)
7. [Results](#7-results)
8. [Conclusion](#8-conclusion)

---

## 1. Introduction

Day 6 focuses on verifying the RTL design before and after synthesis. The design is simulated at RTL level, synthesized using Yosys, and then simulated again using the synthesized netlist.

---

## 2. Objective

- Perform pre-synthesis RTL simulation.
- Synthesize the RTL design using Yosys.
- Perform post-synthesis simulation.
- Compare both waveforms.
- Verify that synthesis preserves the intended functionality.

---

## 3. Design Description

The design is a digital RTL circuit written in Verilog HDL. The RTL implementation is first verified using functional simulation. After successful verification, the design is synthesized into a gate-level netlist.

---

## 4. Pre-Synthesis Simulation

The RTL design was simulated before synthesis to verify its functional behavior.

### Pre-Synthesis Waveform

![Pre-Synthesis Waveform](pre_synth%20waveform.png)

The waveform shows the input, clock, reset and output signals of the RTL design.

---

## 5. Synthesis

Yosys was used to synthesize the RTL design.

The synthesis process converts the behavioral RTL description into a gate-level netlist containing logic cells such as AND, OR, NOT, NAND/NOR gates and flip-flops.

---

## 6. Post-Synthesis Simulation

After synthesis, the generated netlist was simulated to verify the functionality of the synthesized circuit.

### Post-Synthesis Waveform

![Post-Synthesis Waveform](post_synth_sim%20waveforms.png)

The post-synthesis waveform is compared with the RTL waveform to check whether the functional behavior is preserved.

---

## 7. Results

The pre-synthesis and post-synthesis simulations show the expected behavior of the design.

- RTL simulation completed successfully.
- Synthesis was completed successfully using Yosys.
- Post-synthesis simulation was performed successfully.
- The important input and output transitions are consistent between RTL and post-synthesis simulations.

---

## 8. Conclusion

The RTL design was successfully synthesized and verified through post-synthesis simulation. The comparison of the waveforms confirms that the synthesized implementation preserves the intended functional behavior of the original RTL design.

---

## Files

- `README.md`
- `pre_synth waveform.png`
- `post_synth_sim waveforms.png`

## Tools Used

- Verilog HDL
- Yosys
- GTKWave
- Linux/Ubuntu
