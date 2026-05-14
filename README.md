# Nonlinear Vibration Digital Lab

Interactive engineering dashboard for exploring nonlinear vibration dynamics, harmonic balance methods, resonance behavior, spectral harmonics, and phase-space motion using a forced Duffing oscillator model.

---

# Overview

This project is an interactive browser-based nonlinear vibration simulator designed for:

- engineering education
- nonlinear dynamics visualization
- vibration analysis exploration
- harmonic balance demonstration
- resonance and instability studies
- FFT and spectral analysis
- research prototyping

The application combines:
- first-harmonic Harmonic Balance Method (HBM)
- numerical Runge–Kutta integration
- live FFT analysis
- resonance branch visualization
- animated mechanical response
- engineering interpretation dashboard

The simulator is fully client-side and runs directly in a modern web browser.

---

# Features

## Nonlinear Duffing Oscillator Model

The system solves:

```text
m x¨ + c x˙ + kx + αx³ = F₀ sin(ωt)
```

where:

| Parameter | Description |
|---|---|
| m | mass |
| c | damping coefficient |
| k | linear stiffness |
| α | cubic nonlinear stiffness |
| F₀ | forcing amplitude |
| ω | forcing frequency |

---

## Implemented Functionality

### Harmonic Balance Method (HBM)

- first-harmonic approximation
- nonlinear algebraic residual solving
- multiple-root detection
- approximate branch classification

### Numerical Simulation

- RK4 time integration
- steady-state extraction
- numerical/HBM comparison

### Spectral Analysis

- live FFT spectrum
- harmonic identification
- third-harmonic indicator

### Visualization

- animated nonlinear spring-mass system
- harmonic forcing vector
- phase portrait
- amplitude-frequency response
- resonance branch visualization

### Engineering Dashboard

- damping ratio
- frequency ratio
- RMS approximation error
- dominant spectral peak
- automated engineering interpretation

---

# Screenshots

## Amplitude-Frequency Response

Features:
- hardening and softening nonlinearities
- jump regions
- multiple HBM roots
- resonance bending

## FFT Spectrum

Features:
- dominant forcing frequency
- harmonic growth
- nonlinear spectral content

## Mechanical Visualization

Features:
- conceptual nonlinear spring-mass animation
- harmonic forcing vector

---

# Physics Notes

This project uses a first-harmonic harmonic balance approximation.

The stability indicators shown in the dashboard are:
- approximate
- educational
- not equivalent to Floquet analysis or numerical continuation methods

The simulator is intended for:
- educational visualization
- nonlinear dynamics exploration
- engineering demonstrations
- research prototyping

---

# Technology Stack

## Frontend

- HTML5
- CSS3
- JavaScript

## Visualization

- Plotly.js
- HTML5 Canvas

## Numerical Methods

- Harmonic Balance Method
- Runge–Kutta 4th Order Integration
- Discrete Fourier Transform

---

# Running the Project

## Option 1 — Open Directly

Simply open:

```text
nonlinear_vibration_digital_lab_QA_checked.html
```

in a modern browser.

Recommended browsers:
- Chrome
- Edge
- Firefox

---

## Option 2 — Local Server

Python:

```bash
python -m http.server 8000
```

then open:

```text
http://localhost:8000
```

---

# Example Use Cases

## Engineering Education

- resonance visualization
- nonlinear systems courses
- vibration analysis labs
- harmonic balance demonstrations

## Research Prototyping

- nonlinear response exploration
- resonance jump studies
- harmonic analysis

## Condition Monitoring Concepts

Potential future extension toward:
- rotating machinery diagnostics
- fault simulation
- digital twins
- electromechanical coupling
- predictive maintenance systems

---

# Future Improvements

Potential future extensions:

```text
- Floquet stability analysis
- continuation methods
- bifurcation diagrams
- Poincaré sections
- chaos detection
- Lyapunov exponents
- multi-DOF systems
- gearbox dynamics
- bearing fault models
- rotor imbalance models
- electromechanical coupling
- AI-assisted diagnostics
- WebGL / Three.js visualization
```

---

# Repository Structure

```text
project/
│
├── nonlinear_vibration_digital_lab_QA_checked.html
├── README.md
└── preview.png
```

---

# Author

Developed by Iurii Storozhenko

Research interests:
- nonlinear dynamics
- vibration analysis
- condition monitoring
- wind turbine diagnostics
- electrical machine modeling
- digital twin systems
- engineering education technology

---

# License

This project is provided for:
- educational use
- research exploration
- engineering demonstrations

Add your preferred open-source license:
- MIT
- Apache 2.0
- GPL
- proprietary license

depending on your intended usage.
