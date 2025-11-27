# DSBSC-using-python
AIM:
To implement and analyze DOUBLE SIDE BAND SUPPRESSED CARRIER (DSBSC) using Python's NumPy and Matplotlib libraries.

EQUIPMENTS REQUIRED
•personal computer . software: python with numpy and mathplotlib libraries

THEORY:
Double Sideband Suppressed Carrier (DSB-SC) is an amplitude modulation technique where the carrier signal is completely suppressed, and only the sidebands containing the message information are transmitted. It is more power-efficient than standard AM but requires a synchronized carrier at the receiver for proper demodulation.

PROCEDURE
Initialize Parameters: Set the values for message amplitude, carrier amplitude, message frequency, carrier frequency, and sampling frequency.

Generate Time Axis: Create a time vector for the duration of the signal.

Generate Message Signal: Define the message signal as a cosine wave.

Generate Carrier Signal: Define the carrier signal as a cosine wave with a higher frequency.

Generate DSB-SC Signal: Multiply the message signal and carrier signal to produce the Double Sideband Suppressed Carrier (DSB-SC) modulated signal.

Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and the DSB-SC modulated signal.

Program:
import numpy as np
import matplotlib.pyplot as plt

Am=3.5
Fm=307
Ac=7.0
Fs=30700
Fc=3070

t=np.arange(0,2/Fm,1/Fs)

m=Am*np.cos(2*np.pi*Fm*t)
plt.subplot(3,1,1)
plt.plot(t,m)
c=Ac*np.cos(2*np.pi*Fc*t)
plt.subplot(3,1,2)
plt.plot(t,c)
s1 = (Ac + m) * np.cos(2 * np.pi * Fc * t)
s2=(Ac-m)*np.cos(2*np.pi*Fc*t)
s=s1-s2
plt.subplot(3,1,3)
plt.plot(t,s)

Output Waveform

![WhatsApp Image 2025-11-12 at 21 20 00_e9114c32](https://github.com/user-attachments/assets/388eb915-1d77-4f11-8d57-efffb3b04191)


Tabulation :

![WhatsApp Image 2025-11-27 at 18 41 19_7058af66](https://github.com/user-attachments/assets/5634b274-7276-43a2-8fd3-9e31fc42f9b9)

RESULT:

The DSB-SC modulated signal was successfully generated. The output shows suppression of the carrier, with only the sidebands carrying the message information clearly visible in the waveform.
