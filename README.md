# Modular Power Supply - V1
This modular power supply circuit provides selectable fixed and adjustable voltage outputs using LM2596 regulators. It integrates a 555 timer-based pulse generator and supports multiple operational modes via switchable configurations. The design includes high-side switching for improved isolation and safety.





## Features
This modular power supply system offers a range of features designed for flexibility and reliability. It provides switchable voltage outputs, including a fixed 5V regulated supply using the LM2596-5V and an adjustable output of up to 12V via the LM2596-ADJ, controlled by a potentiometer. To ensure proper isolation and seamless switching between these voltage sources, a high-side DPDT switch is integrated into the design. Additionally, the system includes an integrated pulse generator, utilizing a 555 timer circuit to produce clock pulses. The pulse frequency can be adjusted by selecting different capacitors, making the system adaptable for various applications requiring precise timing signals.

## Implementation
The modular power supply system is designed for versatility and stability, incorporating key components for power input, regulation, filtering, and additional functionalities. A DC power jack (J1) serves as the main input source, while a DPDT switch (SW2) allows seamless selection between a fixed and an adjustable voltage regulator. The LM2596-5V (U1) ensures a stable 5V output, whereas the LM2596-ADJ (U2), controlled via a 10k potentiometer (RV1), provides a user-defined adjustable voltage. To enhance performance, capacitors (C1-C8) and inductors (L1, L2) are implemented for stability and noise reduction, while Schottky diodes (D1, D2) safeguard the system against reverse voltage. Additionally, a 555 timer (U3) functions as a pulse generator, with its frequency adjustable through capacitors (TC1-TC4) and resistors (RT1, RT2). The generated clock pulses are accessible via a single-pin connector (J3), offering expanded utility for various applications. Finally, a 4 pin terminal block (J2) efficiently distributes power and ground, ensuring easy connectivity for external circuits.
     
![alt text](https://github.com/ashish-h1080/modular-power-supply-v1/blob/main/img/lay.png)
![alt text](https://github.com/ashish-h1080/modular-power-supply-v1/blob/main/img/pcbren.png)
![alt text](https://github.com/ashish-h1080/modular-power-supply-v1/blob/main/img/3dmod.png)
## Future Iterations
- **Onboard voltage meter**
- **Additional signal processing circuits (e.g., sine wave generator, filters, amplifiers)**
- **Microcontroller-based control for automated switching and monitoring**
