# Sonar Imaging System 
#### EEE3097S DESIGN

##### The aim of this project is to design, build and test an imaging sonar operating at 40 kHz in air.

#### This project split into milestones
	
1. Create Documentation for user requirements, design calculations, sequence diagrams, activity diagrams, etc. 
2. Simulate a 1-D chirp pulse transmission and reception 
3. Build and test 1-D sonar
4. Simulate 2-D sonar with fan beam image
5. Build and test 2-D sonar imaging sysem.

#### File Descriptions:
 - chirp_gen.ipynb used to generate array of values in chirp (int values pre-adjusted for DAC) 
 - globals.h contains chirp array
 - Chirp_Output.ino produces chirp using teensy 3.6 DAC0. 
 - LibSerialPort.ipynb to receive buffer from Teensy through serial port
 - Sampling.ino samples using ADC on teensy.

#### 1D imaging Sonar: 
one transmitter and one receiving transducer.

#### 2D imaging sonar: 
requires that a narrow beam is steered over a range of
angles to form a fan-beam image. Steering can be implemented
electronically by using a linear array of transducers, either for the
transmitter beam or the receiver beam. By combining the received signals
with appropriate delays, beam steering can be achieved. 


#### 3D imaging sonar: 
can be implemented in different ways. A simple method
is to use two perpendicular arrays, one for steering a transmit beam, and the
other for steering a receive beam. This achieves 3D imaging with a
minimum number of channels (compared to a conventional NxN receiving
array).

### Some Theory

#### Simple 1D pulse-echo sonar
![image1](/Images/Image1.png)

#### Matched filtering of received signal 
Radar/sonar transmits a chirp pulse (wide bandwidth for fine resolution; long in
duration for high energy. Received signal is passed through a matched filter.
Output waveform has improved peak SNR. Below is shown a simulation of one
echo.
![image2](/Images/Image2.png)

#### 2D/3D Sonar Imaging System operating at 40 kHz
![image3](/Imagees/Image3.png)


### Received Waveforms on oscilloscope when testing 1-D sonar


![image1](/Images/scope_0.png)
![image2](/Images/scope_1.png)
![image3](/Imagees/scope_2.png)
![image1](/Images/scope_3.png)
![image2](/Images/scope_4.png)
![image3](/Imagees/scope_5.png)
![image1](/Images/scope_6.png)
![image2](/Images/scope_7.png)
