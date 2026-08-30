# UDCF Instrumented Pendulum Rig v3.0

**Unified Dimensionless Cutting Framework | Digital Twin Analysis**

## Overview

This repository contains the source code for the UDCF Instrumented Pendulum Rig v3.0. This simulator serves as a Digital Twin, allowing researchers to predict severance success (\(\eta \ge 1\)) or sub-critical impact based on the kinematic energy of a swinging pendulum. Version 3.0 introduces rigorous physical calibration and enhanced data tracking capabilities.

## Key Features

*   **Dynamic Unit Conversion:** Input data in m, mm, μm, MPa, Pa, mm², or m².
*   **Real-time Physics Engine:** Calculates Impact Velocity (\(v\)) and Kinetic Energy (\(E_k\)) instantly. The v3.0 engine incorporates a precise 0.45 J calibration energy loss to account for bearing friction, ensuring exact alignment with physical rig behavior.
*   **Critical Velocity Tracking:** Dynamically computes the critical velocity (\(v_c\)) threshold required to achieve material severance.
*   **Dimensionless Analysis:** Determines the Predictive Separation Index (\(\eta\)) using the governing UDCF equation.
*   **Visual Schematic:** Interactive SVG-based rig that animates the impact, pendulum follow-through, and material failure.
*   **Data Export:** Includes an "Export Research Data" function to generate downloadable, timestamped reports detailing SI vector analysis and simulation outcomes.

## The Governing Equations

The rig operates on the principle of the Predictive Separation Index (\(\eta\)):

$$ \eta = k_Y \left( \frac{mv^2}{2 \cdot d \cdot \tau_{ult} \cdot A} \right) \ge 1 $$

The impact velocity (\(v\)), accounting for the 0.45 J calibration loss and a standard pendulum length (\(L\)) of 1.2 m, is derived as:

$$ v = \sqrt{\frac{2[mgL(1-\cos\theta) - 0.45]}{m}} $$

Where:
*   \(k_Y\) = Recovery Factor
*   \(m\) = Tool Mass (Standard: 15.4 kg)
*   \(v\) = Impact Velocity
*   \(d\) = Specimen Thickness
*   \(\tau_{ult}\) = Ultimate Shear Strength
*   \(A\) = Contact Area
*   \(g\) = Gravitational Acceleration (9.80665 m/s²)
*   \(\theta\) = Release Angle

## Installation & Usage

1. Clone the repository.
2. Install dependencies: `npm install`
3. Run the application: `npm start`
4. Adjust the "Rig Setup" and "Specimen & Recovery Properties" to observe real-time changes in \(\eta\).
5. Toggle the Safety Interlock to release the pendulum and test severance.

## Research Body

**Lead Researcher:** Clifford Yeboah  
**Institute:** The Yeboah Institute Research  

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Citation

If this Digital Twin is utilized in academic research, please cite it as:

> Yeboah, C. (2026). UDCF Instrumented Pendulum Rig v3.0 [Software]. The Yeboah Institute Research.
