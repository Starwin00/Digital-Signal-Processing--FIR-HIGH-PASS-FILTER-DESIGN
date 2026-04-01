# Digital-Signal-Processing--FIR-HIGH-PASS-FILTER-DESIGN
## AIM:
To generate design of High pass FIR digital filter using Window.
## Software Required:
MATLAB R2012.
## Algorithm:
Step 1: Open MATLAB and Write the program.

Step 2: Read the values of cut off frequency wc.

Step 2: Read the values of Order of the filter N.

Step 3: Find out the desired impulse response of the hIGH Pass filter Coefficient.

Step 4: Find out the windowing sequence.

Step 5: Plot the magnitude spectrum with x-label and y-label with suitable title.

Step 6: Terminate the program.

## PROGRAM: 
```
clc; % clear screen
clear all; % clear screen
close all; % close all figure windows
wc=input('enter the value of cut off frequency'); 
N=input('enter the value of filter'); 
alpha=(N-1)/2; 
eps=0.001; 
%High Pass Filter Coefficient
n=0:1:N-1; 
hd=(sin(pi*(n-alpha+eps))-sin((n-alpha+eps)*wc))./(pi*(n-alpha+eps))
%barlett Window Sequence
n=0:1:N-1;
wh=1-(2*abs(n-alpha))/N
hn=hd.*wh
% Plot the High Pass Filter with Barlett Window Technique
w=0:0.01:pi; 
h=freqz(hn,1,w);
plot(w/pi,abs(h),'blue');
```
## OUTPUT:
<img width="698" height="528" alt="image" src="https://github.com/user-attachments/assets/912f82be-a928-4ea8-8f9d-03726f1c8d10" />

## RESULT:
!![e101470d-631f-419e-bd69-4be85e3fa0db](https://github.com/user-attachments/assets/03735ce7-4102-49da-a4e4-deda83c21d0c)





