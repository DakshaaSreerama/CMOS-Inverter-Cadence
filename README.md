# CMOS Inverter Design using Cadence Virtuoso

This project demonstrates the design, simulation, and verification of a CMOS inverter using **Cadence Virtuoso** with the **GPDK 90nm** technology library. The CMOS inverter, a fundamental digital logic gate, is used to invert binary signals and serves as the building block for more complex logic circuits.



## Overview

A **CMOS inverter** consists of a **PMOS** and **NMOS** transistor connected in a complementary arrangement:
- **When input is LOW (0V):** PMOS conducts, NMOS is off → output is HIGH (VDD)
- **When input is HIGH (VDD):** NMOS conducts, PMOS is off → output is LOW (0V)

This behavior ensures:
- **Low power consumption**
- **Full voltage swing**
- **High noise immunity**



## Objectives

- Design schematic of a CMOS inverter in Virtuoso
- Generate symbol for reuse
- Create a testbench for simulation
- Perform DC and transient analysis
- Analyze output waveform behavior



## Tools & Technologies

| Tool | Purpose |
|------|---------|
| Cadence Virtuoso | Schematic Entry, Simulation |
| Spectre Simulator | DC & Transient Analysis |
| GPDK090 | 90nm Technology Node |

---

## Design Specifications

| Parameter | Value |
|----------|-------|
| Technology Node | 90nm (GPDK090) |
| Supply Voltage | 1.8V |
| Input Source | VPULSE |
| Output | VOUT (inverted waveform) |
| Simulations | DC Sweep & Transient |

## Project Images

### CMOS Inverter Schematic

This is the core schematic showing the PMOS and NMOS transistors connected to form a CMOS inverter.

![Inverter Schematic](https://github.com/DakshaaSreerama/CMOS-Inverter-Cadence/blob/main/inverter_schematic.PNG?raw=true)

---

### CMOS Inverter Symbol

The symbol view was auto-generated from the schematic to allow easy reuse in other designs or testbenches.

![Inverter Symbol](https://github.com/DakshaaSreerama/CMOS-Inverter-Cadence/blob/main/inverter_symbol.PNG?raw=true)

---

### Testbench Schematic

The testbench uses a `vpulse` source to drive the inverter input and a `vdc` for power supply. The output is observed using simulation tools.

![Inverter Testbench](https://github.com/DakshaaSreerama/CMOS-Inverter-Cadence/blob/main/inverter_testbench.PNG?raw=true)

---

### Transient Simulation Result

The waveform below shows how the inverter reacts to a square wave input, confirming its switching behavior.

![Transient Simulation](https://github.com/DakshaaSreerama/CMOS-Inverter-Cadence/blob/main/trans_resp.PNG?raw=true)

---

### DC Analysis Result

DC sweep analysis of input voltage vs. output voltage reveals the inverter's voltage transfer characteristics.

![DC Sweep Analysis](https://github.com/DakshaaSreerama/CMOS-Inverter-Cadence/blob/main/dc_resp.PNG?raw=true)


##  Steps Followed

1. **Create New Library** (Attached to GPDK090)
2. **Design Schematic**: PMOS and NMOS connected to common gate & drain
3. **Add Pins**: VIN, VOUT, VDD, GND
4. **Generate Symbol** from Schematic
5. **Create Testbench**: Instantiate inverter, add VPULSE & VDC sources
6. **Set Simulation Parameters**: VPULSE (0–1.8V), Period = 20ns
7. **Launch ADE**: Set up Spectre, select DC & Transient analysis
8. **Plot VIN & VOUT**, run simulation
9. **View Results**: Check logic switching behavior
10. **Export Plots** for documentation/report



## Results

- **DC Analysis** shows transfer characteristics of the inverter.
- **Transient Analysis** confirms logic inversion and switching behavior.
- Output swings rail-to-rail (0V to 1.8V), verifying proper CMOS operation.



## Future Work

- Extend design to **NAND, NOR, XOR** gates
- Implement **full-custom layout** and perform **DRC/LVS**
- Analyze **propagation delay**, power consumption, and noise margins



## References

- *Cadence Virtuoso User Guide*
- *CMOS VLSI Design* – Weste & Harris
- *GPDK090 Technology Library Documentation*

  ------------------------------------------------**THANK YOU**--------------------------------------------------------------



