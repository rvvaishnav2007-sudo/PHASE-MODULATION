# PHASE-MODULATION


# AIM

To implement and analyze phase modulation (PM) using Python's NumPy and Matplotlib libraries. 
# Apparatus Required

. Software: Python with NumPy and Matplotlib libraries
. Hardware: Personal Computer 

# Theory

Phase Modulation (PM) is a technique where the phase of the carrier wave is varied in proportion to the instantaneous amplitude of the input signal (message signal). Unlike frequency modulation, where the frequency is varied, in phase modulation, the phase angle of the carrier wave changes with the amplitude of the message signal.

# Algorithm

1. Initialize Parameters:
Set values for carrier amplitude (AcA_cAc), carrier frequency (fcf_cfc), message frequency (fmf_mfm), sampling frequency, and phase deviation sensitivity (kpk_pkp).
2. Generate Time Axis:
Create a time vector for the signal duration based on the sampling frequency.
3. Generate Message Signal:
Define the message signal as a cosine wave.
4. Generate PM Signal:
Apply the PM modulation formula to obtain the modulated signal.
5. Plot the Signals:
Use Matplotlib to plot the message signal, carrier signal, and phase-modulated signal.

# PROGRAM 
~~~
Am=3.35;
fm=623;
Ac=5.8625;
fc=6230;
fs=62300;
b=4.38;
kp=4.38;
t=0:1/fs:2/fm;
em=Am*cos(2*3.14*fm*t);
subplot(4,1,1);
plot(t,em);
ec=Ac*cos(2*3.14*fc*t);
subplot(4,1,2);
plot(t,ec);
efm=Ac*cos((2*3.14*fc*t)+(b*sin(2*3.14*fm*t)));
subplot(4,1,3);
plot(t,efm);
epm=Ac*cos((2*3.14*fc*t)+(kp*cos(2*3.14*fm*t)));
subplot(4,1,4);
plot(t,epm);
~~~
# OUTPUT WAVEFORM 

<img width="1078" height="926" alt="image" src="https://github.com/user-attachments/assets/54b4833a-f04c-433b-a71b-78d1890f2f27" />


# TABULATION

<img width="1600" height="946" alt="image" src="https://github.com/user-attachments/assets/a45302e6-c5b8-436a-8de0-c66694f64978" />

# RESULT

The message signal, carrier signal, and phase-modulated (PM) signal will be displayed in separate plots. The modulated signal will show phase variations corresponding to the amplitude of the message signal.
