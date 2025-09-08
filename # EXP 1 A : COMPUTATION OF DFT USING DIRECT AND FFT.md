# EXP 1 A : COMPUTATION OF DFT USING DIRECT AND FFT

# AIM: 

# To Obtain DFT and FFT of a given sequence in SCILAB. 

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
// Program to compute DFT using direct method and FFT

clc;
clear;

// Input sequence
x = [10, 20, 30, 40];  
N = length(x);

// --- Direct computation of DFT ---
disp("DFT using direct formula:");

X = zeros(1, N);   // Initialize DFT result
for k = 0:N-1
    for n = 0:N-1
        X(k+1) = X(k+1) + x(n+1)exp((-%i*2%pi*k*n)/N);
    end
end
disp(X, "DFT(X) =");

// --- Using inbuilt FFT function ---
disp("DFT using FFT function:");
X_fft = fft(x, -1);   // FFT of sequence
disp(X_fft, "FFT(X) =");

// Plotting
subplot(2,1,1);
plot2d3(0:N-1, abs(X));
xlabel("Frequency Index k");
ylabel("|X(k)|");
title("Magnitude Spectrum using DFT");

subplot(2,1,2);
plot2d3(0:N-1, abs(X_fft));
xlabel("Frequency Index k");
ylabel("|X(k)|");
title("Magnitude Spectrum using FFT"); 

# OUTPUT: 
![WhatsApp Image 2025-09-08 at 15 44 48_c863292f](https://github.com/user-attachments/assets/dd6f9ddf-c510-4b82-ac9d-4de20317d1d1)



# RESULT: 
DFT and FFT of the given sequence were successfully computed using SCILAB, and results matched.
