# phin2
Contralateral Fin-Control Simulation Framework

A unified model linking physics, evolution, and development

This repository provides all simulation code accompanying the study:
“Contralateral control as a physically optimal and evolutionarily inevitable architecture in vertebrate motor systems” (submitted to Nature Communications, 2025).

The framework integrates:

Stage 1 – Hydrodynamic roll-stability model
Tests how contralateral versus ipsilateral fin control affects mechanical stabilization.

Stage 1.5 – Evolutionary simulation
Embeds the physical model into a genetic algorithm to test whether contralateral dominance evolves spontaneously.

Stage 2 – Developmental geometry (conceptual, analytical only)

Repository Structure
contralateral_control_framework/
├── stage1_roll_model/      # Physical model (gain optimization, sensitivity)
├── fin_evolution_sim/      # Evolutionary simulation (genetic algorithm)
└── LICENSE
# Stage 1
cd stage1_roll_model
conda env create -f environment.yml
conda activate fin_roll
python optimize_gain.py
python plotting.py

# Stage 1.5
cd ../fin_evolution_sim
conda env create -f environment.yml
conda activate fin_evo
python main_simulation.py
Outputs are saved in results/ and data/.
All parameters and equations match the manuscript Methods.

Key Results

Contralateral control (γ ≈ –1, kf ≈ 1.8) minimizes total cost J and stabilizes roll most efficiently.

Evolutionary simulations converge to the same physical optimum, forming a single global attractor.

The same configuration aligns with developmental geometry where contralateral wiring is shortest.
