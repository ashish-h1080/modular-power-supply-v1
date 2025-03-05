# Modular Power Supply (Version 1)

This modular power supply circuit provides selectable fixed and adjustable voltage outputs using LM2596 regulators. It integrates a 555 timer-based pulse generator and supports multiple operational modes via switchable configurations. The design includes high-side switching for improved isolation and safety.

![alt text](https://github.com/ashish-h1080/modular-psu/blob/main/img/sch.png)
![alt text](https://github.com/ashish-h1080/modular-psu/blob/main/img/lay.png)

## Features
- **Switchable Voltage Outputs (with high side switching):**
  - Fixed 5V regulated output (LM2596-5V)
  - Adjustable output up to 12V (LM2596-ADJ)
  - DPDT switch for selecting between the two regulators

- **Integrated Pulse Generator:**
  - 555 timer-based circuit generates clock pulses
  - Selectable frequency via capacitor switching
- **Robust Filtering & Regulation:**
  - Input and output capacitors for stability
  - Schottky diodes for reverse current protection
  - Inductor-based switching regulation for efficiency

## Implementation Details
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
   - A 5-pin output header (J2) distributes power.
   - A single pin output header (J3) provides clock signal.


## Future Enhancements
- **Onboard voltage meter (without ADC-based implementation)**
- **Additional signal processing circuits (e.g., sine wave generator, filters, amplifiers)**
- **Microcontroller-based control for automated switching and monitoring**
