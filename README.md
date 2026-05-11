# Harmonic Balance Simulator — Nonlinear Vibration Analysis

**Harmonic Balance Simulator** is a browser-based interactive tool for studying the harmonic balance method applied to a forced nonlinear vibration system.

The simulator focuses on a single-degree-of-freedom Duffing-type oscillator with cubic stiffness nonlinearity. It allows users to change model parameters, compute the first-harmonic harmonic balance solution, and compare the result with direct numerical time-domain simulation.

---

## Governing Equation

The model is based on the forced nonlinear vibration equation:

m x'' + c x' + kx + alpha x^3 = F0 sin(omega t)

where:

| Symbol | Description |
|---|---|
| `m` | Mass |
| `c` | Damping coefficient |
| `k` | Linear stiffness |
| `alpha` | Cubic nonlinear stiffness coefficient |
| `F0` | Harmonic excitation force amplitude |
| `omega` | Excitation frequency |
| `x` | Displacement |
| `x'` | Velocity |
| `x''` | Acceleration |

When `alpha = 0`, the system is linear.

When `alpha > 0`, the system has hardening stiffness.

When `alpha < 0`, the system has softening stiffness.

---

## Harmonic Balance Approximation

The simulator uses the first-harmonic approximation:

x(t) ≈ A sin(omega t - phi)

For the cubic nonlinear term, the fundamental harmonic approximation is:

x^3 ≈ (3/4) A^3 sin(omega t - phi)

Substituting into the equation of motion gives the harmonic balance amplitude equation:

F0^2 = A^2 [ (k + (3/4) alpha A^2 - m omega^2)^2 + (c omega)^2 ]

The phase lag is computed as:

phi = atan2(c omega, k + (3/4) alpha A^2 - m omega^2)

---

## Model Inputs

The interactive simulator allows users to change:

- Mass
- Damping
- Linear stiffness
- Cubic nonlinear stiffness
- Force amplitude
- Excitation frequency
- Frequency sweep range
- Numerical comparison mode

---

## Preset Scenarios

The app includes several preset examples:

- Linear reference
- Hardening Duffing oscillator
- Softening Duffing oscillator
- Strong nonlinear response

These presets help demonstrate how the harmonic balance solution changes when nonlinear stiffness is introduced.

---

## Analysis and Visualization

The simulator generates several plots and metrics.

### Harmonic Balance Analysis

- Amplitude-frequency response
- Multiple algebraic amplitude branches
- Phase-frequency response
- Harmonic balance residual at the selected excitation frequency
- Number of amplitude roots at the selected frequency

### Numerical Comparison

The simulator also compares the harmonic balance solution with direct numerical simulation using the same nonlinear equation of motion.

The numerical comparison includes:

- Steady-state time response
- Numerical response vs. harmonic balance approximation
- Phase portrait
- Harmonic balance ellipse approximation
- Approximation error

---

## Numerical Method

The nonlinear equation is converted into the first-order system:

x_dot = v

v_dot = (F0 sin(omega t) - c v - k x - alpha x^3) / m

The direct numerical solution is computed using a fixed-step fourth-order Runge-Kutta method.

---

## What the Simulator Shows

The simulator helps visualize several important nonlinear vibration concepts:

- Linear resonance
- Hardening stiffness behavior
- Softening stiffness behavior
- Frequency-response bending
- Multiple harmonic balance roots
- Jump-type nonlinear response behavior
- Difference between harmonic balance approximation and numerical simulation
- Limitations of the single-harmonic approximation

---

## Important Notes and Limitations

The harmonic balance implementation uses a **single-harmonic approximation**.

This means the response is assumed to be dominated by the fundamental excitation frequency. Higher harmonics are neglected.

The amplitude-frequency branches shown in the app are algebraic harmonic balance roots. They are not automatically classified as stable or unstable.

For strong nonlinear behavior, the response may include:

- Higher harmonics
- Subharmonics
- Superharmonics
- Jump phenomena
- Multi-periodic response
- Chaotic response

In such cases, the single-harmonic harmonic balance approximation may differ from the direct numerical simulation.

For more advanced analysis, multi-harmonic harmonic balance, continuation methods, or direct numerical bifurcation analysis may be required.

This project is intended as an educational and visualization tool. It is not certified engineering design software.

---

## Technologies Used

- HTML
- CSS
- JavaScript
- Plotly.js
- MathJax

---

## Suggested Repository Name

Recommended repository name:

harmonic-balance-simulator

Alternative names:

- nonlinear-vibration-harmonic-balance
- duffing-harmonic-balance-simulator
- hbm-nonlinear-vibration

---

## Possible Future Improvements

Potential future improvements include:

- Multi-harmonic harmonic balance
- Stability classification of branches
- Forward and backward frequency sweeps
- Continuation-based amplitude-frequency response
- Bifurcation diagram
- Poincare section
- Lyapunov exponent estimation
- Export of plots as PNG
- Export of simulation data as CSV
- Comparison between one-harmonic and multi-harmonic solutions
- Base excitation model
- Multi-degree-of-freedom nonlinear vibration systems

---

## Educational Purpose

This project is intended for:

- Learning nonlinear vibration theory
- Understanding the harmonic balance method
- Visualizing Duffing oscillator response
- Comparing approximate analytical methods with numerical simulation
- Teaching resonance and nonlinear frequency-response behavior

It can be useful for students, instructors, researchers, and engineers interested in mechanical vibrations, nonlinear dynamics, and simulation.

---

## License

This project is released under the MIT License.

MIT License

Copyright (c) 2026 Iurii Storozhenko

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files, to deal in the software
without restriction, including without limitation the rights to use, copy,
modify, merge, publish, distribute, sublicense, and/or sell copies of the
software, and to permit persons to whom the software is furnished to do so,
subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

---

## Author

**Iurii Storozhenko**

Mechanical engineering, vibration analysis, nonlinear dynamics, dynamic systems, wind turbine diagnostics, and condition monitoring.
