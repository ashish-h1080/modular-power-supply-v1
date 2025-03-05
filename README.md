# Modular Power Supply with Pulse Generator

## Overview
This modular power supply circuit provides selectable fixed and adjustable voltage outputs using LM2596 regulators. It integrates a 555 timer-based pulse generator and supports multiple operational modes via switchable configurations. The design includes high-side switching for improved isolation and safety.

![alt text](https://github.com/ashish-h1080/modular-psu/blob/main/img/sch.png)

## Features
- **Switchable Voltage Outputs:**
  - Fixed 5V regulated output (LM2596-5V)
  - Adjustable output up to 12V (LM2596-ADJ)

- **High-Side DPDT Switching:**
  - Ensures proper isolation when switching between voltage sources
 
- **Integrated Pulse Generator:**
  - 555 timer-based circuit generates clock pulses
  - Selectable frequency via capacitor switching

## Circuit Breakdown
1. **Power Input and Switching:**
   - A DC power jack (J1) provides the main supply input.
   - A DPDT switch (SW2) selects between fixed and adjustable voltage regulators.
2. **Voltage Regulation:**
   - LM2596-5V (U1) provides a stable 5V output.
   - LM2596-ADJ (U2) allows user-defined voltage output via RV1 (10k potentiometer).
3. **Filtering & Protection:**
   - Capacitors (C1-C8) and inductors (L1, L2) enhance stability and noise reduction.
   - Schottky diodes (D1, D2) protect against reverse voltage.
4. **Pulse Generator:**
   - 555 timer (U3) generates clock pulses with frequency controlled by capacitors (TC1-TC4) and resistors (RT1, RT2).
   - Output is accessible through a single-pin connector (J3).
5. **Output Connections:**
   - A 5-pin output header (J2) distributes power and signals.

![alt text](https://github.com/ashish-h1080/modular-psu/blob/main/img/lay.png)
## Footprint Assignments
| Symbol | Component | Footprint |
|--------|------------|------------|
| C1, C3, C5, C7 | 220uF Capacitor | Radial_D8.0mm_P3.50mm |
| C2, C4, C6, C8 | 0.1uF Capacitor | SMD 0805 |
| D1, D2 | 1N5822 Schottky Diode | DO-201AD |
| D3 | 1N4148 Diode | DO-35 SOD27 |
| J1 | DC Jack | PJ-035DH |
| J2 | 5-Pin Header | PinHeader_1x05_P2.00mm |
| J3 | 1-Pin Header | PinHeader_1x01_P2.00mm |
| L1, L2 | 33uH Inductor | SRR1260-330M |
| R1 | 680Ω Resistor | Axial |
| R2 | 1kΩ Resistor | Axial |
| RT1, RT2 | 1.5kΩ Resistor | SMD 0805 |
| RV1 | 10kΩ Potentiometer | Piher PC-16 |
| SW1 | Rotary Switch | PEC12R-3x17F |
| SW2 | DPDT Switch | TL2230AF140 |
| TC1 | 470nF Capacitor | SMD 0805 |
| TC2 | 100nF Capacitor | SMD 0805 |
| TC3 | 47nF Capacitor | SMD 0805 |
| TC4 | 10nF Capacitor | SMD 0805 |
| U1 | LM2596-5V Regulator | TO-263-5 |
| U2 | LM2596-ADJ Regulator | TO-263-5 |
| U3 | NE555 Timer | DIP-8 |
![alt text](https://github.com/ashish-h1080/modular-psu/blob/main/img/pcbren.png)



![alt text](https://github.com/ashish-h1080/modular-psu/blob/main/img/3dmod.png)

## Future Enhancements
- **Onboard voltage meter**
- **Additional signal processing circuits (e.g., sine wave generator, filters, amplifiers)**
- **Microcontroller-based control for automated switching and monitoring**
