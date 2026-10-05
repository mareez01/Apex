# Project Apex: Mixed-Signal Diagnostic Instrument

Hardware design, manufacturing files, and system architecture for Project Apex, a multi-functional diagnostic edge-computing tool

**Demonstration:**
*   Watch the hardware demo here: https://drive.google.com/drive/folders/1B4_CrYPebX7i6lBTUv4ibxBGYRtsgXC7?usp=sharing

## Version 1.0 (Current Files)
*   **Architecture:** Dual-MCU system featuring an ESP32 master and ATmega328P co-processor.
*   **PCB:** Custom 4-layer stackup engineered to ensure signal integrity by isolating the 3.3V digital logic from the 5V analog domains[cite: 1].
*   **Analog Front-End:** Auto-ranging 12-bit impedance analyzer utilizing an AD9833 waveform generator, MCP6022 PGA, and MCP3208 ADC over an isolated SPI bus.
*   **Digital IC Tester:** 16-pin ZIF socket routed via a discrete 1P3T mechanical switch matrix for deterministic fault injection and truth-table validation.
*   **Project reports are listed:** The Final version 1 project report have been submitted with all the ECAD files and GERBER files.


## Version 2.0 Roadmap (In Development)
Transitioning to a fully autonomous, solid-state architecture to support 24MSPS logic analysis and frequency response plotting (Bode/Nyquist).
*   **Master MCU:** Upgrading to STM32H723 (550MHz) utilizing DMA for high-speed ADC polling and 16-channel logic analysis.
*   **Slave MCU:** Upgrading to AVR32DB48. Utilizes native Multi-Voltage I/O (MVIO) on Port C to eliminate external level shifters. Includes dedicated 12-bit ADC channels for absolute floating-gate fault detection.
*   **Solid-State Matrix:** Replacing mechanical relays with an AO4606/SI1539CDL MOSFET crossbar switching matrix for automated IC power routing.
*   **PC Interface:** Transitioning from serial prints to a Python/PySide6 desktop GUI utilizing pySerial for live PyQtGraph data visualization.
*   **Design Files** So we are actively wroking on the version 2 deisgn and the design documention file is listed here please use iitm mail id to view the G-sheets :https://docs.google.com/document/d/17MV_ibkEd-tFQ1U5sWTHGYrbQkPEoYyiVjMqvgrKTJg/edit?usp=sharing
