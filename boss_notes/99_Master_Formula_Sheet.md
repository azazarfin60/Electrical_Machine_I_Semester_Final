# 📐 Master Formula Sheet — ECE 2207

> Quick reference for all formulas across both sections. Each entry links back to the boss note where it is derived and explained. Print this. Take it into revision. Know every formula cold.

---

## Section A — Transformer

### EMF Equation

$$E = 4.44 f N \Phi_m \text{ (volts)}$$

- [T-01: Transformer Fundamentals](T-01_Transformer_Fundamentals.md)

### Turns Ratio

$$a = \frac{N_1}{N_2} = \frac{E_1}{E_2} = \frac{V_1}{V_2} = \frac{I_2}{I_1}$$

### Equivalent Circuit (Referred to Primary)

$$R_{01} = R_1 + a^2 R_2, \qquad X_{01} = X_1 + a^2 X_2, \qquad Z_{01} = \sqrt{R_{01}^2 + X_{01}^2}$$

- [T-04: Equivalent Circuit](T-04_Equivalent_Circuit.md)

### Voltage Regulation

$$\%\text{VR} = \frac{E_2 - V_2}{V_2} \times 100 \approx \frac{I_2(R_{02}\cos\phi \pm X_{02}\sin\phi)}{V_2} \times 100$$

(+ for lagging, - for leading)

- [T-05: Voltage Regulation](T-05_Voltage_Regulation.md)

### Condition for Zero VR

$$\tan\phi = \frac{R_{02}}{X_{02}} \quad \text{(leading pf)}$$

### Losses and Efficiency

$$\eta = \frac{xS\cos\phi}{xS\cos\phi + P_i + x^2P_{Cu}} \times 100\%$$

where $x$ = fraction of full load, $S$ = VA rating, $P_i$ = iron loss, $P_{Cu}$ = full-load Cu loss.

### Condition for Maximum Efficiency

$$P_i = x^2 P_{Cu} \implies x = \sqrt{\frac{P_i}{P_{Cu}}}$$

- [T-06c: Efficiency](T-06c_Efficiency.md)

### OC Test (Gives $R_c$, $X_m$, $P_i$)

$$\cos\phi_0 = \frac{P_0}{V_1 I_0}, \quad I_c = I_0\cos\phi_0, \quad I_m = I_0\sin\phi_0$$

$$R_c = V_1/I_c, \quad X_m = V_1/I_m, \quad P_i = P_0$$

### SC Test (Gives $R_{01}$, $X_{01}$, $P_{Cu}$)

$$Z_{01} = V_{sc}/I_{sc}, \quad R_{01} = P_{sc}/I_{sc}^2, \quad X_{01} = \sqrt{Z_{01}^2 - R_{01}^2}$$

- [T-06a: OC Test](T-06a_OC_Test.md) | [T-06b: SC Test](T-06b_SC_Test.md)

### Parallel Operation (Load Sharing)

$$S_A = S \cdot \frac{Z_B}{Z_A + Z_B}, \qquad S_B = S \cdot \frac{Z_A}{Z_A + Z_B}$$

- [T-09: Vector Groups & Parallel Operation](T-09_Vector_Groups.md)

### Auto-Transformer Savings

$$\text{Saving} = \left(1 - \frac{1}{a}\right) \times 100\%$$

$$\text{VA}_{\text{induction}} = \left(1 - \frac{1}{a}\right) \times \text{VA}_{\text{conduction}}$$

- [T-10: Auto-Transformer](T-10_Auto_Transformer.md)

### 3-Phase Transformer Connections

| Connection | $V_2$ (ratio) | Phase Shift |
|:---|:---|:---|
| Y-Y | $V_L/a$ | 0° |
| $\Delta$-$\Delta$ | $V_L/a$ | 0° |
| Y-$\Delta$ | $V_L/(a\sqrt{3})$ | -30° |
| $\Delta$-Y | $V_L\sqrt{3}/a$ | +30° |

- [T-07a: Three-Phase Connections](T-07a_3Phase_Connections.md)

### Scott Connection

$$V_{\text{teaser}} = V \times (\sqrt{3}/2) \times (N_2/N_1)$$

$$V_{\text{main}} = V \times (N_2/N_1)$$

### Open-Delta Power Rating

$$S_{\text{open-}\Delta} = \frac{1}{\sqrt{3}} \times S_{\text{closed-}\Delta} = 57.7\% \text{ of V-V}$$

- [T-07b: Open-Delta](T-07b_Open_Delta.md) | [T-08: Scott Connection](T-08_Scott_Connection.md)

---

## Section B — Induction Motor

### Synchronous Speed

$$\boxed{N_s = \frac{120f}{P} \text{ rpm}}$$

- [T-12: Rotating Magnetic Field](T-12_Rotating_Magnetic_Field.md)

### 3-Phase RMF Magnitude

$$\Phi_r = 1.5\Phi_m = \frac{3}{2}\Phi_m \quad (\text{constant, rotating at } N_s)$$

### 2-Phase RMF Magnitude

$$\Phi_r = \Phi_m \quad (\text{constant, rotating at } N_s)$$

### Slip

$$\boxed{s = \frac{N_s - N}{N_s}}, \qquad N = N_s(1-s)$$

- [T-13: Slip & Basics](T-13_Slip_and_Basics.md)

### Rotor Frequency

$$f_r = sf$$

### Rotor Quantities at Slip $s$

