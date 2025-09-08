# EXP 1 A : COMPUTATION OF DFT USING DIRECT AND FFT

# AIM: 

# To Obtain DFT and FFT of a given sequence in SCILAB. 

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
// DISCRETE FOURIER TRANSFORM 
clc;
clear;

// Take input discrete signal
x = input("Enter discrete signal as [x1 x2 ...]: ");
N = length(x);

// Initialize DFT output
X = zeros(1, N);

// DFT calculation using formula
for k = 0:N-1
    for n = 0:N-1
        X(k+1) = X(k+1) + x(n+1) * exp(-%i * 2 * %pi * k * n / N);
    end
end

// Frequency axis (normalized)
f = (0:N-1) / N;

// Plot magnitude spectrum
plot(f, abs(X));
xlabel("Normalized Frequency");
ylabel("Magnitude");
title("Discrete Fourier Transform )");

# OUTPUT: 
https://cdn.corenexis.com/view/6157872168

# RESULT: 
DFT and FFT of a given sequence in SCILAB was obtained 
