EXP 1 A : COMPUTATION OF DFT USING DIRECT AND FFT
AIM:
To Obtain DFT and FFT of a given sequence in SCILAB.
APPARATUS REQUIRED:
PC installed with SCILAB.

PROGRAM:
clc; clear;

x = [10, 20, 30, 40];
N = length(x);

disp("DFT using direct formula:");

X = zeros(1, N);
for k = 0:N-1 for n = 0:N-1 X(k+1) = X(k+1) + x(n+1)exp((-%i2*%pikn)/N); end end disp(X, "DFT(X) =");

disp("DFT using FFT function:"); X_fft = fft(x, -1);
disp(X_fft, "FFT(X) =");

subplot(2,1,1); plot2d3(0:N-1, abs(X)); xlabel("Frequency Index k"); ylabel("|X(k)|"); title("Magnitude Spectrum using DFT");

subplot(2,1,2); plot2d3(0:N-1, abs(X_fft)); xlabel("Frequency Index k"); ylabel("|X(k)|"); title("Magnitude Spectrum using FFT");

OUTPUT:
![Uploading Screenshot 2025-09-08 152519.png…]()

RESULT:
The DFT and FFT of the given sequence were successfully computed using SCILAB. Both direct computation and FFT function produced identical results, and the magnitude spectrum was plotted.
