# Decoherence in Superconducting Qubits — T1 and T2 Simulation

This repository contains simulations of **T1 relaxation** and **T2 dephasing** in superconducting qubits using Python and the [QuTiP](http://qutip.org/) framework. These processes model the dominant noise mechanisms that limit coherence in real quantum processors.


## What Are T1 and T2?

- **T1 (Energy Relaxation):** The qubit loses energy, decaying from the excited state |1⟩ to the ground state |0⟩.
- **T2 (Dephasing):** The qubit loses phase coherence due to environmental noise, causing superpositions to degrade without changing population.

In real systems, both processes happen together. This simulation helps visualize and quantify their effects on the qubit’s Bloch vector over time.


## Simulation Details

- Initial state: **|+⟩ = (|0⟩ + |1⟩)/√2**
- Simulation uses the **Lindblad master equation**
- Implements two collapse operators:
  - `destroy(2)` for T1 relaxation
  - `sigmaz()` for T2 dephasing
- Solves for and plots:
  - ⟨σ<sub>x</sub>⟩ (quantum coherence)
  - ⟨σ<sub>y</sub>⟩ (quantum coherence)
  - ⟨σ<sub>z</sub>⟩ (population difference)


## Output

The notebook generates line plots showing the decay of Bloch vector components over time due to T1 and T2 noise.

| Component           | Behavior                                      |
|--------------------|-----------------------------------------------|
| ⟨σ<sub>x</sub>⟩, ⟨σ<sub>y</sub>⟩ | Decay to 0 due to T2 (dephasing)         |
| ⟨σ<sub>z</sub>⟩            | Decays toward −1 due to T1 (relaxation) |

These reflect a transition from a coherent superposition state to a classical mixed state in |0⟩.

---

## File Included

- `T1_T2_Simulation.ipynb`: Complete notebook with code, simulation, plots, and interpretation


## How to Run

Install the dependencies:
```bash
pip install qutip matplotlib numpy

## Author

**Shiva Heidari**  
Physicist | Quantum Researcher | Qiskit Enthusiast  
GitHub: [@Shiva-Heidari](https://github.com/Shiva-Heidari)


## ⭐️ If you found this useful…

Feel free to ⭐️ star the repo or connect with me on [LinkedIn](https://www.linkedin.com/in/shiva-heidari) to collaborate or chat quantum!
