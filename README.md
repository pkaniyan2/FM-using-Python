# FM-using-Python

## Aim
To implement and analyze frequency modulation (FM) using Python's NumPy and Matplotlib libraries. 

## Apparatus Required

1.	Software: Python with NumPy and Matplotlib libraries
2.	Hardware: Personal Computer
  
## Theory

Frequency Modulation (FM) is a method of transmitting information over a carrier wave by varying its frequency in accordance with the amplitude of the input signal (message signal). The frequency of the carrier wave is varied according to the instantaneous amplitude of the message signal. The general form of an FM signal is:

## Algorithm


1.	Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and frequency deviation.
2.	Generate Time Axis: Create a time vector for the signal duration.
3.	Generate Message Signal: Define the message signal as a cosine wave.
4.	Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
5.	Generate FM Signal: Apply the FM modulation formula to obtain the modulated signal.
6.	Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

## Program

import numpy as np
import matplotlib.pyplot as plt
Am=4
fm=346
fs=34600
Ac=8
fc=3460
t=np.arange(0,2/fm,1/fs)
B=4.1
m=Am*np.cos(2*np.pi*fm*t)
plt.subplot(3,1,1)
plt.plot(t,m)
c=Ac*np.cos(2*np.pi*fc*t)
plt.subplot(3,1,2)
plt.plot(t,c)
s=Ac*np.cos((2*np.pi*fc*t)+B*np.sin(2*np.pi*fm*t))
plt.subplot(3,1,3)
plt.plot(t,s)
plt.tight_layout()
plt.show()

## Output Waveform
<img width="803" height="601" alt="image" src="https://github.com/user-attachments/assets/1c84cc51-6075-4575-95ad-2c20f98ad7c6" />

## Tabular Column
![WhatsApp Image 2025-12-05 at 02 34 01_ae65524d](https://github.com/user-attachments/assets/af860b4f-0692-4385-adda-024dcf0abd1e)


## Calculation
<img width="940" height="355" alt="image" src="https://github.com/user-attachments/assets/c5e53556-e0b2-4156-8a72-21c35fea5300" />

## Result
The message signal, carrier signal, and frequency modulated (FM) signal will be displayed in separate plots. The modulated signal will show frequency variations corresponding to the amplitude of the message signal.
