# Design of PWM Generator in Verilog

##  Project Overview

This project implements an **8-bit PWM (Pulse Width Modulation) Generator** using **Verilog HDL**.

The design uses a simple counter and comparator-based approach to generate a PWM output signal with a variable duty cycle. The design is modeled using **behavioral Verilog** and verified through simulation using **Xilinx Vivado**.


## Abstract

The PWM Generator is designed using Verilog HDL using a **behavioral modeling approach**.

An 8-bit counter continuously increments with every clock cycle. The counter value is compared with the input duty cycle. When the counter value is less than the duty cycle, the PWM output is HIGH; otherwise, it is LOW.

By changing the duty cycle input, the ON time of the PWM signal can be controlled.

The design is simulated using **Xilinx Vivado** to verify its operation for different duty cycle values.

---

## Problem Statement

Design a PWM generator that produces a digital output signal with a **variable duty cycle** using Verilog HDL.

### System Specifications

- **Input:** Clock signal
- **Duty Cycle Input:** 8-bit
- **Output:** PWM signal
- **Duty Cycle Range:** 0–100%
- **Design Type:** Clock-driven sequential logic
- **Modeling:** Behavioral
- **Tool:** Xilinx Vivado

---

## Working Principle

The PWM generator consists of:

1. **8-bit Counter**
2. **Comparator**
3. **PWM Output**

The counter increments on every positive edge of the clock.

The counter is continuously compared with the duty cycle input.

### Logic

```text
if (counter < duty)
    pwm_out = 1;
else
    pwm_out = 0;
