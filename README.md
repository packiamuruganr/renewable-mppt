# EXP-4SIMULATION-OF-P-O-MPPT-ALGORITHM-BASED-SOLAR-POWERED-DC-DC-CONVERTER

## Aim
To simulate Perturb and Observe (P&O) based solar powered DC/DC boost converter using MATLAB for maximum power extraction.

---

## Software Used
- MATLAB (2021 or above)
- Simulink

---

## Modelling Parameters

| S.No | Parameter          | Value       |
|------|--------------------|-------------|
| 1    | Maximum Voltage    | 120 V       |
| 2    | Irradiance         | 1000 W/m²   |
| 3    | Temperature        | 25°C        |
| 4    | Inductor (L)       | 100 µH   |
| 5    | Capacitor (C)       | 1000 µF  |
| 6    | Switching Frequency | 25 kHz   |
| 7    | Load Resistance     | 350 Ω    |
| 8    | Duty Cycle          | 10%–80%  |
| 1    | Switching Frequency | 1 kHz    |

---

## Theory
Maximum Power Point Tracking (MPPT) is used to extract maximum power from solar PV systems under varying environmental conditions.

The Perturb and Observe (P&O) algorithm works by:
- Slightly changing voltage or duty cycle
- Observing change in power
- Moving toward maximum power point

Advantages:
- Simple to implement
- Low cost
- Good adaptability

---
## Circuit Diagram
<img width="1769" height="751" alt="Screenshot 2026-03-20 172852" src="https://github.com/user-attachments/assets/d260e767-4aa0-4402-a54f-080bd7415155" />
<img width="1742" height="668" alt="Screenshot 2026-03-20 172940" src="https://github.com/user-attachments/assets/ea4ef00c-b127-47db-9de4-c0a94e2e0298" />

## Procedure
1. Open MATLAB.
2. Open Simulink Library Browser.
3. Add required components:
   - Solar panel, measurement blocks
   - MOSFET, diode, inductor, capacitor
   - RLC load
   - PI controller, PWM generator
   - Slider, scope
4. Connect components as per circuit diagram.
5. Link slider with reference input.
6. Set parameters.
7. Run simulation for different irradiance values.
8. Record input and output parameters.

---
## P&O MPPT Algorithm:
function [P, D] = fcn(V, I, StepSize)
% P&O MPPT Algorithm
% Inputs:
% V - Voltage
% I - Current
% StepSize - Step size for perturbation
%
% Outputs:
% P - Power
% D - Duty cycle

% Initialization
persistent Pprev Vprev Dprev

if isempty(Pprev)
    Pprev = 0;
    Vprev = 0;
    Dprev = 0.5;
end


## Tabulation
| Irradiance (W/m²) | Vin (V) | Iin (A) | Ppv (W) | Vo (V) | Io (A) | Po (W) |
|-------------------|--------|--------|--------|-------|-------|--------|
| 525.6             | 2.763  | 0.0230 | 0.001226 | 5.256 | 0.001471 | 0.001226 |

---
## Output Waveform



## Result
The P&O based MPPT algorithm for solar powered DC/DC boost converter was successfully simulated and maximum power extraction was achieved.

