# Impedance and Admittance Calculations

This repository contains calculations related to impedance and admittance in electrical circuits, including conversions between impedance and admittance, as well as phase angle calculations. The code in this repository implements these concepts and provides a framework for analyzing impedance data.

## Key Concepts

### Impedance ($Z$)
Impedance is a complex number that describes the opposition to alternating current (AC) in a circuit. It is composed of both real and imaginary components:

$$Z = R + jX$$

Where:
- $R$ is the **real part** of impedance (resistance, measured in Ohms),
- $X$ is the **imaginary part** of impedance (reactance, measured in Ohms),
- $j$ is the imaginary unit ($j^2 = -1$).

### Admittance ($Y$)
Admittance is the reciprocal of impedance and also has real and imaginary parts:

$$Y = \frac{1}{Z} = G + jB$$

Where:
- $G$ is the **conductance** (real part, measured in Siemens),
- $B$ is the **susceptance** (imaginary part, measured in Siemens).

### Key Equations
- **Conductance ($G$)**: $$G = \frac{R}{R^2 + X^2}$$
- **Susceptance ($B$)**: $$B = -\frac{X}{R^2 + X^2}$$
- **Phase Angle ($\theta$)**: $$\theta = \arctan\left(\frac{X}{R}\right)$$
- Phase angle in degrees: $$\theta_{\text{degrees}} = \theta \times \left(\frac{180}{\pi}\right)$$

### RMSD (Root Mean Square Deviation) Calculation
The RMSD in percentage is calculated using:

$$
\text{RMSD} (\%) = \sqrt{ \frac{ \sum_{i=1}^{N} (G_i - G_{\text{bl}})^2 }{ \sum_{i=1}^{N} (G_{\text{bl}})^2 } }
$$

Where:
- $G_i$ is the value from the test data (e.g., $R$ values),
- $G_{\text{bl}}$ is the baseline value (e.g., baseline $R$),
- $N$ is the total number of data points.

## Project Structure
- **`Impedance_deb.ipynb`**: The main Jupyter Notebook where the impedance and admittance calculations are implemented.
- **Data Files**: Data used for impedance analysis (if any) should be placed in the appropriate directory.

## How to Use
1. Clone this repository:
   ```bash
   git clone https://github.com/hguangshuai/Imped_spec.git
pip install -r requirements.txt
jupyter notebook Impedance_deb.ipynb
