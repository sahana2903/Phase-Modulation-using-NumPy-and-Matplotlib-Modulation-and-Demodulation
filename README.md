# Phase-Modulation-using-NumPy-and-Matplotlib-Modulation-and-Demodulation

__Aim__:

To implement and analyze phase modulation (PM) using Python's NumPy and Matplotlib libraries. 


__Apparatus Required__:

1. Software: Python with NumPy and Matplotlib libraries
   
2. Hardware: Personal Computer
   
__Theory__:

Phase Modulation (PM) is a technique where the phase of the carrier wave is varied in proportion to the 
instantaneous amplitude of the input signal (message signal). Unlike frequency modulation, where the frequency 
is varied, in phase modulation, the phase angle of the carrier wave changes with the amplitude of the message 
signal. 


The general form of a PM signal can be represented as:

<img width="483" height="254" alt="image" src="https://github.com/user-attachments/assets/8d5a2e54-cf93-4ff0-b0a6-e2000e078682" />






__Algorithm__: 

1. Initialize Parameters:
   
o Set values for carrier amplitude (Ac), carrier frequency (fc), message frequency
 
(fm), sampling frequency, and phase deviation sensitivity (kp). 

2. Generate Time Axis: 

o Create a time vector for the signal duration based on the sampling frequency. 

3. Generate Message Signal: 

o Define the message signal as a cosine wave. 

4. Generate PM Signal:
 
o Apply the PM modulation formula to obtain the modulated signal.

5. Plot the Signals:
 
o Use Matplotlib to plot the message signal, carrier signal, and phase-modulated signal.

# PROGRAM :
```
import numpy as np 
import matplotlib.pyplot as plt 
Ac = 2 
fc = 7000 
Am = 5 
fm = 800 
fs = 8000 
t = np.arange(0, 2/fm, 1/fs) 
Wm = 2 * np.pi * fm 
Wc = 2 * np.pi * fc 
Em = Am * np.sin(Wm * t) 
Ec = Ac * np.sin(Wc * t) 
Edsbsc = ((Am / 2) * np.cos((Wc - Wm) * t)) - ((Am / 2) * np.cos((Wc + Wm) * t)) 
plt.figure(figsize=(10, 6)) 
plt.subplot(3, 1, 1) 
plt.plot(t, Em) 
plt.grid() 
plt.subplot(3, 1, 2) 
plt.plot(t, Ec) 
plt.grid() 
plt.subplot(3, 1, 3) 
plt.plot(t, Edsbsc) 
plt.grid() 
plt.tight_layout() 
plt.show()
```
# TABULATION :
<img width="1040" height="1094" alt="image" src="https://github.com/user-attachments/assets/9c324a2f-f172-4065-98af-7877bd37e3b3" />

# CALCULATION :
<img width="955" height="1280" alt="image" src="https://github.com/user-attachments/assets/0832dca8-5001-443e-b776-ac048be556cc" />

# Output :
<img width="645" height="488" alt="image" src="https://github.com/user-attachments/assets/38aeff15-cb47-421f-89a1-c09c758f55d0" />

# Result :
The message signal, carrier signal, and phase-modulated (PM) signal will be displayed in separate plots. The modulated signal will show phase variations corresponding to the amplitude of the message signal. 





