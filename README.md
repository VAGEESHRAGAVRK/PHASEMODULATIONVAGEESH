EXPT.NO.8	Phase Modulation

Aim

To implement and analyze phase modulation (PM) using Sci lab 
 Apparatus Required
1.	Software: Python with NumPy and Matplotlib libraries
2.	Hardware: Personal Computer Theory
Phase Modulation (PM) is a technique where the phase of the carrier wave is varied in proportion to the instantaneous amplitude of the input signal (message signal). Unlike frequency modulation, where the frequency is varied, in phase modulation, the phase angle of the carrier wave changes with the amplitude of the message signal.

The general form of a PM signal can be represented as:


Algorithm

1.	Initialize Parameters:
o	Set values for carrier amplitude (AcA_cAc), carrier frequency (fcf_cfc), message frequency (fmf_mfm), sampling frequency, and phase deviation sensitivity (kpk_pkp).
2.	Generate Time Axis:
o	Create a time vector for the signal duration based on the sampling frequency.
3.	Generate Message Signal:
o	Define the message signal as a cosine wave.
4.	Generate PM Signal:
o	Apply the PM modulation formula to obtain the modulated signal.
5.	Plot the Signals:
o	Use Matplotlib to plot the message signal, carrier signal, and phase-modulated signal.
CODE
am=7.2;

fm=465;

ac=14.2;

fc=4650;

fs=46500;

t=0:1/fs:3/fm;

b=4.7;

em=am*cos(2*3.14*fm*t);

subplot(4,1,1);

plot(t,em);

ec=ac*cos(2*3.14*fc*t);

subplot(4,1,2);

plot(t,ec);

efm = ac * cos((2*3.14*fc*t) + b * sin(2*3.14*fm*t));

subplot(4,1,3);

plot(t,efm);

epm= ac * cos((2*3.14*fc*t) + b * cos(2*3.14*fm*t));

subplot(4,1,4);

plot(t,epm);
OUTPUT 
<img width="960" height="1280" alt="image" src="https://github.com/user-attachments/assets/e76930ca-0266-47da-8988-3d16dc297179" />
<img width="1909" height="776" alt="image" src="https://github.com/user-attachments/assets/daf16adb-ed01-4eb9-8bb2-981b43e19a62" />


 
Result

The message signal, carrier signal, and phase-modulated (PM) signal will be displayed in separate plots. The modulated signal will show phase variations corresponding to the amplitude of the message signal.
