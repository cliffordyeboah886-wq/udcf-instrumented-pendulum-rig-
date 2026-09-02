# UDCF Instrumented Pendulum Cutting Rig v3.1

**Unified Dimensionless Cutting Framework | Digital Twin Analysis**

## Overview

This repository contains the source code for the UDCF Instrumented Pendulum Cutting Rig v3.1. This simulator serves as a Digital Twin, allowing researchers to predict severance success (&eta; &ge; 1) or sub-critical impact based on the kinematic energy of a swinging pendulum. Version 3.1 introduces rigorous physical calibration, enhanced data tracking capabilities, and precise critical velocity tracking that fully incorporates the material recovery factor (k<sub>Y</sub>).

## Key Features

*   **Dynamic Unit Conversion:** Input data in m, mm, μm, MPa, Pa, mm², or m².
*   **Real-time Physics Engine:** Calculates Impact Velocity (v) and Kinetic Energy (E<sub>k</sub>) instantly. The v3.1 engine incorporates a precise 0.45 J calibration energy loss to account for bearing friction, ensuring exact alignment with physical rig behaviour.
*   **Critical Velocity Tracking:** Dynamically computes the critical velocity (v<sub>c</sub>) threshold required to achieve material severance.
*   **Dimensionless Analysis:** Determines the Predictive Separation Index (&eta;) using the governing UDCF equation.
*   **Visual Schematic:** Interactive SVG-based rig that animates the impact, pendulum follow-through, and material failure.
*   **Data Export:** Includes an "Export Research Data" function to generate downloadable, timestamped reports detailing SI vector analysis and simulation outcomes.

## The Governing Equations

The rig operates on the principle of the Predictive Separation Index (&eta;):

$$
\eta = k_Y \left( \frac{mv^2}{2 \cdot d \cdot \tau_{ult} \cdot A} \right) \ge 1
$$

The impact velocity (v), accounting for the 0.45 J calibration loss and a standard pendulum length (L) of 1.2 m, is derived as:

$$
v = \sqrt{\frac{2[mgL(1-\cos\theta) - 0.45]}{m}}
$$

The critical velocity (v<sub>c</sub>), which represents the minimum velocity required to achieve material severance (where &eta; = 1), incorporates the recovery factor (k<sub>Y</sub>) and is calculated as:

$$
v_c = \sqrt{\frac{2 \cdot d \cdot \tau_{ult} \cdot A}{m \cdot k_Y}}
$$

Where:
*   k<sub>Y</sub> = Recovery Factor
*   m = Tool Mass (Standard: 15.4 kg)
*   v = Impact Velocity
*   v<sub>c</sub> = Critical Velocity
*   d = Specimen Thickness
*   &tau;<sub>ult</sub> = Ultimate Shear Strength
*   A = Contact Area
*   g = Gravitational Acceleration (9.80665 m/s²)
*   &theta; = Release Angle

## Installation & Usage

1. Clone the repository.
2. Install dependencies: `npm install`
3. Run the application: `npm start`
4. Adjust the "Rig Setup" and "Specimen & Recovery Properties" to observe real-time changes in (&eta;).
5. Toggle the Safety Interlock to release the pendulum and test severance.

## Research Body

**Lead Researcher:** Clifford Yeboah  
**Institute:** The Yeboah Institute Research  

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Citation

If this Digital Twin is utilised in academic research, please cite it as:

> Yeboah, C. (2026). UDCF Instrumented Pendulum Cutting Rig v3.1 [Software]. The Yeboah Institute Research.
