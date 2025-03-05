# Modular Power Supply - V1

## Overview
This modular power supply circuit provides selectable fixed and adjustable voltage outputs using LM2596 regulators. It integrates a 555 timer-based pulse generator and supports multiple operational modes via switchable configurations. The design includes high-side switching for improved isolation and safety.

![alt text](https://github.com/ashish-h1080/modular-psu/blob/main/img/sch.png)



## Features
1. **Switchable Voltage Outputs:**
  - Fixed 5V regulated output (LM2596-5V)
  - Adjustable output up to 12V (LM2596-ADJ)

2. **High-Side DPDT Switching:**
  - Ensures proper isolation when switching between voltage sources
 
3. **Integrated Pulse Generator:**
  - 555 timer-based circuit generates clock pulses
  - Selectable frequency via capacitor switching

## Implementation
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
![alt text](https://github.com/ashish-h1080/modular-psu/blob/main/img/pcbren.png)
![alt text](https://github.com/ashish-h1080/modular-psu/blob/main/img/3dmod.png)

## Future Iterations
- **Onboard voltage meter**
- **Additional signal processing circuits (e.g., sine wave generator, filters, amplifiers)**
- **Microcontroller-based control for automated switching and monitoring**
