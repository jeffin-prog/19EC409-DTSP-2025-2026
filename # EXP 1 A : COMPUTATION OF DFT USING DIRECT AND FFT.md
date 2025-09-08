# EXP 1 A : COMPUTATION OF DFT USING DIRECT AND FFT

# AIM: 

# To Obtain DFT and FFT of a given sequence in SCILAB. 

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
// DISCRETE FOURIER TRANSFORM 
// SCILAB Program to compute DFT and FFT of a sequence

clc;
clear;

// Input sequence
x = [1 2 3 4];    // Example sequence
N = length(x);

// ----- DFT Calculation -----
X_dft = zeros(1, N);
for k = 0:N-1
    for n = 0:N-1
        X_dft(k+1) = X_dft(k+1) + x(n+1)*exp(-%i*2*%pi*k*n/N);
    end
end

// ----- FFT using built-in function -----
X_fft = fft(x, -1);   // -1 → forward FFT

// Display results
disp(x, "Input sequence x(n):");
disp(X_dft, "DFT of x(n):");
disp(X_fft, "FFT of x(n):");

// Magnitude and Phase
disp(abs(X_fft), "Magnitude of FFT:");
disp(angle(X_fft), "Phase of FFT:");

// Plot
subplot(2,1,1);
stem(0:N-1, abs(X_fft));
xlabel("k"); ylabel("|X(k)|");
title("Magnitude Spectrum");

subplot(2,1,2);
stem(0:N-1, angle(X_fft));
xlabel("k"); ylabel("∠X(k)");
title("Phase Spectrum");


# OUTPUT: 
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/4375c74f-69ff-480e-9071-bb1c9b909945" />
<img width="610" height="460" alt="image" src="https://github.com/user-attachments/assets/f3b204b8-46aa-4324-ae18-5c7662f83736" />


# RESULT: 
