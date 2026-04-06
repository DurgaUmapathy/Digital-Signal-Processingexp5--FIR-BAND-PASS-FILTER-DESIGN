# Digital-Signal-Processing--FIR-BAND-PASS-FILTER-DESIGN
## AIM:
To generate design of Band Pass FIR digital filter using Window.
## Software Required:
MAT LAB R2012.
## Algorithm:
Step 1: Open MATLAB and Write the program.

Step 2: Read the values of cut off frequency wc.

Step 2: Read the values of Order of the filter N.

Step 3: Find out the desired impulse response of the Band Pass filter Coefficient.

Step 4: Find out the windowing sequence.

Step 5: Plot the magnitude spectrum with x-label and y-label with suitable title.

Step 6: Terminate the program.

## PROGRAM: 
clc; % clear screen
clear all; % clear screen
close all; % close all figure windows
Wc1=input('enter the value of Wc1=');
Wc2=input('enter the value of Wc2=');
N=input('enter the value of N=');
alpha=(N-1)/2;
eps=0.001;
%Band Stop Filter Coefficient
n=0:1:N-1; 
hd=(sin(Wc1*(n-alpha+eps))-sin(Wc2*(n-alpha+eps))+sin(pi*(n-alpha+eps)))./((n-alpha+eps)*pi)
%Bartlett Window Sequence
n=0:1:N-1;
wh=1-2*abs(n- alpha)/N
hn=hd.*wh
% Plot the Band Stop Filter with Bartlett Window Technique
w=0:0.01:pi;
h=freqz(hn,1,w);
plot(w/pi,abs(h),'blue');

## OUTPUT:
![dspexp5](https://github.com/user-attachments/assets/dbac174b-60bb-45f0-a600-2d0e3ef02925)


## RESULT:
![dspexp52](https://github.com/user-attachments/assets/7a7e8d70-a715-494e-a9f4-42f47c539f9f)

