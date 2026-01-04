# RF SQUID

An RF SQUID consists of a superconducting loop interrupted by a single
Josephson junction and coupled to a resonant RF circuit (tank circuit).
It converts magnetic flux into changes in impedance or resonance behavior.

---

## 1) Basic Concept

Components:
- superconducting loop with inductance \( L \)
- one Josephson junction (critical current \( I_c \))
- RF tank circuit (inductor + capacitor)
- RF drive and detection electronics

Unlike the DC SQUID, the RF SQUID is usually **not DC biased**.
Instead, it is driven and read out through an **AC electromagnetic coupling**.

---

## 2) Nonlinear Inductance

The Josephson junction behaves as a nonlinear inductance:

\[
L_J(\delta) = \frac{\Phi_0}{2\pi I_c \cos \delta}
\]

The effective inductance of the SQUID loop becomes flux dependent.
This shifts the resonance frequency of the coupled tank circuit.

---

## 3) Coupling to the Tank Circuit

The SQUID is inductively coupled to a high-Q resonator:

- Input RF excites the tank
- SQUID modifies tank impedance
- Reflected or transmitted RF power depends on applied flux

Thus:
\[
\Phi_{\text{ext}} \rightarrow Z_{\text{tank}}(\Phi) \rightarrow V_{\text{RF,out}}
\]

---

## 4) Screening Parameter

A key parameter is:

\[
\beta_L = \frac{2 \pi L I_c}{\Phi_0}
\]

Regimes:
- \( \beta_L < 1 \): non-hysteretic, smooth response
- \( \beta_L > 1 \): hysteretic behavior, multivalued states

Most precision RF SQUIDs operate near or below \( \beta_L \approx 1 \).

---

## 5) Readout Modes

Common detection methods:
- amplitude modulation of the RF signal
- phase modulation
- frequency shift detection

These allow very sensitive flux detection with simpler fabrication
than DC SQUIDs.

---

## 6) Advantages and Limitations

Advantages:
- only one junction → easier fabrication
- simpler cryogenic wiring
- useful for array integration

Limitations:
- generally higher noise than optimized DC SQUIDs
- more sensitive to RF interference and microphonics

---

## Notes for future expansion

- noise sources and noise matching
- RF electronics and demodulation schemes
- comparison of RF vs DC SQUID sensitivity and bandwidth