$$E_{2s} = sE_2, \qquad X_{2s} = sX_2, \qquad R_2 = \text{unchanged}$$

$$I_2 = \frac{sE_2}{\sqrt{R_2^2 + (sX_2)^2}}$$

### Equivalent Circuit: Load Resistance

$$\frac{R_2}{s} = R_2 + \underbrace{R_2\frac{(1-s)}{s}}_{R_L \text{ (mech. load)}}$$

- [T-14: IM Equivalent Circuit](T-14_IM_Equivalent_Circuit.md)

### Running Torque

$$\boxed{T = \frac{ksE_2^2 R_2}{R_2^2 + s^2X_2^2}}, \qquad k = \frac{3}{2\pi n_s}$$

- [T-15b: Running & Max Torque](T-15b_Torque_Running_and_Max.md)

### Starting Torque ($s = 1$)

$$T_{st} = \frac{kE_2^2 R_2}{R_2^2 + X_2^2}$$

### Maximum Starting Torque: $R_2 = X_2$

- [T-15a: Starting Torque](T-15a_Torque_Starting.md)

### Slip at Maximum Torque

$$\boxed{s_{mT} = \frac{R_2}{X_2}}$$

### Maximum Torque (Independent of $R_2$!)

$$\boxed{T_{\max} = \frac{kE_2^2}{2X_2}}$$

### $T_f/T_{\max}$ Ratio

$$\boxed{\frac{T_f}{T_{\max}} = \frac{2as_f}{a^2 + s_f^2}}, \qquad a = s_{mT} = \frac{R_2}{X_2}$$

### Torque-Speed Approximations

| Region | Condition | Approximation |
|:---|:---|:---|
| Low slip | $sX_2 \ll R_2$ | $T \propto s$ (linear) |
| High slip | $sX_2 \gg R_2$ | $T \propto 1/s$ (inversely) |

- [T-15c: Torque-Speed Curves](T-15c_Torque_Speed_Curves.md)

### Power Flow (The Golden Ratio)

$$\boxed{P_g : P_{Cu,r} : P_m = 1 : s : (1-s)}$$

$$P_{Cu,r} = sP_g, \qquad P_m = (1-s)P_g$$

$$\eta_{\text{rotor}} = (1-s)$$

- [T-16: Power Flow](T-16_Power_Flow.md)

### No-Load Test (Gives $R_c$, $X_m$)

$$\cos\phi_0 = \frac{P_0}{\sqrt{3}V_0 I_0}$$

$$R_c = V_\phi/I_c, \qquad X_m = V_\phi/I_m$$

- [T-17a: No-Load Test](T-17a_No_Load_Test.md)

### Blocked Rotor Test (Gives $R_{01}$, $X_{01}$)

$$Z_{01} = \frac{V_{sc}/\sqrt{3}}{I_{sc}}, \quad R_{01} = \frac{P_{sc}}{3I_{sc}^2}, \quad X_{01} = \sqrt{Z_{01}^2 - R_{01}^2}$$

$$R_2' = R_{01} - R_1, \qquad X_1 = X_2' = X_{01}/2$$

- [T-17b: Blocked Rotor Test](T-17b_Blocked_Rotor_Test.md)

### Star-Delta Starter

$$I_{L,Y}/I_{L,\Delta} = 1/3, \qquad T_{st,Y}/T_{st,\Delta} = 1/3$$

Equivalent auto-transformer ratio: $x = 1/\sqrt{3} = 57.7\%$

- [T-19: Starting Methods](T-19_Starting_Methods_3Phase.md)

### Rotor Resistance Speed Control (Constant Torque)

$$\frac{s_1}{R_2} = \frac{s_2}{R_2 + R_{\text{ext}}}$$

- [T-20: Speed Control & Braking](T-20_Speed_Control_and_Braking.md)

### Induction Generator: Engine Speed

$$N_{\text{engine}} = N_s(1 + |s|)$$

### SEIG Capacitance (Delta)

$$Q = \sqrt{3}V_LI_L\sin\phi, \quad X_C = V_L^2/(Q/3), \quad C = 1/(2\pi f X_C)$$

- [T-21: Induction Generator](T-21_Induction_Generator.md)

### DFRT: Pulsating Field Decomposition

$$\Phi = \frac{\Phi_m}{2}\sin(\omega t - \theta) + \frac{\Phi_m}{2}\sin(\omega t + \theta)$$

Slip for forward field: $s_f = s$. Slip for backward field: $s_b = 2-s$.

- [T-22: DFRT & 1-Phase IM](T-22_DFRT_and_1Phase_IM.md)

### Capacitor-Start: Max Starting Torque

$$X_C = X_a + R_a\tan(90° - \phi_m), \qquad C = \frac{1}{2\pi f X_C}$$

- [T-23: 1-Phase IM Starting Methods](T-23_1Phase_Starting_Methods.md)

---

## Quick Number Reference

| Quantity | Typical Range |
|:---|:---|
| Full-load slip | 2-5% |
| No-load current | 25-40% of rated |
| Starting current (DOL) | 5-8x rated |
| Power factor (full load) | 0.8-0.88 lagging |
| Power factor (no load) | 0.08-0.2 lagging |
| Efficiency (large motor) | 85-95% |
| Starting torque (squirrel-cage) | 1.5-2x FL |
| Starting torque (cap-start) | 2-4x FL |
| Breakdown torque | 2-3x FL |

---

[🏠 Index](00_Index.md)
