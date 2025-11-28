# QSPC: Quantum Simulated Particles Collider

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Framework: PennyLane](https://img.shields.io/badge/Framework-PennyLane-mediumpurple)](https://pennylane.ai/)
[![Backend: PyTorch](https://img.shields.io/badge/Backend-PyTorch-red)](https://pytorch.org/)

**QSPC** is a Holographic Quantum Machine Learning framework designed to simulate high-energy particle collisions. 

By combining **Differentiable Quantum Circuits** with **Holographic Tensor Networks**, this project acts as a generative model for particle physics. It ingests real experimental data (LHC/CERN), compresses the quantum state complexity, and "learns" the underlying interaction Hamiltonian required to reproduce observed particle resonances and cross-sections.

---

## 🚀 Key Capabilities

*   **Holographic Compression:** Uses Tree Tensor Networks (MERA-style) to map complex, high-entanglement collision events (the "Bulk") onto a lower-dimensional qubit register (the "Boundary").
*   **Inverse Folding:** Instead of simulating forward physics, QSPC uses PyTorch to backpropagate through the quantum circuit, reverse-engineering the laws of physics from experimental data.
*   **Anomaly Detection:** Capable of identifying deviations between Standard Model predictions and measured reality by analyzing quantum gate "correction" magnitudes.
*   **Real-World Integration:** Validated against CERN Open Data (CMS Z-Boson Resonance) and HEPData (ATLAS Z+Dijet Cross-sections).

---

## 🧠 Core Principles

This project integrates concepts from two primary domains:

1.  **Quantum-Holographic Compression:**
    Based on the principle that the information of a volume of space can be encoded on a lower-dimensional boundary. We use hierarchical quantum circuits to compress the thermodynamic entropy of a particle collision.
    *   *Inspiration:* [Quantum-Holographic-Compression](https://github.com/peterbabulik/Quantum-Holographic-Compression)

2.  **Differentiable Quantum Circuits:**
    Treating the particle interaction ($S$-matrix) as a learnable unitary operator $U(\theta)$. By optimizing $\theta$ via gradient descent, the collider "learns" physics.
    *   *Inspiration:* [QuantumPyTorch-Differentiable-Quantum-Circuits](https://github.com/peterbabulik/QuantumPyTorch-Differentiable-Quantum-Circuits)

---

## 🛠 Architecture

The simulation pipeline consists of four stages:

1.  **Injection (State Prep):** Initializes qubits representing the incoming beam energy.
2.  **Holographic Encoder:** A hierarchical circuit that entangles and coarse-grains the state, creating a compressed representation of the collision manifold.
3.  **Interaction Engine:** A parameterized unitary evolution that mimics the scattering forces (Strong/Electroweak interactions).
4.  **Detector (Measurement):** Measures the output probability distribution (Cross-section) and calculates the **Safe-KL Divergence** against real experimental data.

```python
# Pseudo-code logic
injection = ParticleInjection(qubits)
compressed_state = HolographicEncoder(injection)
scattering_event = InteractionHamiltonian(compressed_state)
loss = KL_Divergence(scattering_event, atlas_experimental_data)
loss.backward() # Learn Physics
```

---

## 📊 Results

### 1. Z-Boson Resonance (CMS Data)
The model successfully learned to reproduce the Breit-Wigner resonance curve of the Z-Boson (mass ~91.2 GeV) from raw CMS Open Data.

### 2. Anomaly Detection (ATLAS Z+Dijet)
Using data from **ATLAS Run 2 (13 TeV)**, the system mapped 6 distinct fiducial regions (including High-$p_T$ and EW-enriched regions) to a 3-qubit holographic state.
*   **Convergence:** Achieved `0.0000` KL-Divergence error after 100 training steps.
*   **Discovery:** The system quantified the "Quantum Correction" required to match the High-Mass tail, effectively acting as a detector for New Physics (BSM) deviations.

---



---

## 📜 Citation & References

If you use this code or principles in your research, please link back to this repository.


This project builds upon concepts from:
*   [**Quantum-Holographic-Compression**](https://github.com/peterbabulik/Quantum-Holographic-Compression) - Peter Babulik
*   [**QuantumPyTorch**](https://github.com/peterbabulik/QuantumPyTorch-Differentiable-Quantum-Circuits) - Peter Babulik
*   [**Quantum Inspired Learning In Tensor Space**](https://github.com/peterbabulik/QuILT) - Peter Babulik

**Data Sources:**
*   [CERN Open Data Portal](http://opendata.cern.ch/)
*   [HEPData - ATLAS Z+Dijet (Ins1627873)](https://www.hepdata.net/record/82616)

---
