ASIC Design and SoC Chip

PicoRV32A ASIC Physical Design Using OpenLane and Sky130

Index

1. Introduction
2. Objective
3. Design Used
4. ASIC Physical Design Flow
5. Configuration and Flow Files
6. LEF Merging and Technology Libraries
7. Floorplanning and Placement
8. PicoRV32A Design Statistics
9. Layout Analysis and Observations
10. Results and Conclusion

---

1. Introduction

Application-Specific Integrated Circuit (ASIC) design involves implementing a digital circuit for a specific application. The physical design stage converts the synthesized circuit into a physical layout suitable for semiconductor implementation.

This module focuses on the physical design concepts associated with the PicoRV32A RISC-V processor using open-source ASIC design tools and SkyWater SKY130 technology.

The module includes visual references related to configuration files, LEF merging, standard-cell libraries, placement layouts, and PicoRV32A design statistics.

These activities help explain how a processor design is prepared for physical implementation.

2. Objective

The main objectives of this module are:

- To understand the physical design flow of a RISC-V processor.
- To study the configuration required for ASIC implementation.
- To understand the role of LEF files and technology libraries.
- To learn about standard-cell physical abstracts.
- To study placement and layout visualizations.
- To examine PicoRV32A design statistics.
- To understand the relationship between technology configuration, placement, and physical implementation.

3. Design Used

3.1 PicoRV32A Processor

PicoRV32A is a variant of the PicoRV32 processor, a compact implementation of the RISC-V instruction set architecture.

A processor design contains digital logic blocks that work together to execute instructions and process data.

The synthesized design can be mapped to standard cells and implemented using a compatible technology library.

3.2 Technology Used

The module references SkyWater SKY130 technology resources and standard-cell physical information.

The SKY130 Process Design Kit (PDK) provides technology-specific information needed for circuit implementation, including physical and electrical library resources.

3.3 Tools and Resources

The design flow may involve:

- OpenLane for ASIC implementation.
- Yosys for logic synthesis.
- OpenROAD for physical design operations.
- SkyWater SKY130 PDK for technology information.
- LEF files for physical cell and routing information.

The exact tools and versions depend on the configuration used in the project.

4. ASIC Physical Design Flow

The general ASIC implementation flow includes the following stages:

1. RTL design.
2. Logic synthesis.
3. Floorplanning.
4. Power planning.
5. Standard-cell placement.
6. Clock-tree synthesis, when required.
7. Routing.
8. Physical verification.
9. Static timing analysis.

Conceptual flow:

RTL Design → Synthesis → Floorplanning → LEF and Library Preparation → Placement → Routing → Verification → Timing Analysis

Each stage contributes to transforming the processor's logical description into a physical implementation.

5. Configuration and Flow Files

Configuration files define the parameters and resources required by the physical design tools.

The "config.tcl.png" file visible in the earlier module screenshot is associated with Module 4's configuration-related material.

A design configuration may specify:

- Design name and source files.
- Technology and process information.
- Standard-cell libraries.
- Clock and timing constraints.
- Floorplanning parameters.
- Tool-specific implementation settings.

Correct configuration ensures that the tools use compatible technology resources and design constraints.

6. LEF Merging and Technology Libraries

6.1 What Is LEF?

LEF stands for Library Exchange Format. It describes physical information required by physical design tools.

LEF data can include cell dimensions, pin locations, routing obstructions, and metal-layer information.

6.2 Standard-Cell LEF

Standard-cell LEF files describe the physical abstracts of library cells. These abstracts allow placement and routing tools to work with cells without requiring their complete transistor-level layouts.

6.3 Technology LEF

Technology LEF describes physical routing technology information, including metal layers, routing directions, and design-rule-related parameters used by the implementation tools.

6.4 LEF Merging

LEF merging combines the required technology and cell physical information into a form suitable for the design flow.

The files shown in this module include:

- "inv_less_vsdinv.lefs.png"
- "inv_vsdinv_layouts.png"
- "less sky130_2.png"
- "less sky130_fd.png"
- "less tracks.inf.png"
- "merged_lef.png"

These images appear to relate to LEF files, technology resources, routing tracks, and physical layout information. Their exact contents should be verified by opening the images.

7. Floorplanning and Placement

Floorplanning establishes the design area and prepares the design for subsequent physical implementation.

Placement assigns physical locations to standard cells while considering connectivity, timing, congestion, and design constraints.

Important concepts include:

- Core and die dimensions.
- Standard-cell placement.
- Placement density.
- Cell utilization.
- Routing resources.
- Congestion management.

The "placement_layouts.png" file provides a visual reference for examining the placement stage.

The quality of placement can influence routing complexity, timing performance, and overall implementation area.

8. PicoRV32A Design Statistics

Design statistics provide information about the synthesized or implemented processor.

Depending on the report stage, statistics may include:

- Total standard-cell count.
- Cell counts by type.
- Sequential and combinational cell counts.
- Estimated or implemented cell area.
- Utilization.
- Timing information.

The following files are present in the module:

- "picorv32a_stats.png"
- "picorv32a_stats_3.png"
- "picorv32a_stats1.png"

These images appear to contain PicoRV32A design statistics. The actual values should be transcribed from the images and identified by their corresponding flow stage.

Synthesis statistics and post-placement statistics should not be treated as interchangeable because placement and optimization can change the implementation.

9. Layout Analysis and Observations

Physical layout visualization helps explain how standard cells are arranged and connected during implementation.

The layout-related files can be examined to understand:

- Standard-cell placement patterns.
- Physical cell dimensions and boundaries.
- The role of technology and cell LEF files.
- The relationship between placement and routing resources.
- The relationship between design statistics and physical implementation.

The "inv_layout1.png" and "placement_layouts.png" files provide layout-related visual references, while the LEF images illustrate physical library information.

Detailed conclusions about timing closure, design-rule correctness, or routing completion require the corresponding tool reports.

10. Results and Conclusion

This module introduces important physical design concepts for a PicoRV32A-based ASIC implementation using Sky130 technology resources.

The main learning outcomes are:

1. Understanding the general ASIC physical design flow.
2. Learning the purpose of technology and standard-cell LEF files.
3. Understanding LEF merging and physical library preparation.
4. Studying standard-cell placement and layout visualizations.
5. Learning how to interpret processor design statistics.
6. Understanding the relationship between placement, area, and timing.

In conclusion, this module provides a foundation for understanding how a synthesized processor is prepared for physical implementation. It highlights the importance of correct technology configuration, physical library preparation, placement, and design statistics in an open-source ASIC workflow.

---

References

1. PicoRV32 project documentation.
2. SkyWater SKY130 PDK documentation.
3. OpenLane documentation.
4. OpenROAD documentation.
5. Yosys documentation.
6. LEF/DEF physical design format documentation.
