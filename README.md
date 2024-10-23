# Impedance and Admittance Calculations

This repository focuses on various calculations related to **Impedance (Z)**, **Admittance (Y)**, **EIS fitting** (Electrochemical Impedance Spectroscopy), **piezoelectric effects**, and methods for **Structural Health Monitoring (SHM)** using piezoelectric materials. The code implements key concepts in impedance analysis and provides tools for analyzing data, particularly in circuits and materials where such phenomena are observed.

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

### 3. Piezoelectric Effect and SHM (Structural Health Monitoring)
The **piezoelectric effect** describes the phenomenon where certain materials generate an electric charge in response to applied mechanical stress. In the context of **Structural Health Monitoring (SHM)**, piezoelectric materials, especially using the **Electromechanical Impedance (EMI)** technique, can be employed to detect changes in structures by monitoring electrical responses under different conditions.

#### SHM Analysis Techniques
The following methods are commonly used to analyze the data obtained from EMI measurements using piezoelectric materials for SHM:

- **Statistical Analysis**: Statistical tools like mean, standard deviation, and RMSD (Root Mean Square Deviation) are used to detect anomalies in the structure by comparing the baseline impedance signatures with the current state. Statistical indices are useful for quantifying damage or changes in the system.

- **Filtering**: Filters such as low-pass, high-pass, and band-pass are applied to EMI signals to remove noise and enhance important features in the impedance data. This improves the clarity of peak detection and other signal characteristics.

- **Different Electrical Signal Analysis**: Analysis of different electrical signals (such as voltage, current, and phase) helps in characterizing the structure’s dynamic behavior. By studying how these signals vary with frequency, one can identify material degradation or structural damage.

- **Peak Feature Analysis**: Peaks in impedance and admittance spectra are often related to the resonant behavior of the structure. By monitoring the shift in peak position, height, and width, one can infer changes in the mechanical properties of the structure. Peak feature analysis is a key tool for identifying damage in SHM applications.

- **Wavelet Analysis**: Wavelet transforms provide a time-frequency representation of the signal, which is particularly useful in detecting transient events or localized damage in structures. Wavelet analysis allows for multi-resolution analysis of the EMI signals, capturing both high-frequency and low-frequency features effectively.

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
- **`Impedance_spec.ipynb`**: This Jupyter Notebook contains the core calculations for impedance, admittance, EIS fitting, and SHM analysis. It demonstrates statistical analysis, signal filtering, peak feature analysis, and wavelet analysis on EMI data.
  
- **Data Files**: The repository may contain impedance data (e.g., CSV files) used for analysis.

## How to Run

### 1. Clone the Repository
Use the following command to clone the repository:
```bash
git clone https://github.com/hguangshuai/Imped_spec.git
