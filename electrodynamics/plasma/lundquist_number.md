# Lundquist Number

The Lundquist number \(S\) is a dimensionless parameter that compares
magnetic field advection by the plasma flow to magnetic diffusion
due to finite resistivity. It is central to magnetic reconnection,
current-sheet formation, and many fusion/plasma regimes.

---

## 1) Definition

A common definition is

\[
S = \frac{\mu_0 L V_A}{\eta}
\]

where:
- \( \mu_0 \) is the permeability of free space
- \( L \) is a characteristic macroscopic length scale
- \( V_A \) is the Alfvén speed
- \( \eta \) is the plasma resistivity (SI units: \(\Omega\cdot\text{m}\))

**Important:** \(S\) is **dimensionless**.

---

## 2) Alfvén Speed

\[
V_A = \frac{B}{\sqrt{\mu_0 \rho}}
\]

with magnetic field \(B\) and mass density \(\rho\).

Interpretation: \(V_A\) is the characteristic wave/communication speed
for disturbances in a magnetized plasma.

---

## 3) Diffusion vs Advection Timescales

Magnetic diffusion time (resistive timescale):

\[
\tau_R \sim \frac{\mu_0 L^2}{\eta}
\]

Alfvén/advection time:

\[
\tau_A \sim \frac{L}{V_A}
\]

Taking the ratio:

\[
\frac{\tau_R}{\tau_A} \sim \frac{\mu_0 L V_A}{\eta} = S
\]

So:

\
