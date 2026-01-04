# DC SQUID

This file focuses on the practical behavior of the DC SQUID:
biasing, IV characteristics, flux modulation, and the basic ideas
behind flux-locked loop (FLL) operation.

---

## 1) Basic Structure

A DC SQUID consists of:
- a superconducting loop
- two Josephson junctions with critical currents \( I_{c1}, I_{c2} \)
- loop inductance \( L \)

In most measurement systems the SQUID is **current biased** slightly above its
critical current and the resulting voltage is measured.

---

## 2) I–V Characteristics

At zero applied flux, the effective critical current is maximal.
Applying flux modulates the critical current periodically with period \( \Phi_0 \).

Typical operating mode:
- Bias current \( I_b \gtrsim I_{c,\text{eff}}(\Phi) \)
- Measure resulting voltage \( V(\Phi) \)

The result is a **periodic voltage–flux characteristic**:
\[
V(\Phi + \Phi_0) = V(\Phi)
\]

---

## 3) Flux-to-Voltage Transfer Function

Define the small-signal transfer coefficient:

\[
V_\Phi = \frac{dV}{d\Phi}
\]

This determines the SQUID’s intrinsic flux sensitivity and directly enters the noise
performance of the system.

High performance SQUIDs are designed for large \( V_\Phi \) and low noise.

---

## 4) Role of Loop Inductance

Self-induced flux modifies the total loop flux:

\[
\Phi = \Phi_{\text{ext}} + L I_{\text{loop}}
\]

The parameter

\[
\beta_L = \frac{2 L I_c}{\Phi_0}
\]

controls screening and stability.

Design goals:
- \( \beta_L \lesssim 1 \) for low hysteresis and clean modulation
- symmetric junctions for maximal modulation depth

---

## 5) Flux-Locked Loop (FLL)

Because \( V(\Phi) \) is periodic, a DC SQUID alone is not linear over large flux ranges.
An **FLL** linearizes the response:

1. SQUID is biased at a steep slope of \( V(\Phi) \)
2. Output voltage is amplified
3. Feedback current is applied to a coil coupled to the SQUID
4. Feedback cancels changes in input flux

The measured feedback signal is then a **linear, wide-range representation of flux**.

---

## 6) Practical Considerations

Key limitations in real systems:
- junction asymmetry
- thermal noise and critical current noise
- amplifier noise in the readout chain
- magnetic interference and vibration coupling

Optimizing these determines whether a SQUID reaches fT/√Hz performance or not.

---

## Notes for future expansion

- full RSJ / RCSJ model
- dynamic behavior and bandwidth
- noise spectra and equivalent flux noise
- cryogenic implementation details
