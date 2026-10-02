# Trigger-System Jitter Simulation

Python-based simulation and timing-jitter analysis developed during my internship at the **Variable Energy Cyclotron Centre (VECC)** with the **High Energy Physics (HEP) department**.

This repository contains the **initial-stage work of the project**, developed by me with the help of my project partner **Hiramoni**. The work focuses on simulating an ideal trigger system and studying the effects of different timing-jitter conditions using Python. The project was subsequently taken further through collaboration with other contributors. The later stages and associated work are **not included in this repository**.

---

## Project Overview

The project investigates the behavior of a trigger system under different timing-jitter conditions and examines how timing fluctuations affect trigger synchronization and detection.

The simulation establishes an ideal no-jitter baseline and introduces different types of timing variations at different points in the timing chain. The resulting behavior is analyzed using numerical simulations, visualizations, and statistical timing metrics.

The simulation uses a **40 MHz reference** and a **400 MHz trigger clock**, along with a defined trigger/acquisition window for evaluating the timing relationship between the input signal and trigger.

---

## Objectives

The main objectives of the project were to:

- Establish an ideal trigger-system baseline without jitter.
- Introduce different timing-jitter models.
- Study the effect of jitter on trigger synchronization.
- Compare different jitter conditions and their effects.
- Analyze timing errors resulting from jitter.
- Study jitter introduced at different points in the timing chain.
- Generate simulation datasets for different operating conditions.
- Calculate and analyze RMS and peak-to-peak timing metrics.

---

## Jitter Models

The project explores several timing-jitter conditions, including:

- **Gaussian Jitter**
- **Periodic / Deterministic Jitter**
- **Data-Dependent Jitter**
- **Duty-Cycle Distortion**
- **Bounded Uncorrelated Jitter**

These models are applied to different parts of the simulated timing system to study their individual and combined effects.

---

## Simulation Configurations

The simulations investigate jitter introduced into different parts of the timing system, including:

- External input pulse
- 40 MHz clock
- 400 MHz clock
- Multiple timing signals simultaneously

### Main Simulation Cases

**Case 1 — Ideal Clock + Jittered External Pulse**

The trigger clock remains ideal while timing jitter is introduced into the external input pulse.

**Case 2 — Jittered Clock + Ideal External Pulse**

The external input remains ideal while timing jitter is introduced into the trigger clock.

**Case 3 — Jittered Clock + Jittered External Pulse**

Both the trigger clock and external input pulse contain timing jitter.

These cases are used to study how the location and combination of timing jitter affect the resulting trigger behavior.

---

## Simulation and Analysis

The simulations were developed in Python to generate timing signals, introduce controlled jitter, and analyze the resulting trigger behavior.

The project includes large-scale simulation runs and generates datasets containing quantities such as:

- Trigger timing
- Input timing
- Jitter values
- Detection/error counts
- Mean errors
- RMS jitter
- Peak-to-peak jitter
- Other calculated timing metrics

The generated simulation and metric datasets are stored as CSV files in the `data/raw/` directory.

---

## Tools & Technologies

- **Python**
- **NumPy**
- **Pandas**
- **Matplotlib**
- **Plotly**
- **Google Colab**
- **Google Drive**

---

## Repository Structure

```text
lhc-trigger-jitter-simulation/
│
├── README.md
├── LICENSE
├── .gitignore
├── requirements.txt
│
├── notebooks/
│   └── Jitter_Ideal_Trigger_v34.ipynb
│
├── data/
│   └── raw/
│       └── simulation and metric CSV files
│
└── results/
