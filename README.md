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

1 - Audio is preamplified to 0-5v and biased at 2.5v

2 - Audio channels are multiplexed

3 - Audio signal is converted to 8-bit using an ADC

Parallel port signals used to control the process are:
- /STROBE: Amiga ask for the next sample 
- /SELECT: Select the current channel for sample (0=Left, 1= Right)
## PCB
![image](https://user-images.githubusercontent.com/18539931/232578970-ba53bcfb-2755-417a-baea-773ec0bc1436.png)
![image](https://user-images.githubusercontent.com/18539931/232579062-5ad23c21-5285-4d03-8580-92c7db3a8c98.png)
## Bill of materials
