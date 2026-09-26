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
Am=2.15;
fm=447;
Ac=3.7625;
fc=4470;
fs=44700;
b=3.02;
kp=3.02;
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

<img width="743" height="597" alt="Screenshot 2026-08-28 155151" src="https://github.com/user-attachments/assets/b30e447c-0543-4756-a604-2fb267414fe9" />


# TABULATION

<img width="720" height="1600" alt="image" src="https://github.com/user-attachments/assets/181eef78-5e3a-4ad7-b42b-13d4532f3ea9" />



# RESULT

The message signal, carrier signal, and phase-modulated (PM) signal will be displayed in separate plots. The modulated signal will show phase variations corresponding to the amplitude of the message signal.
