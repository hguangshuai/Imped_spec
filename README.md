# Impedance analysis for EIS sample and Piezoelectric materials

This repository focuses on various calculations related to **Impedance (Z)**, **Admittance (Y)**, **EIS fitting** (Electrochemical Impedance Spectroscopy), and **piezoelectric effects**(Electromechanical Impedance). The code implements key concepts in impedance analysis and provides tools for analyzing data, particularly in circuits and materials where such phenomena are observed.

## Key Concepts

### 1. Impedance ($Z$) and Admittance ($Y$)
Impedance is a complex number used to describe the opposition to alternating current (AC) in a circuit, consisting of both a real part (resistance) and an imaginary part (reactance).

- **Impedance Formula**:
  
  $$Z = R + jX$$
  
  Where:
  - $R$ = real part of impedance (resistance, in Ohms),
  - $X$ = imaginary part of impedance (reactance, in Ohms),
  - $j$ = imaginary unit ($j^2 = -1$).

- **Admittance Formula** (reciprocal of impedance):

  $$Y = \frac{1}{Z} = G + jB$$

  Where:
  - $G$ = conductance (real part of admittance, in Siemens),
  - $B$ = susceptance (imaginary part of admittance, in Siemens).

### 2. Electrochemical Impedance Spectroscopy (EIS) Fitting
EIS is a powerful technique used to study the electrical properties of materials and interfaces by applying a small AC voltage and measuring the resultant current. It is particularly useful for analyzing batteries, fuel cells, corrosion, and biological systems.

- **EIS Modeling**: EIS data can be modeled using an equivalent circuit that mimics the real electrochemical system. The most common elements in such circuits include resistors, capacitors, inductors, and constant phase elements (CPEs).

- **EIS Fitting**: Fitting EIS data involves optimizing the parameters of an equivalent circuit model to best match the experimental impedance data across various frequencies. Tools such as ZView, and Python libraries like `scipy.optimize` are used for this purpose.

- **Common Parameters**:
  - **Solution Resistance (Rs)**: The resistance of the electrolyte solution.
  - **Charge Transfer Resistance (Rct)**: The resistance associated with electrochemical reactions at the electrode-electrolyte interface.
  - **Double Layer Capacitance (Cdl)**: The capacitance formed by the separation of charge at the electrode-electrolyte interface.

### 3. Piezoelectric Effect
The piezoelectric effect describes the phenomenon where certain materials generate an electric charge in response to applied mechanical stress. This property is commonly used in sensors, actuators, and energy harvesting systems.

- **Direct Piezoelectric Effect**: When mechanical stress is applied, the material generates a voltage.
  
- **Inverse Piezoelectric Effect**: When a voltage is applied, the material undergoes mechanical deformation.

Piezoelectric materials are often characterized by their impedance and admittance, and their response to alternating electric fields is of particular interest in the study of resonance behavior and energy dissipation.

### 4. Conversion between Impedance and Admittance
- **Conductance ($G$)**: 

  $$G = \frac{R}{R^2 + X^2}$$

- **Susceptance ($B$)**: 

  $$B = -\frac{X}{R^2 + X^2}$$

- **Phase Angle ($\theta$)**: The phase angle describes the relationship between resistive and reactive components of impedance:

  $$\theta = \arctan\left(\frac{X}{R}\right)$$

  And in degrees:

  $$\theta_{\text{degrees}} = \theta \times \left(\frac{180}{\pi}\right)$$

### 5. RMSD Calculation (Root Mean Square Deviation)
The **RMSD** is used to evaluate the difference between experimental data and model predictions. It is often expressed as a percentage:

$$
\text{RMSD} (\%) = \sqrt{ \frac{ \sum_{i=1}^{N} (G_i - G_{\text{bl}})^2 }{ \sum_{i=1}^{N} (G_{\text{bl}})^2 } }
$$

Where:
- $G_i$ is the test data value (e.g., resistance values $R$),
- $G_{\text{bl}}$ is the baseline value,
- $N$ is the total number of data points.

## Project Structure
- **`Impedance_deb.ipynb`**: This Jupyter Notebook contains the core calculations for impedance, admittance, and EIS fitting. It also demonstrates the RMSD calculation for comparing experimental data with theoretical models.
  
- **Data Files**: The repository may contain impedance data (e.g., CSV files) used for analysis.

## How to Run

### 1. Clone the Repository
Use the following command to clone the repository:
```bash
git clone https://github.com/hguangshuai/Imped_spec.git
