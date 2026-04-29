# Fuzzy Logic Decision Support System: "To Sleep or Not to Sleep?"

## Overview
This project implements a Mamdani-type Fuzzy Inference System (FIS) designed to solve a common human dilemma: deciding whether to continue working, take a break, or go to sleep. The system processes subjective inputs—Fatigue and Task Importance—to provide a nuanced recommendation that mirrors human reasoning.

## Features
- **Linguistic Variables:** Uses 3 input sets for Fatigue and 4 for Task Importance.
- **Granular Output:** Provides 4 possible recommendations (Work, Break, Nap, Sleep).
- **Fuzzy Logic Engine:** Implemented using `scikit-fuzzy` in Python.
- **Visualization:** Generates membership function plots and a 3D Control Surface.

## Requirements
To run this project, you need Python 3.x and the following libraries:
- `numpy`: For numerical operations.
- `scikit-fuzzy`: The core fuzzy logic library.
- `matplotlib`: For generating plots.
- `networkx`: Required by the `skfuzzy.control` module.

## How It Works
1. **Fuzzification:** Converts crisp inputs (e.g., 85% fatigue) into degrees of membership in fuzzy sets.
2. **Inference:** Evaluates 12 logic rules (e.g., *IF fatigue is critical AND importance is low THEN decision is sleep*).
3. **Defuzzification:** Uses the **Centroid (Center of Gravity)** method to calculate a single crisp percentage indicating the necessity of sleep.

## Mathematical Model
- **Input 1 (Fatigue):** Range [0-100%]. Terms: *Low, Medium, Critical*.
- **Input 2 (Importance):** Range [0-10]. Terms: *Irrelevant, Low, Important, Priority*.
- **Output (Decision):** Range [0-100%]. Terms: *Work, Break, Nap, Sleep*.

## Author
Natalia Czop