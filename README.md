Qubit Decoherence & Information Theory Simulation using QuTiP

This repository contains a comprehensive suite of simulations analyzing the open quantum system dynamics of a single qubit under environmental noise (pure dephasing). Using the QuTiP (Quantum Toolbox in Python) library, these scripts solve the Lindblad master equation to investigate how quantum states transition from pure to mixed states, tracking both physical state evolution and information-theoretic metrics.

Physics & Information Theory Background

All simulations initialize a qubit in the equal superposition state: $$|\psi_0\rangle = |+\rangle = \frac{1}{\sqrt{2}}(|0\rangle + |1\rangle)$$

When a quantum system interacts with its environment, it undergoes decoherence. We model pure dephasing using the Pauli-Z operator ($\sigma_z$) as a collapse operator scaled by the decoherence rate $\sqrt{\gamma}$.
This destroys the off-diagonal phase information of the density matrix $\rho$ without changing the energy level populations.

To quantify this loss of quantum information, the scripts track two primary metrics over time:

1. Purity: Measures how close a state is to being a pure state.
   $$\gamma_{\text{purity}} = \text{Tr}(\rho^2)$$
   Pure State: $\text{Tr}(\rho^2) = 1$
   Maximally Mixed 2-Level State: $S = \ln(2) \approx 0.693$

2.von Neumann Entropy: Measures the lack of information (or uncertainty) about the quantum state.$$S = -\text{Tr}(\rho \ln \rho)$$
  Pure State: $S = 0$
  Maximally Mixed 2-Level State: $S = \ln(2) \approx 0.693$

