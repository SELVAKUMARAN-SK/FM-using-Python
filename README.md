# FM-using-Python

Aim


To implement and analyze frequency modulation (FM) using Python's NumPy and Matplotlib libraries. 

Apparatus Required

1.	Software: Python with NumPy and Matplotlib libraries
2.	Hardware: Personal Computer
  
Theory

Frequency Modulation (FM) is a method of transmitting information over a carrier wave by varying its frequency in accordance with the amplitude of the input signal (message signal). The frequency of the carrier wave is varied according to the instantaneous amplitude of the message signal. The general form of an FM signal is:



Algorithm


1.	Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and frequency deviation.
2.	Generate Time Axis: Create a time vector for the signal duration.
3.	Generate Message Signal: Define the message signal as a cosine wave.
4.	Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
5.	Generate FM Signal: Apply the FM modulation formula to obtain the modulated signal.
6.	Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

Program
import matplotlib.pyplot as plt
Am = 3.5
fm = 244
Ac = 6.10
fc = 2440
fs = 24400
B = 2.7
t = np.arange(0, 2/fm, 1/fs)
m = Am * np.cos(2 * np.pi * fm * t)
c = Ac * np.cos(2 * np.pi * fc * t)
efm = Ac * np.cos((2 * np.pi * fc * t) + (B * np.sin(2 * np.pi * fm * t)))
plt.figure(figsize=(10, 8))
plt.subplot(3, 1, 1)
plt.plot(t, m)
plt.subplot(3, 1, 2)
plt.plot(t, c)
plt.subplot(3, 1, 3)
plt.plot(t, efm)
plt.tight_layout()
plt.show()

Output Waveform
<img width="1102" height="564" alt="Screenshot 2025-10-23 193153" src="https://github.com/user-attachments/assets/5a1c6612-e0d5-4a88-9eb6-3ef92b17f8cb" />
<img width="1052" height="281" alt="Screenshot 2025-10-23 193204" src="https://github.com/user-attachments/assets/afb9cb96-43d5-4a22-8ce3-227e5cb46464" />-

Tabular Column
![WhatsApp Image 2025-12-04 at 12 02 50 PM](https://github.com/user-attachments/assets/d1128fc1-9404-40f5-a83b-d9e4c426d775)



Calculation
![WhatsApp Image 2025-11-28 at 8 50 33 AM](https://github.com/user-attachments/assets/2f5334a0-01b4-407d-8598-a0fd96e0235e)




Result


The message signal, carrier signal, and frequency modulated (FM) signal will be displayed in separate plots. The modulated signal will show frequency variations corresponding to the amplitude of the message signal.
