# -Frequency-Modulation-and-Demodulation-using-NumPy-and-Matplotlib-

__Aim:__

To implement and analyze frequency modulation (FM) using Python's NumPy and Matplotlib libraries.

__Apparatus Required:__ 

1. Software: Python with NumPy and Matplotlib libraries
   
2. Hardware: Personal Computer

 
__Theory:__

Frequency Modulation (FM) is a method of transmitting information over a carrier wave by varying its 
frequency in accordance with the amplitude of the input signal (message signal). The frequency of the carrier 
wave is varied according to the instantaneous amplitude of the message signal.

__Algorithm:__

1. Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and 
   frequency deviation.
   
2. Generate Time Axis: Create a time vector for the signal duration.
    
3. Generate Message Signal: Define the message signal as a cosine wave.
    
4. Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
    
5. Generate FM Signal: Apply the FM modulation formula to obtain the modulated signal.
 
6. Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

__Programme:__

// Parameters
Am = 16.1;        
Fm = 583;         
B  =  5.6;         
Ac = 32.2;          
Fc = 5830;       
Fs = 58300;       
T  = 0:1/Fs:2/Fm; 

// Message signal
em = Am * cos(2*%pi*Fm*T);
subplot(3,1,1);
plot(T, em);
xtitle("Message Signal");
xgrid();

// Carrier signal
ec = Ac * cos(2*%pi*Fc*T);
subplot(3,1,2);
plot(T, ec);
xtitle("Carrier Signal");
xgrid();
// FM signal
efm = Ac * cos( (2*%pi*Fc*T) + (B * sin(2*%pi*Fm*T)) );
subplot(3,1,3);
plot(T, efm);
xtitle("FM Signal");
xgrid();

TABULATION : 

![WhatsApp Image 2026-04-07 at 12 59 09 PM](https://github.com/user-attachments/assets/33af91bc-556b-4096-8dbd-9a44b7c89e00)

__Output:__

<img width="787" height="532" alt="Screenshot 2026-04-07 130105" src="https://github.com/user-attachments/assets/9222729e-5445-402f-982d-47040af5df01" />

![WhatsApp Image 2026-04-07 at 12 59 09 PM (1)](https://github.com/user-attachments/assets/03c855c8-b3f5-48c9-9a77-3cef24ba6a29)


__Result:__

![WhatsApp Image 2026-04-07 at 12 59 09 PM (2)](https://github.com/user-attachments/assets/bcd1b438-ff26-4b14-aa09-9a394504c87e)
