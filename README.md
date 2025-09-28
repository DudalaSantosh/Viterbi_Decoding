# Viterbi Decoding Simulation in MATLAB

This repository contains a MATLAB implementation of a **Viterbi decoder** for a communication system with inter-symbol interference (ISI).  
The code simulates transmission, channel distortion, and decoding using the Viterbi algorithm, along with visualization of the **state diagram**, **trellis diagram**, and **symbol error rate (SER) performance**.

---

## Features
- Defines a channel model with ISI using FIR filter coefficients.  
- Constructs **state space** representation for the channel memory.  
- Plots the **state diagram** with all transitions and outputs.  
- Generates trellis transitions and visualizes them step by step.  
- Implements **Viterbi decoding** to estimate transmitted symbols.  
- Performs **Monte Carlo simulations** to evaluate **SER performance** under AWGN for different block lengths.  
- Compares decoding performance for block sizes:  
  - `N = μ`  
  - `N = 2μ`  
  - `N = 5μ`  
  - `N = 7μ`  
  - `N = 10μ`  

---

## File Description
- **Main Script (`.m`)**  
  - Generates transmitted and received signals.  
  - Runs trellis diagram visualization.  
  - Performs Monte Carlo simulations.  
  - Plots SER vs SNR curves.  

- **Functions**
  - `Decode(...)` → Implements the Viterbi algorithm for symbol sequence estimation.  
  - `plotStateDiagram(...)` → Plots the state diagram for given channel coefficients and input symbols.  

---

## Parameters
- **Channel coefficients (ISI filter):**  
  ```matlab
  A = 1/sqrt(2) * [0.6 -1 0.8];
