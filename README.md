# Amiga Stereo Audio Digitizer v1.3a
An Amiga Stereo Digitizer for Audio. Compatible with most softwares. Input gain is adjustable.
<img width="692" height="753" alt="image" src="https://github.com/user-attachments/assets/582bbd2e-bd3e-46ee-b6a5-00f5d0039a7d" />
## Schematic
<img width="3300" height="2550" alt="image" src="https://github.com/user-attachments/assets/294d2f8d-ceff-4d4b-a7c8-4555f9f9cf94" />

## Theory of Operation
This board can convert one or two audio channel to uncompressed digital 8-bit audio stream.  
It connects to the Amiga Parallel Port through a D-SUB-25 male connector. 
It was sucessfully tested with Audio Master IV at a maximum rate of 53KSPS (mono) on an unmodified Amiga 500.

Audio processing on the board is as follow:

1. Audio is preamplified to +5v p-p and biased at +2.5v
2. Left and right channels are multiplexed and sampled alternatively
3. Audio signal is converted to 8-bit using an high-speed ADC

Parallel port signals used to control the process are:
- /STROBE: Amiga ask for the next sample 
- /SELECT: Select the current channel for sample (0=Left, 1= Right)
## PCB
<img width="715" height="678" alt="image" src="https://github.com/user-attachments/assets/46d5b16d-fbcd-4b0e-bd69-e085d4397c02" />
<img width="713" height="678" alt="image" src="https://github.com/user-attachments/assets/8cd7f13d-56bd-48e0-9a9f-0421a3befb1c" />

## Bill of materials
| Reference | Quantity | Value | Component | Description | Vendor |
| --- | --- | --- | --- | --- | --- |
| C1, C2, C3,  | 3 | 10uF 10v 10% | Electrolytic, Radial |
| C4, C5, C6,  | 3 | 100nF 50v 10% | Ceramic |
| C7,  | 1 | 47uF 10v 10% | Electrolytic, Radial |
| J1,  | 1 |  | PJRAN1X1U03X | RCA female connector, Red | Switchcraft |
| J2,  | 1 |  | PJRAN1X1U02X | RCA female connector, White |  Switchcraft |
| J3,  | 1 |  | DB25-SL-24 | PCB D-SUB 25 male, Right-Angle | Adam Tech |
| R1, R2, R3, R4,  | 4 | 1K 1% 1/4 Watts | Resistor | Trough hole resistor |
| RV1,  | 1 | A10K | RK09K1110A0J |  Single right-angle potentiometer, 10K Exponential | ALPS |
| U1,  | 1 | | MCP6002 | 1MHz, Low-Power Op Amp, DIP-8 | Microchip |
| U2,  | 1 | | ADG419BNZ | Single SPDT CMOS Analog Switch, DIP-8 | Analog Devices |
| U3,  | 1 | | ADC0820CCN+ | Analog to Digital 8 bits converter, DIP-20 | Texas Instruments |
## Revision information
- 1.0 Original release
- 1.1 Modified D-Sub 25M connector footprint
- 1.2 Modified RCA connector footprint
- 1.3 Redesigned bias for more stable reference and simplified op-amp circuitry + PCB redesign
- 1.3a Corrected routing from v1.3 + replaced SPDT Analog Switch for new part

