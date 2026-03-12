Two-Stage CMOS Operational Amplifier Design

# Overview

The project entails the design and simulation of a two-stage CMOS operational amplifier using the LTspice tool.  
The amplifier comprises a differential input stage with a current mirror active load and a common source gain stage. Miller compensation is employed in the design to guarantee circuit stability with adequate phase margin.

The design process was assessed using **DC analysis of the circuit's operating point, AC analysis of the circuit's frequency response, and transient analysis** of the circuit.

# Circuit Architecture

The operational amplifier circuit comprises the following components:

1. Differential Input Stage
- NMOS Differential Pair (M1, M2)
- PMOS Current Mirror Load (M3, M4)
- Tail Current Source (M5)

The first stage of the operational amplifier circuit converts the differential input signal to a single-ended output. It comprises an NMOS differential pair with a PMOS active load.

2. Second Gain Stage
- PMOS Common Source Amplifier (M6)
- NMOS Current Sink Load (M7)

The second gain stage of the circuit comprises a PMOS common source amplifier with an NMOS active load.

3. Bias Network
- Current Reference and Bias Transistor (M8)

The bias network ensures a stable bias point in the circuit.

4. Frequency Compensation
- Miller compensation capacitor (Cc)

This capacitor provides compensation to the amplifier and thus improves the phase margin of the amplifier. 

5. Load
- Output load capacitor (CL)

# Design Specifications

Parameter & Value 

 Supply Voltage = ±2.5 V 
 Tail Current = ~30 µA 
 Compensation Capacitor = 3 pF 
 Load Capacitor = 10 pF 

# Simulation Results

# DC Operating Point

The DC analysis of the amplifier is conducted to check the biasing of the transistor and to ensure that the MOSFETs are operating in the saturation region for linear amplification.

Important Observations:

- The tail current is divided equally between the differential pair.
- The output node is biased close to the mid-supply point.
- The total power consumption is 0.8 mW.

AC Frequency Response

AC analysis was carried out to obtain the following parameters:
Gain
Bandwidth
Stability

 Parameter & Result
 DC Gain = ~80 dB 
 Gain Bandwidth Product (GB)  ~10 MHz  
 Phase Margin  ~65°

The result shows that the amplifier is stable with adequate gain and bandwidth for analog signal processing.

# Slew Rate Measurement

Transient analysis was carried out to analyze the large signal response of the amplifier.

The slew rate is given by:
SR = dVout / dt

Slew rate:
~20 V/µs

This is consistent with the calculated slew rate:
SR ≈ I / Cc

## Simulation Tools

The following simulator was used to carry out all the simulations:
LT Spice

Types of simulations carried out:
- DC Operating Point Analysis
- AC Frequency Response Analysis
- Transient Analysis

# Key Learning Outcomes

This project demonstrates:

- CMOS analog circuit design
- Differential amplifier design
- Current mirror biasing
- Frequency compensation techniques
- Stability analysis using phase margin
- Slew rate analysis in operational amplifiers
