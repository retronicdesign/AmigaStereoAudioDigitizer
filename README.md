# Amiga Stereo Audio Digitizer v1.3
An Amiga Stereo Digitizer for Audio. Compatible with most softwares. Input gain is adjustable.
![image](https://github.com/user-attachments/assets/a72174fe-128a-45c5-bd57-e1ef4f07df78)
## Schematic
![image](https://github.com/user-attachments/assets/7293b0cb-0490-4af3-a189-06760a76e585)

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
![image](https://github.com/user-attachments/assets/698d8d60-3f34-4ccf-8395-4a5957ee3a44)
![image](https://github.com/user-attachments/assets/4bfc23e6-7b73-4492-9b96-77edfe42d33a)

## Bill of materials
| Reference | Quantity | Value | Component | Description | Vendor |
| --- | --- | --- | --- | --- | --- |
| C1, C2, C3,  | 3 | 10uF 10v 10% | Electrolytic, Radial |
| C4, C5, C6,  | 3 | 100nF 50v 10% | Ceramic |
| C7,  | 1 | 47uF 10v 10% | Electrolytic, Radial |
| J1,  | 1 |  | PJRAN1X1U03X | RCA female connector, Red | Switchcraft |
| J2,  | 1 |  | PJRAN1X1U02X | RCA female connector, White |  Switchcraft |
| J3,  | 1 |  | 25-pin male D-SUB connector | PCB, Right-Angle |
| R1, R2, R3, R4,  | 4 | 1K 1% 1/4 Watts | Resistor | Trough hole resistor |
| RV1,  | 1 | A10K | RK09K1110A0J |  Single right-angle potentiometer, 10K Exponential | ALPS |
| U1,  | 1 | | MCP6002 | 1MHz, Low-Power Op Amp, DIP-8 | Microchip |
| U2,  | 1 | | DG419DJ | Single SPDT 3V Logic Compatible CMOS Analog Switch, DIP-8 | Vishay Siliconix |
| U3,  | 1 | | ADC0820CCN+ | Analog to Digital 8 bits converter, DIP-20 | Texas Instruments |
## Revision information
- 1.0 Original release
- 1.1 Modified D-Sub 25M connector footprint
- 1.2 Modified RCA connector footprint
- 1.3 Redesigned bias for more stable reference and simplified op-amp circuitry + PCB redesign

