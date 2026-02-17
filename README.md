## Signal Extraction and Filtering from Square Waveform

This project focuses on extracting and processing various frequency components from a square waveform using passive and active filter designs. The system was analyzed theoretically, simulated, and implemented practically, with results compared using Bode plots and time-domain graphs.

---

## 1. Project Objective

The objective of this project was to design and implement filter circuits capable of:

1. Extracting the DC component (2.5V ±10mV) from a square waveform  
2. Extracting the 1 kHz sinusoidal component  
3. Extracting the 5 kHz sinusoidal component  
4. Combining 1 kHz and 5 kHz components to obtain modulation  
5. Removing the DC component to obtain a zero-centered AC signal  

---

## 2. FFT of Input Signal

The square waveform was analyzed using FFT to identify its frequency components before designing the filters.

---

## 3. Filter Designs

### Filter 1 – Cascaded RC Low-Pass Filter

- Type: Passive Low-Pass  
- Order: 2nd Order  
- Topology: Cascaded RC  
- Cutoff Frequency:  
  fc = 1 / (2πRC)  
  fc ≈ 15.9 Hz  

Purpose: Extract DC component and suppress higher frequencies.

---

### Filter 2 – LC Low-Pass Matching Filter

- Type: Passive LC Low-Pass  
- Order: 8th Order (4 LC π-sections)  
- Topology: Ladder (π-section)  
- Cutoff Frequency:  
  fc ≈ 5.03 kHz  

Features:
- 50 Ω termination  
- Steep attenuation  
- Suitable for communication systems  

---

### Filter 3 – LCLCRC Low-Pass Filter

- Type: Passive Low-Pass  
- Order: Approx. 4th Order  
- Topology: Ladder with damping resistors  
- Cutoff Frequency: 503 Hz  

Features:
- Damping resistors prevent resonance  
- Stable frequency response  

---

### Filter 4 – Active Amplifier Stage

- Configuration: Op-amp amplifier  
- Gain: Av = 11  

Purpose:
- Amplify filtered signal  
- Provide buffering  
- Reduce output impedance  

---

### Filter 5 – LC Low-Pass Filter

- Type: Passive LC Low-Pass  
- Order: 6th Order  
- Cutoff Frequency: 5.03 kHz  

Purpose:
- Suppress high-frequency noise  
- Clean amplifier output  

---

### Filter 6 – Capacitive Tap

- Purpose: DC blocking and AC sampling  
- Time Constant: τ = 5 ms  
- Cutoff Frequency: 31.8 Hz  

Used for removing DC component and obtaining AC waveform.

---

## 4. Bode Plot Comparison

Each output was analyzed and compared through:

- Theoretical Response  
- Simulated Response  
- Measured Response  

This comparison validated the design accuracy.

---

## 5. Results

- DC component successfully extracted  
- 1 kHz and 5 kHz signals isolated  
- Signal modulation achieved  
- DC removed to obtain AC waveform  
- Practical and simulation results closely matched  

---

## 6. Images and Graphs

---

## FFT of Input

![FFT Input](images/fft_input.png)

---

## Filter Circuits

### Filter 1 – RC Low Pass

![Filter 1](images/filter1_rc.png)

---

### Filter 2 – LC Matching Filter

![Filter 2](images/filter2_lc.png)

---

### Filter 3 – LCLCRC Filter

![Filter 3](images/filter3_lclcrc.png)

---

### Active Amplifier Stage

![Amplifier](images/amplifier_stage.png)

---

### Filter 5 – LC Low Pass

![Filter 5](images/filter5_lc.png)

---

### Capacitive Tap

![Capacitive Tap](images/capacitive_tap.png)

---

## Bode Plot Comparisons

### Output 1

![Output1 Theoretical](images/bode_output1_theoretical.png)  
![Output1 Measured](images/bode_output1_measured.png)  
![Output1 Simulated](images/bode_output1_simulated.png)

---

### Output 2

![Output2 Theoretical](images/bode_output2_theoretical.png)  
![Output2 Measured](images/bode_output2_measured.png)  
![Output2 Simulated](images/bode_output2_simulated.png)

---

### Output 3

![Output3 Theoretical](images/bode_output3_theoretical.png)  
![Output3 Measured](images/bode_output3_measured.png)  
![Output3 Simulated](images/bode_output3_simulated.png)

---

### Output 4

![Output4 Theoretical](images/bode_output4_theoretical.png)  
![Output4 Measured](images/bode_output4_measured.png)  
![Output4 Simulated](images/bode_output4_simulated.png)

---

### Output 5

![Output5 Theoretical](images/bode_output5_theoretical.png)  
![Output5 Measured](images/bode_output5_measured.png)  
![Output5 Simulated](images/bode_output5_simulated.png)

---

## Graph Comparisons

### Simulation vs Implementation

![Simulation](images/comparison_simulation.png)  
![Implementation](images/comparison_implementation.png)

---

### Input Signal

![Input Simulated](images/input_simulated.png)  
![Input Measured](images/input_measured.png)

---

### Outputs

#### Output 1
![Output1 Sim](images/output1_simulated.png)  
![Output1 Meas](images/output1_measured.png)

#### Output 2
![Output2 Sim](images/output2_simulated.png)  
![Output2 Meas](images/output2_measured.png)

#### Output 3
![Output3 Sim](images/output3_simulated.png)  
![Output3 Meas](images/output3_measured.png)

#### Output 4
![Output4 Sim](images/output4_simulated.png)  
![Output4 Meas](images/output4_measured.png)

#### Output 5
![Output5 Sim](images/output5_simulated.png)  
![Output5 Meas](images/output5_measured.png)

---

## Conclusion

The project successfully extracted and processed frequency components from a square waveform using passive and active filter networks. Simulation and measured results closely matched theoretical predictions, validating the design methodology. The project demonstrates practical application of filter design, frequency analysis, impedance matching, and amplifier integration in electrical network analysis.

---

## Team Members

- Muhammad Bilal Chaudhry  
- Talha Ahmad  
- Muhammad Muzammil  


