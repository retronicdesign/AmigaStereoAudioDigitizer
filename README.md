# Amiga Stereo Audio Digitizer v1.3b
An Amiga Stereo Digitizer for Audio. Compatible with most softwares. Input gain is adjustable.
<img width="770" height="792" alt="image" src="https://github.com/user-attachments/assets/ef5da569-69dc-4cef-be02-ffbe46bebeb6" />
## Schematic
<img width="3300" height="2550" alt="image" src="https://github.com/user-attachments/assets/59db09b5-b770-4921-96d4-85b148359052" />

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
<img width="871" height="754" alt="image" src="https://github.com/user-attachments/assets/edfca3d5-3eda-4f31-9621-18b9cea93274" />
<img width="873" height="728" alt="image" src="https://github.com/user-attachments/assets/ecd93537-59cf-4563-96f1-5a4a8680a204" />

## Bill of materials
| Reference | Quantity | Value | Component | Description | Vendor |
| --- | --- | --- | --- | --- | --- |
| C1, C2, C3,  | 3 | 10uF 10v 10% | Electrolytic, Radial |
| C4, C5, C6,  | 3 | 100nF 50v 10% | Ceramic |
| C7,  | 1 | 47uF 10v 10% | Electrolytic, Radial |
| J1,  | 1 |  | SJ1-3525NG-PI | Stereo jack female connector, Red | Same Sky |
| J2,  | 1 |  | DB25-SL-24 | PCB D-SUB 25 male, Right-Angle | Adam Tech |
| R1, R2, R3, R4,  | 4 | 1K 1% 1/4 Watts | Resistor | Trough hole resistor |
| RV1,  | 1 | A10K | RK09K1110A0J |  Single right-angle potentiometer, 10K Exponential | ALPS |
| U1,  | 1 | | MCP6002 | 1MHz, Low-Power Op Amp, DIP-8 | Microchip |
| U2,  | 1 | | ADG419BNZ | Single SPDT CMOS Analog Switch, DIP-8 | Analog Devices |
| U3,  | 1 | | ADC0820CCN+ | Analog to Digital 8 bits converter, DIP-20 | National Semiconductors |
## Revision information
- 1.0 Original release
- 1.1 Modified D-Sub 25M connector footprint
- 1.2 Modified RCA connector footprint
- 1.3 Redesigned bias for more stable reference and simplified op-amp circuitry + PCB redesign
- 1.3a Corrected routing from v1.3 (issue#2) + replaced SPDT Analog Switch for new part
- 1.3b Corrected routing from v1.3a (issue#3) + replaced RCA plugs for Setero jack 3.5mm

