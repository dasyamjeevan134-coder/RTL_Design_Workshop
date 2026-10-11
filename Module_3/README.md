# ASIC Design and SoC Chip

## Sky130 CMOS Inverter Design, SPICE Simulation and Physical Design

## Index

1. Introduction
2. Objective
3. Design Used
4. ASIC Design Flow
5. Configuration and Design Files
6. Synthesis and Simulation Analysis
7. Floorplanning and Physical Design
8. LEF and Technology Libraries
9. Timing and Waveform Analysis
10. Results and Conclusion

---

## 1. Introduction

ASIC design involves developing integrated circuits for specific applications. The design process includes circuit design, simulation, verification, and physical implementation.

This module focuses on CMOS inverter design and analysis using SkyWater SKY130 technology. It includes SPICE simulation resources, inverter waveform visualizations, transistor-related library images, and physical floorplanning and layout references.

The module provides an introduction to the relationship between transistor-level circuit behavior and the physical implementation of integrated circuits.

## 2. Objective

The main objectives of this module are:

- To understand the working principle of a CMOS inverter.
- To study PMOS and NMOS transistor operation.
- To understand SPICE-based circuit simulation.
- To examine inverter input and output waveforms.
- To become familiar with Sky130 technology resources.
- To study floorplanning and physical layout concepts.
- To understand the role of technology libraries in ASIC design.

## 3. Design Used

3.1 CMOS Inverter

A CMOS inverter is a fundamental digital circuit consisting of one PMOS transistor and one NMOS transistor.

The circuit produces an output that is the logical complement of the input.

Boolean expression:

Y = NOT(A)

3.2 Working Principle

- Input LOW: The PMOS transistor turns ON, and the NMOS transistor turns OFF. The output becomes HIGH.
- Input HIGH: The PMOS transistor turns OFF, and the NMOS transistor turns ON. The output becomes LOW.

This complementary switching behavior allows the inverter to perform logical inversion.

3.3 Technology Used

The design uses SkyWater SKY130 technology resources. The Process Design Kit (PDK) provides technology-specific information and transistor models for circuit design and simulation.

NGSpice can be used to simulate the inverter when the required netlist and compatible transistor models are available.

## 4. ASIC Design Flow

The general ASIC design flow includes the following stages:

1. RTL design.
2. Logic synthesis.
3. Floorplanning.
4. Power planning.
5. Placement.
6. Clock-tree synthesis, when required.
7. Routing.
8. Physical verification.
9. Static timing analysis.

For transistor-level inverter analysis, the corresponding workflow includes preparing a circuit netlist, loading device models, running SPICE simulation, and analyzing the resulting waveforms.

Conceptual flow:

CMOS Inverter → Sky130 Device Models → SPICE Simulation → Waveform Analysis → Layout and Floorplan Visualization

The exact implementation stages depend on the tools and design files used.

## 5. Configuration and Design Files

The following files are present in the module:

File Name| Description
"README.md"| Module documentation.
"sky130_inv_spice.png"| Sky130 inverter SPICE-related visualization.
"ngspice sky130_inv.spices.png"| NGSpice simulation-related image.
"inv_waveform.png"| Inverter waveform visualization.
"plot vs time graphical spice.png"| Time-domain simulation graph.
"floorplan.png"| Floorplanning visualization.
"floorplan.tcl.png"| Floorplanning Tcl-related image.
"inverter_layout.png"| Physical layout visualization of the inverter.
"merged floorplan layout_11.png"| Combined floorplan layout image.
"pshortlib_2.png"| PMOS-related library or device visualization.
"pshorts_lib.png"| Additional PMOS-related visualization.
"readme.ma_floorplans.png"| Floorplanning documentation-related image.

The descriptions are based on the filenames. The images should be inspected to confirm their exact contents.

## 6. Synthesis and Simulation Analysis

Circuit simulation is used to study the electrical behavior of electronic components before implementation.

For a CMOS inverter, SPICE simulation helps analyze the relationship between the input and output voltages.

Important observations include:

- Input and output voltage levels.
- Switching behavior.
- Rise and fall transitions.
- Propagation delay.
- The response of the circuit to changing input signals.

Synthesis is a separate process that converts a digital hardware description into a gate-level netlist. The visible filenames alone do not establish that synthesis was performed in this module.

## 7. Floorplanning and Physical Design

Floorplanning is an important stage of physical implementation. It defines the arrangement of the design area and provides a foundation for subsequent placement and routing.

The floorplan images in this module provide visual references for understanding physical design organization.

Important concepts include:

- Die area and core area.
- Component placement.
- Power distribution.
- Layout organization.
- Preparation for placement and routing.

The inverter layout image can be used to understand how a circuit is represented geometrically.

## 8. LEF and Technology Libraries

Technology libraries provide information needed by design and implementation tools.

LEF stands for Library Exchange Format. It describes physical information such as cell dimensions, pin locations, and routing obstructions.

Technology LEF files provide process-specific physical information, while cell LEF files describe the physical abstracts of standard cells.

Transistor model files used by SPICE serve a different purpose: they describe the electrical behavior of devices during circuit simulation.

These resources are important for connecting logical design, physical implementation, and circuit-level analysis.

## 9. Timing and Waveform Analysis

Waveform analysis helps verify the expected switching behavior of the inverter.

When the input changes from LOW to HIGH, the output should change from HIGH to LOW. When the input changes from HIGH to LOW, the output should change from LOW to HIGH.

The waveform can be used to investigate:

- Input and output transitions.
- Voltage levels.
- Rise time and fall time.
- Propagation delay.

Static Timing Analysis (STA) evaluates timing constraints in a digital implementation. Actual STA results require the appropriate timing reports and constraints; they cannot be determined from the image filenames alone.

## 10. Results and Conclusion

This module introduces CMOS inverter operation, Sky130 transistor models, SPICE simulation, waveform analysis, and physical layout concepts.

The main learning outcomes are:

1. Understanding the complementary switching behavior of a CMOS inverter.
2. Learning how SPICE simulation is used to analyze circuit behavior.
3. Understanding the role of transistor models and technology libraries.
4. Becoming familiar with floorplanning and layout visualization.
5. Understanding the distinction between circuit simulation, synthesis, physical design, and timing analysis.

In conclusion, this module provides a foundation for understanding transistor-level circuit behavior and its relationship to ASIC physical implementation using open-source design resources.

2. NGSpice documentation.
3. CMOS digital circuit design references.
4. Open-source ASIC design and physical implementation resources.
