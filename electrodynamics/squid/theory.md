# SQUID Theory Notes

These notes summarize the core physics behind SQUIDs (Superconducting Quantum Interference Devices),
with emphasis on concepts useful for practical measurement systems: Josephson relations, flux
quantization, and how interference produces a flux-to-voltage (or flux-to-impedance) transducer.

---

## 1) Ingredients

A SQUID combines:

- A **superconducting loop** → supports a macroscopic phase and quantized flux states
- One or two **Josephson junctions** → provide a nonlinear phase-dependent current
- A **readout** (DC bias + amplifier, or RF tank circuit) → converts flux modulation into a measurable signal

Two common types:

- **DC SQUID:** two junctions in a loop, typically voltage-biased or current-biased in a flux-locked loop.
- **RF SQUID:** one junction in a loop, coupled to an RF resonant (tank) circuit.

---

## 2) Josephson Relations (DC and AC effects)

For a Josephson junction with phase difference \( \delta \):

**Current-phase relation (DC Josephson effect):**
\[
I_s = I_c \sin(\delta)
\]

**Voltage-phase relation (AC Josephson effect):**
\[
V = \frac{\Phi_0}{2\pi}\,\frac{d\delta}{dt}
\]

where the flux quantum is:
\[
\Phi_0 = \frac{h}{2e} \approx 2.0678\times10^{-15}\ \text{Wb}
\]

Interpretation:
- A **static** phase difference supports a **supercurrent** with zero voltage.
- A **nonzero voltage** implies a **time-evolving phase**, producing oscillations at
  \[
  f = \frac{2e}{h}V = \frac{V}{\Phi_0}
  \]

---

## 3) Flux Quantization in a Superconducting Loop

In a simply connected superconducting loop, the phase must be single-valued around the loop, giving:

\[
\oint \nabla \phi \cdot d\ell = 2\pi n
\]

This leads to quantization of the fluxoid; in many SQUID contexts this is summarized as the
effective constraint that the loop prefers flux states near:

\[
\Phi \approx n\Phi_0
\]

In practice, finite inductance and junction dynamics mean the loop can occupy metastable
states and switch between them depending on parameters and noise.

---

## 4) Why SQUIDs Are Interferometers

In a **DC SQUID**, the two junction supercurrents add like phasors. The applied flux changes the
relative phase around the loop, so the maximum supercurrent (effective critical current) becomes
flux-dependent:

\[
I_{c,\text{eff}}(\Phi) \approx 2 I_c \left|\cos\left(\pi\frac{\Phi}{\Phi_0}\right)\right|
\]
(ideal symmetric, negligible inductance limit)

This periodic dependence (period \( \Phi_0 \)) is the basis of SQUID sensing: external flux modulates the
junction behavior, which modulates voltage or impedance at fixed bias.

---

## 5) Inductance, Screening, and the Parameter \( \beta_L \)

Loop inductance \( L \) matters because currents in the loop generate self-flux:

\[
\Phi = \Phi_{\text{ext}} + L I_{\text{loop}}
\]

A common dimensionless parameter:

\[
\beta_L = \frac{2 L I_c}{\Phi_0}
\]

- \( \beta_L \ll 1 \): “small inductance” limit, clean sinusoidal modulation, minimal hysteresis
- \( \beta_L \gtrsim 1 \): stronger screening, multivalued states, possible hysteresis and jumps

---

## 6) From Flux to Readable Signal

### DC SQUID readout (typical)
Bias near/above critical current → junctions develop voltage.
The voltage \( V(\Phi) \) becomes periodic; a **flux-locked loop (FLL)** linearizes this by applying feedback
flux to hold the SQUID at a fixed operating point.

### RF SQUID readout
A single junction loop behaves like a flux-dependent nonlinear inductor, shifting the resonance of a
tank circuit. Changes in reflected/transmitted RF power map back to flux.

---

## 7) Noise (very brief)

Practical SQUID sensitivity is often limited by:
- junction noise (thermal, shot-like in some regimes)
- amplifier noise in readout chain
- 1/f noise (materials, critical current fluctuations)
- environmental magnetic noise and vibration/microphonics (especially in cryostats)

(Expand later with noise spectra, flux noise \(S_\Phi^{1/2}\), and transfer functions.)

---

## References / Next files
- `dc_squid.md` → biasing, IV curves, FLL basics, transfer function \(dV/d\Phi\)
- `rf_squid.md` → tank circuits, coupling, demodulation
- `high_tc_squids.md` → material and fabrication tradeoffs, LN2 systems, limitations
- `references.md` → textbooks, review articles, classic SQUID papers
