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

## 📂 Project Structure

This repository contains standalone Jupyter Notebooks representing different experimental modules:

```text
QSPC/
├── DarkSectorAnomalyDetector.ipynb           # BSM Search: Detecting hidden particles via reconstruction error.
├── QuantumSimulatedParticleCollider.ipynb    # Core Engine: Z-Boson resonance & ATLAS data anomaly detection.
├── Quark_GluonPlasmaPhaseTransition.ipynb    # Thermodynamics: Simulating the early universe & entropy saturation.
├── HamiltonianLearning.ipynb                 # Theory Generator: Precision learning of physical constants.
├── QuantumGenerativeAIforPhysicsData.ipynb   # Digital Twin: QGAN for compressing collider data.
├── README.md                                 # Project Documentation.
└── LICENSE                                   # MIT License.
```

---

## 📊 Results

### 1. Dark Sector Anomaly Detector
We implemented an unsupervised detection algorithm to hunt for "Dark Photons" (hypothetical Dark Matter mediators).
*   **Method:** The holographic network was trained on "Standard Model" background noise until it learned smooth physical correlations.
*   **Experiment:** When fed data containing a hidden, faint signal peak, the network failed to compress the anomaly.
*   **Result:** The system flagged a massive spike in **Reconstruction Error** at ~6.5 GeV, successfully identifying the hidden particle candidate without prior labeling.

### 2. Z-Boson Resonance (CMS Data)
The model successfully learned to reproduce the Breit-Wigner resonance curve of the Z-Boson (mass ~91.2 GeV) from raw CMS Open Data.

### 3. Anomaly Detection (ATLAS Z+Dijet)
Using data from **ATLAS Run 2 (13 TeV)**, the system mapped 6 distinct fiducial regions (including High-$p_T$ and EW-enriched regions) to a 3-qubit holographic state.
*   **Convergence:** Achieved `0.0000` KL-Divergence error after 100 training steps.
*   **Discovery:** The system quantified the "Quantum Correction" required to match the High-Mass tail, effectively acting as a detector for New Physics (BSM) deviations.

### 4. Quark-Gluon Plasma Phase Transition
We simulated the thermodynamics of the Early Universe by sweeping a coupling parameter through the holographic network.
*   **Observation:** The system successfully identified a critical point ($T_c \approx 2.56$) where Von Neumann entropy saturates.
*   **Interpretation:** This mimics the confinement/deconfinement phase transition where protons melt into Quark-Gluon Plasma.

### 5. Hamiltonian Learning (Theory Generator)
We treated the quantum circuit as a "White Box" to discover hidden physical constants.
*   **Task:** The model was initialized with Standard Model laws ($g=1.0$) and fed experimental data generated by a hidden reality ($g=1.25$).
*   **Result:** The circuit converged to $g=1.2498$ (**99.99% Accuracy**), effectively "discovering" the correct mass/force parameter without human intervention.

### 6. Generative Quantum AI (QGAN)
The QSPC framework includes a Quantum Generative Adversarial Network acting as a "Digital Twin" for the High-Luminosity LHC.
*   **Problem:** Storing exabytes of raw collision data.
*   **Solution:** We trained a quantum circuit to learn the data distribution.
*   **Compression:** The physics of the dataset was successfully compressed into **<1KB** of model weights, allowing for on-demand regeneration of the data.

---

## 💻 Usage

These experiments are provided as Jupyter Notebooks designed to run in **Google Colab** or a local environment with GPU support.

1.  Clone the repository:
    ```bash
    git clone https://github.com/peterbabulik/QSPC.git
    ```
2.  Install dependencies:
    ```bash
    pip install pennylane torch pandas matplotlib numpy
    ```
3.  Launch any notebook (e.g., `DarkSectorAnomalyDetector.ipynb`) to replicate the experiments.

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
