# Digital-Signal-Processing--Correlation
## AIM:
To generate discrete auto correlation and cross correlation of signals using MATLAB.
## APPARATUS REQUIRED:
MATLAB R2012.
## ALGORITHM:
Step 1: Open matlab. Write the program.

Step 2: Read the input sequence 1 and input sequence 2 sequence.

Step 3: Perform auto correlation and cross correlation for both the sequences. 

Step 4: Plot the output sequence with x-label and y-label with suitable title.

Step 5: Terminate the program.


## PROGRAM: 
clc;
clear all;
close all;

% INPUT SIGNAL-1
a = input('Enter the starting index of x(n): ');
x = input('Enter the x(n) sequence: ');

n = a : a+length(x)-1;

figure(1)
stem(n,x)
xlabel('Time')
ylabel('Amplitude')
title('Input Signal-1')

% INPUT SIGNAL-2
b = input('Enter the starting index of y(n): ');
y = input('Enter the y(n) sequence: ');

n1 = b : b+length(y)-1;

figure(2)
stem(n1,y)
xlabel('Time')
ylabel('Amplitude')
title('Input Signal-2')

% AUTO CORRELATION
out1 = xcorr(x);

n2 = -(length(x)-1) : (length(x)-1);

figure(3)
stem(n2,out1)
xlabel('Time')
ylabel('Amplitude')
title('Discrete Auto Correlation')

% CROSS CORRELATION
out2 = xcorr(x,y);

n3 = -(length(y)-1) : (length(x)-1);

figure(4)
stem(n3,out2)
xlabel('Time')
ylabel('Amplitude')
title('Discrete Cross Correlation')
## OUTPUT:
<img width="679" height="613" alt="image" src="https://github.com/user-attachments/assets/c237b85e-2bbf-463c-b858-b7d2467a038c" />
<img width="686" height="610" alt="image" src="https://github.com/user-attachments/assets/efe757d8-9504-4ec9-a785-f499174b5751" />
<img width="686" height="623" alt="image" src="https://github.com/user-attachments/assets/e46dfdf5-6eb1-497a-8cb0-2d00fd6c225f" />
<img width="686" height="512" alt="image" src="https://github.com/user-attachments/assets/d3c09ad2-32ae-451a-91a2-2a1e70bdf0f1" />



## RESULT:
The cross correlation of x1[n] and x2[n] is {3,11,-7,-1,20,-18,8}
