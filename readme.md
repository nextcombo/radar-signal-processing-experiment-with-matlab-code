# Radar Signal Processing Experiment [with MATLAB Code]

1.1. Uniform distribution
1.2 Gaussian distribution
1.3 Rayleigh distribution
1.4 Relationship between Gaussian noise and Rayleigh distribution
2. Noise signal generation
Uniformly distributed noise generation
\n        \n  
It can display its time-domain waveform, histogram, and spectrum. Its histogram shows uniform distribution, the energy of each frequency point within its band is uniform, which meets the characteristics of white noise.
Gaussian distribution noise generation
\n        \n  
The time-domain waveform, histogram, and spectrum are visible. The histogram displays a Gaussian bell curve characteristic, with energy distribution even across all frequencies within its bandwidth, consistent with white noise properties.
Raleigh distribution noise generation
\n        \n  
It can display its time-domain waveform, histogram, and spectrum. Its histogram shows the characteristics of Rayleigh distribution, and the energy distribution of each frequency point within its bandwidth is uniform, which meets the characteristics of white noise.
3. Radar Signal Generation and Noise Addition
3.1 BPSK signal generation and noise addition
\n        \n  
The BPSK symbol signals, the modulated signals, and the spectrum of the modulated signals.
It can be seen that its spectrum has a significant harmonic characteristic, as the original signal is a product of sine and square wave, and the harmonic components of the square wave are reflected in the spectrum of the modulated signal.
\n        \n  
Now add noise to the BPSK modulation signal. It can be clearly seen that there are spikes and peaks in its time-domain waveform.
3.2 LFM (Linear Frequency Modulation) Signal Generation and Noise Addition
The LFM signal waveform, its modulation waveform, the energy spectrum and the frequency spectrum.
\n        \n  
It can be seen that its spectrum also has a distinct harmonic characteristic, as the original signal is multiplied by a sine wave with a slope and also contains sudden components. The sudden components mean that there are high-frequency harmonics, which are reflected in the spectrum of the modulated signal.
\n        \n  
Now add noise to the LFM modulated signal. It can be clearly seen that there are spikes and peaks on its time-domain waveform.  
4. MATLAB code
clc; clear; close all;\n​\n% Time base parameters\ndt = 1e-6;              % Time scale: 1us\nfs = 1/dt;              % Sampling frequency: 1Mhz\nstop = 5e-3;            % Stop time: 5ms\nt = 0 : dt : stop-dt;   % Discrete time vector\nN = length(t);          % Points\nfv = (0:N/2-1)*1/dt/N;  % Discrete frequency vector\n​\n% Linear FM pulse\nA = 1;                  % Amplititude: 1V\nf0 = 10e3;              % Carrier frequency: 10kHz\nfshift = 100e3;         % Frequency shift: 100kHz\nfm = 0.4e3;             % Modulation frequency: 40Hz\n​\nmod = 0.5*square(0.5).*(2*sawtooth(2*pi*fm*t) + 1);\nlfm = 0.5*square( 0.5).*vco(mod, [f0 f0+fshift], fs);\ns = 20.*log10(abs(fft(lfm))./N);\n  
End

## Images

![Radar Signal Processing Experiment [with MATLAB Code]](01.png)
![Radar Signal Processing Experiment [with MATLAB Code]](02.png)
![Radar Signal Processing Experiment [with MATLAB Code]](03.png)
![Radar Signal Processing Experiment [with MATLAB Code]](04.png)
![Radar Signal Processing Experiment [with MATLAB Code]](05.png)
![Radar Signal Processing Experiment [with MATLAB Code]](06.png)
![Radar Signal Processing Experiment [with MATLAB Code]](07.png)
![Radar Signal Processing Experiment [with MATLAB Code]](08.jpg)

<!-- PAYMENT_BLOCK -->

## Get this dataset

- Payment link (Stripe): [Buy now](https://buy.stripe.com/3cs8yP7sY87d0vu9AB)
- Payment QR code: ![Payment QR code](pay.png)

<!-- /PAYMENT_BLOCK -->
