# Amiga Stereo Digitizer v1.1
An Amiga Stereo Digitizer for Audio. Compatible with most softwares. Input volume is adjustable.
![image](https://user-images.githubusercontent.com/18539931/232578439-98e58c09-3f3d-41c6-abcd-1fefc3d42a47.png)
## Schematic
![image](https://user-images.githubusercontent.com/18539931/232578802-d9e64a61-ccab-48a6-8866-7c32fd6352ec.png)

## Theory of Operation
This board can convert one or two audio channel to uncompressed digital 8-bit audio stream.  
It connects to the Amiga Parallel Port through a D-SUB-25 male connector. 
It was sucessfully tested with Audio Master IV at a maximum rate of 53KSPS (mono) on an unmodified Amiga 500.

Audio processing on the board is as follow:

1. Audio is preamplified to 0-5v and biased at 2.5v
2. Audio channels are multiplexed
3. Audio signal is converted to 8-bit using an ADC

Parallel port signals used to control the process are:
- /STROBE: Amiga ask for the next sample 
- /SELECT: Select the current channel for sample (0=Left, 1= Right)
## PCB
![image](https://user-images.githubusercontent.com/18539931/232578970-ba53bcfb-2755-417a-baea-773ec0bc1436.png)
![image](https://user-images.githubusercontent.com/18539931/232579062-5ad23c21-5285-4d03-8580-92c7db3a8c98.png)
## Bill of materials
| Reference | Quantity | Value | Component | Description | Vendor |
| --- | --- | --- | --- | --- | --- |
| C1, C2, C7, C8,  | 4 | 10uF 10v 10% | Electrolytic, Radial |
| C3, C4, C5,  | 3 | 100nF 50v 10% | Ceramic |
| C6,  | 1 | 47uF 10v 10% | Electrolytic, Radial |
| J1,  | 1 |  | RCA Connector | Red |  
| J2,  | 1 |  | RCA Connector | White |  
| J3,  | 1 |  | 25-pin male D-SUB connector | 
| R1, R2, R3, R4, R5, R6  | 6 | 1K | Resistor |  
| RV1,  | 1 | 10K Exponential | RK09L Horizontal Double|  Dual potentiometer, 10K Exponential | ALPS |
| U1,  | 1 | | MCP6002 | 1MHz, Low-Power Op Amp, DIP-8 | Microchip |
| U2,  | 1 | | DG419DJ | Single SPDT 3V Logic Compatible CMOS Analog Switch, 35Ohm Ron, with Vlogic, DIP-8 | Vishay Siliconix |
| U3,  | 1 | | ADC0820CCN+ | Analog to Digital 8 bits converter, DIP-20 | Texas Instruments |


