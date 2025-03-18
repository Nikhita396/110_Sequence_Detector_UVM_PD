# 110_Sequence_Detector_UVM_PD
# Sequence Detector using EDA Playground with UVM and Physical Design using OpenROAD

## Overview
This project implements a **Sequence Detector** using SystemVerilog on **EDA Playground** with Universal Verification Methodology (**UVM**). The physical design implementation is done using the open-source tool **OpenROAD**.

## Table of Contents
- [Project Description](#project-description)
- [Features](#features)
- [Setup and Requirements](#setup-and-requirements)
- [Usage](#usage)
- [Design Flow](#design-flow)
- [Simulation and Verification](#simulation-and-verification)
- [Physical Design](#physical-design)
- [Results](#results)
- [References](#references)

## Project Description
A **sequence detector** identifies a predefined sequence of bits in an input stream and produces a signal when the sequence is detected. This project demonstrates:
- **Design and simulation** of a sequence detector using **EDA Playground**.
- **UVM-based verification** methodology for robust testing.
- **Physical design** implementation using **OpenROAD**.

## Features
- Implemented in **SystemVerilog**.
- UVM-based **testbench for verification**.
- Uses **EDA Playground** for simulation.
- OpenROAD for **synthesis, floorplanning, placement, and routing**.

## Setup and Requirements
### Tools Used:
- **EDA Playground** (https://www.edaplayground.com/)
- **OpenROAD** (https://github.com/The-OpenROAD-Project/OpenROAD)
- SystemVerilog with UVM
- Standard Cell Library (e.g., SKY130 or Nangate45)

## Usage
### Running the Sequence Detector in EDA Playground
1. Open [EDA Playground](https://www.edaplayground.com/).
2. Copy and paste the SystemVerilog design and testbench.
3. Run the simulation and check waveform outputs.

### Running UVM Testbench
1. Include UVM package in EDA Playground.
2. Run the testbench and analyze verification results.

### Running Physical Design in OpenROAD
1. Clone the OpenROAD repository:
   ```sh
   git clone https://github.com/The-OpenROAD-Project/OpenROAD.git
   ```
2. Setup the design files and run synthesis:
   ```sh
   yosys -p "read_verilog sequence_detector.v; synth -top sequence_detector; write_verilog synth_out.v"
   ```
3. Perform floorplanning, placement, and routing using OpenROAD commands.

## Design Flow
1. **RTL Design** – SystemVerilog implementation of the sequence detector.
2. **Simulation** – Use EDA Playground for functional verification.
3. **Verification** – UVM-based testbench ensures correctness.
4. **Synthesis** – Convert RTL into a gate-level netlist using Yosys.
5. **Physical Design** – OpenROAD handles placement, routing, and timing analysis.

## Simulation and Verification
- The UVM testbench generates test sequences and verifies output correctness.
- Log files and waveforms (via GTKWave) validate the detection process.

## Physical Design
- **Synthesis:** Yosys converts RTL into gates.
- **Floorplanning:** Defines the layout dimensions.
- **Placement:** Places the standard cells optimally.
- **Routing:** Connects cells while meeting timing constraints.
- **Signoff:** Verifies DRC, LVS, and timing closure.

## Results
- Functional correctness validated using UVM testbench.
- Successful synthesis and layout generation in OpenROAD.
- Timing and area reports confirm performance.

## References
- [EDA Playground](https://www.edaplayground.com/)
- [UVM Methodology](https://verificationacademy.com/uvm)
- [OpenROAD Project](https://github.com/The-OpenROAD-Project/OpenROAD)
- [SKY130 PDK](https://github.com/google/skywater-pdk)

---
### Author:
**Nikhita Patil**
