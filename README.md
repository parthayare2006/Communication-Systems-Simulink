# Communication-Systems-Simulink

This repository contains MATLAB Simulink projects developed for the study and implementation of communication systems.

Projects
1. Morse Code ASK Modulation and Demodulation

This project implements a complete Morse Code communication system using Amplitude Shift Keying (ASK).

The system accepts a text message, converts it into Morse code, generates the Morse waveform, performs ASK modulation, demodulates the received signal, and decodes it back into the original text.

Features
Text input
ASCII conversion
Morse code encoding
Morse waveform generation
ASK modulation
ASK demodulation
Morse code decoding
Original text recovery
Supports alphabets A–Z
Supports numbers 0–9
Morse Code Timing
Signal	Duration
Dot	0.1 s
Dash	0.3 s
Element Gap	0.1 s
Letter Gap	0.3 s
Word Gap	0.7 s
Example

Input: SOS

Morse Code: ... --- ...

The ASK modulator represents the Morse code using bursts of a 100 Hz carrier.

A dot produces a short carrier burst, while a dash produces a longer carrier burst. During gaps, the carrier is turned OFF.

After demodulation and decoding, the original message is recovered.

Output: SOS

Software Used
MATLAB
Simulink
Project File

MORSECODE.slx

2. QPSK Modulation and Bit Error Rate Analysis

This project implements Quadrature Phase Shift Keying (QPSK) modulation and demodulation and analyzes the Bit Error Rate (BER) under noise-free and noisy channel conditions.

Features
Binary data generation
QPSK modulation
QPSK constellation diagram
Noise-free QPSK demodulation
AWGN noisy channel
Noisy QPSK demodulation
BER calculation
Digital up-conversion
QPSK passband waveform visualization
Working

The input binary data is grouped into pairs of bits and supplied to the QPSK modulator.

Each pair of bits is represented by one of four possible phase states.

The modulated signal is divided into two paths.

Noise-Free Path:
The QPSK signal is directly supplied to the QPSK demodulator. The recovered bits are compared with the transmitted bits using the Error Rate Calculation block.

Noisy Path:
The QPSK signal is passed through an AWGN (Additive White Gaussian Noise) channel before demodulation. The recovered bits are compared with the transmitted bits to calculate the BER.

QPSK Constellation

QPSK uses four constellation points, with each point representing a unique 2-bit combination.

The four phase states correspond to the four possible combinations of two input bits.

BER Results
Channel	BER	Errors	Total Bits
Noise-Free	0	0	1002
AWGN Noisy	0.007984	8	1002

The noise-free channel produces zero bit errors, while the AWGN channel introduces a small number of bit errors.

Passband Waveform

The QPSK complex baseband signal is digitally up-converted to obtain a real passband waveform.

The passband signal maintains approximately constant amplitude while its phase changes according to the transmitted QPSK symbols.

Software Used
MATLAB
Simulink
Project File

QPSK_BER.slx

Technologies Used
MATLAB
Simulink
MATLAB Function Blocks
Digital Modulation
Digital Demodulation
AWGN Channel
Bit Error Rate Analysis
Communication Techniques Covered
Morse Code
Amplitude Shift Keying (ASK)
Quadrature Phase Shift Keying (QPSK)
AWGN Channel
Digital Up-Conversion
Bit Error Rate (BER)
Author

Communication Systems Project
