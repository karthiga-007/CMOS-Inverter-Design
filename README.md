# CMOS Inverter Design and Transient Analysis using LTspice

## Overview

This project implements a CMOS inverter using LTspice and analyzes its switching behavior through transient simulation.

A CMOS inverter is the fundamental building block of digital integrated circuits. It consists of a PMOS transistor connected to the supply voltage and an NMOS transistor connected to ground. The output is taken from the common drain connection of both transistors.

---

## Objectives

- Design a CMOS inverter in LTspice
- Verify inverter operation using transient analysis
- Observe input-output switching characteristics
- Study the behavior of CMOS logic under pulse excitation

---

## Circuit Description

The inverter consists of:

- PMOS transistor (pull-up network)
- NMOS transistor (pull-down network)
- 5 V DC supply (VDD)
- Pulse input source
- 1 pF load capacitor

### Operating Principle

- When the input is LOW (0 V):
  - PMOS turns ON
  - NMOS turns OFF
  - Output is pulled to VDD (Logic HIGH)

- When the input is HIGH (5 V):
  - PMOS turns OFF
  - NMOS turns ON
  - Output is pulled to Ground (Logic LOW)

Thus, the output is always the logical inverse of the input.

---

## Simulation Parameters

### Supply Voltage

```text
VDD = 5 V
```

### Input Pulse

```text
PULSE(0 5 0 0 0 10m 20m)
```

### Load Capacitance

```text
1 pF
```

### Transient Analysis

```text
.tran 0 100m 0
```

---

## Results

The transient simulation demonstrates the inverter action:

- Input transitions from LOW to HIGH and HIGH to LOW
- Output switches in the opposite direction
- Proper CMOS logic inversion is observed

### Expected Waveforms

| Input (Vin) | Output (Vout) |
|------------|--------------|
| 0 V | 5 V |
| 5 V | 0 V |

---

## Files Included

- `CMOS inverter design.asc` – LTspice schematic
- `README.md` – Project documentation

---

## Software Used

- LTspice

---

## Applications

- Digital Logic Design
- VLSI Design
- CMOS Integrated Circuits
- Logic Gates
- Microprocessor and FPGA Systems

---

## Conclusion

The CMOS inverter was successfully designed and simulated in LTspice. The transient analysis verified correct inverter functionality, with the output consistently producing the complement of the input signal. This project demonstrates the fundamental operation of CMOS logic and serves as a foundation for more complex digital circuit designs.
