# LIGO-project
# 🌠 Chirp Mass Estimation from Gravitational Wave Signal (LIGO GW150914)

**Author:** Purvasha Mathur  
**Institute:** IIT Jodhpur | BS AI & Data Science (1st Year)  
**Project Domain:** Gravitational Wave Astrophysics, Signal Processing, Python Simulation

---

## 📖 Overview

This project focuses on extracting and analyzing real gravitational wave data from the **LIGO Hanford detector**, particularly the historic event **GW150914**, to estimate the **chirp mass** of the binary black hole system. Chirp mass is a critical parameter that determines how the frequency of a gravitational wave signal increases over time — or "chirps" — as two massive objects spiral inward and merge.

Using Python libraries such as `gwpy`, `SciPy`, and `NumPy`, the project:
- Downloads LIGO time series strain data
- Applies a **Hilbert transform** to estimate **instantaneous frequency**
- Calculates **df/dt** (rate of change of frequency)
- Computes **chirp mass** using a relativistic formula

---

## 🎯 Objectives

- Understand how black hole mergers are detected via gravitational waves.
- Extract and preprocess real LIGO data using `gwpy`.
- Estimate the **chirp mass** from the signal’s frequency evolution using physics.
- Visualize the waveform, frequency, and derivative behavior.

---

## 🧠 Theoretical Background

### 🔹 What Is Chirp Mass?

When two compact objects (like black holes) spiral in and merge, they emit gravitational waves whose **frequency and amplitude increase** over time — known as a **chirp**. The chirp mass controls how rapidly the frequency changes.

### 🔹 Chirp Mass Equation:

\[
\mathcal{M} = \frac{c^3}{G} \left( \frac{5}{96 \pi^{8/3}} \cdot \frac{1}{f^{11/3}} \cdot \frac{df}{dt} \right)^{3/5}
\]

Where:
- \( f \) is the gravitational wave frequency
- \( \frac{df}{dt} \) is the rate of change of frequency
- \( G \) = gravitational constant
- \( c \) = speed of light

---

## ❓ Research Questions & ✅ Answers

| Research Question | Answer |
|-------------------|--------|
| **What is chirp mass and why is it important?** | Chirp mass is a derived parameter that governs how fast the gravitational wave frequency increases. It's crucial for estimating the masses of the objects involved. |
| **How can we extract chirp mass from real LIGO data?** | By applying Hilbert transform to find instantaneous frequency, then computing df/dt, and plugging these into the chirp mass formula. |
| **Why does the frequency increase during a merger?** | As black holes spiral closer, they orbit faster and radiate more energy — this causes both the frequency and amplitude of the wave to rise until merger. |
| **Why use Hilbert transform?** | It converts the real-valued waveform into an analytic signal, from which we can extract phase and compute instantaneous frequency smoothly. |

---

## 📊 Features

- ✅ Extracts open LIGO Hanford data for GW150914 event using `gwpy`
- ✅ Applies Hilbert transform to get phase and instantaneous frequency
- ✅ Computes \( \frac{df}{dt} \) numerically using `np.gradient()`
- ✅ Estimates **chirp mass** in solar masses
- ✅ Plots:
  - Gravitational wave strain
  - Instantaneous frequency
  - \( \frac{df}{dt} \)
  - Highlighted chirp point

---

## 🧰 Technologies Used

- **Python**
- `gwpy` – to access and process gravitational wave data  
- `NumPy` – numerical operations and gradients  
- `Matplotlib` – plotting graphs  
- `SciPy` – Hilbert transform and signal tools  
- Google Colab / Jupyter Notebook

---

## 📁 File Structure

