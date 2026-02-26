# Renewable-H2-Electrolyzer-Model

## 🧪 Overview
This repository hosts a simplified Python model for simulating a Proton Exchange Membrane (PEM) electrolyzer, a key technology for producing green hydrogen ($H_2$) from renewable energy sources. The model aims to demonstrate the fundamental principles of electrolysis efficiency and hydrogen production rates under varying power inputs from renewable sources like solar or wind.

## ✨ Features
* **Energy Balance Calculation:** Determines the energy required for the electrolysis process.
* **Faraday Efficiency:** Estimates the ratio of actual hydrogen produced to the theoretical maximum.
* **Production Rate:** Calculates the hourly $H_2$ output in Nm$^3$/hr.
* **Input Variability:** Allows for adjustment of voltage, current, temperature, and renewable energy profiles.

## ⚙️ How it Works
The simulation is based on the following key equations:

### 1. **Theoretical Voltage ($E_{rev}$)**
The reversible voltage, or thermoneutral voltage, required to split water:
$$E_{rev} = E_0 + \frac{RT}{nF} \ln\left(\frac{a_{H_2} a_{O_2}^{0.5}}{a_{H_2O}}\right)$$
*Where:*
* $E_0$ is the standard electrode potential (1.229 V).
* $R$ is the ideal gas constant.
* $T$ is the temperature in Kelvin.
* $n$ is the number of electrons transferred (2 for water splitting).
* $F$ is Faraday's constant.
* $a_i$ are activities of the species.

### 2. **Cell Voltage ($V_{cell}$)**
Actual cell voltage considers overpotentials:
$$V_{cell} = E_{rev} + \eta_{act} + \eta_{ohm} + \eta_{conc}$$
*Where:*
* $\eta_{act}$ is activation overpotential.
* $\eta_{ohm}$ is ohmic overpotential.
* $\eta_{conc}$ is concentration overpotential.
* *For this simplified model, we use a fixed efficiency factor.*

### 3. **Faraday Efficiency ($\eta_F$)**
The ratio of the actual amount of hydrogen produced to the theoretical amount predicted by Faraday's laws. For PEM electrolyzers, it typically ranges from 95-99%.

### 4. **Hydrogen Production Rate ($Q_{H_2}$)**
Calculated using the current, Faraday's constant, number of electrons, and Faraday efficiency:
$$Q_{H_2} = \frac{I \cdot \eta_F}{nF} \cdot \frac{RT}{P} \quad (\text{m}^3/\text{s at STP})$$
*(Converted to Nm$^3$/hr for practical representation)*

## 🚀 Getting Started

### Prerequisites
* Python 3.x

### Installation
No specific installation is required beyond Python. The model uses standard libraries.

### Running the Simulation
1.  Clone this repository:
    ```bash
    git clone [https://github.com/your-username/Renewable-H2-Electrolyzer-Model.git](https://github.com/your-username/Renewable-H2-Electrolyzer-Model.git)
    cd Renewable-H2-Electrolyzer-Model
    ```
    *(Note: For your purposes, you don't need to run this command. You'll upload the file directly.)*

2.  Execute the Python script:
    ```bash
    python electrolyzer_model.py
    ```

## 📄 File Structure
* `electrolyzer_model.py`: The main Python script containing the simulation logic.
* `README.md`: This documentation file.

## 🤝 Contributing
Feel free to fork the repository and propose enhancements, especially regarding detailed electrochemical modeling or integration with renewable energy profiles.

## 📝 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
