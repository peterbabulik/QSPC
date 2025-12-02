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


## 📂 Project Structure

This repository contains standalone Jupyter Notebooks representing different experimental modules:

```text
QSPC/
├── DarkSectorAnomalyDetector.ipynb           # BSM Search: Detecting hidden particles via reconstruction error.
├── QuantumSimulatedParticleCollider.ipynb    # Core Engine: Z-Boson resonance & ATLAS data anomaly detection.
├── Quark_GluonPlasmaPhaseTransition.ipynb    # Thermodynamics: Simulating the early universe & entropy saturation.
├── HamiltonianLearning.ipynb                 # Theory Generator: Precision learning of physical constants.
├── HL_LHC_Predictor.ipynb                    # HL-LHC Predictor: Calibrates the Universe's RAM to predict future suppression factors for HL-LHC collisions.
├── ProjectSigma5_Simulation.ipynb            # Project Sigma 5: Simulates the computational cutoff in high-energy events, exploring the "Finite Universe" theory.
├── QSPC_Neutrino_Filter_&_Computational_Mass_Spectrometer.ipynb # Neutrino Filter & Mass Spectrometer: Simulates particle impact signatures and explores the "Particle Zoo" hierarchy.
├── QSPC_on_Real_IBM_Quantum_Hardware.ipynb   # Digital Twin on IBM Hardware: Trains a Z-Boson Digital Twin model on a simulator and deploys it to real IBM Quantum hardware.
├── QuantumGenerativeAIforPhysicsData.ipynb   # Digital Twin: QGAN for compressing collider data.
├── RealHardwareCollider.ipynb                # Real Hardware Collider: Executes particle collision simulations directly on IBM Quantum hardware to measure cross-sections.
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

### 7. HL-LHC Predictor (Sigma 5 Extrapolation)
We calibrated the "Universe's RAM" using ATLAS data to predict future suppression factors at higher energies.
*   **Calibration:** Discovered Computational Cutoff Parameter (Lambda) = 0.01000.
*   **Prediction:** Simulating 3 TeV collisions (HL-LHC) yielded a suppression ratio of **0.775**.
*   **Prediction:** Simulating 4 TeV collisions yielded a suppression ratio of **0.717**.

### 8. Project Sigma 5: Finite Universe Simulation
We simulated the "Computational Cutoff" theory by mapping energy levels to quantum circuit depth on real IBM hardware.
*   **Method:** Performed an "Energy Sweep" (Circuit Depth 1-15) on the IBM Fez/Torino backend.
*   **Result:** Observed signal suppression at higher depths, consistent with the hypothesis that the universe has a finite computational limit (Babulik Inversion).

### 9. Neutrino Filter & Mass Spectrometer
We simulated the "Particle Zoo" hierarchy by toggling control qubits to represent different particle types.
*   **Neutrino Mode (Key=0):** Showed **NO entanglement**, consistent with weakly interacting particles.
*   **Electron Mode (Key=1):** Showed **HIGH entanglement**, consistent with charged particle interactions.
*   **Conclusion:** Validated the ability to toggle particle physics properties via quantum control logic.

### 10. Digital Twin on Real IBM Hardware
We trained a Z-Boson generative model on a simulator and successfully deployed it to a real quantum processor.
*   **Training:** Optimized a PennyLane model to reproduce the Z-Boson resonance peak.
*   **Deployment:** Converted the model to Qiskit and executed it on **IBM Fez**.
*   **Validation:** The real hardware output successfully reconstructed the Z-Boson resonance peak, validating the "Digital Twin" concept.

### 11. Real Hardware Collider
We executed direct particle collision simulations on IBM Quantum hardware to measure interaction cross-sections.
*   **Neutrino-Neutrino:** Measured Cross-Section = **0.0345** (Low interaction).
*   **Neutrino-Electron:** Measured Cross-Section = **0.0465**.
*   **Electron-Electron:** Measured Cross-Section = **0.9247** (High interaction).

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
