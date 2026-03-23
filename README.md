# Reliability-Driven Optimization of Redundant Through-Glass Via (TGV)

This research was conducted in the **Thermal Engineering and Laser Applications (TELA) Lab** at Chung-Ang University under the supervision of **Prof. Jung Bin In**.  
The project was independently designed and executed during a 10-week intensive research program (2025 Winter MeSTeR).

---

## Research Significance

High-frequency RF and AI-driven semiconductor systems require reliable glass interposer technologies.  
Through-Glass Via (TGV) structures offer low dielectric loss and high-frequency compatibility, but their practical scalability is limited by:

- Low thermal conductivity of glass  
- Brittle fracture behavior  
- Severe thermo-mechanical stress concentration at the Cu–glass interface  

Under RF-induced volumetric heat generation, these limitations significantly increase crack initiation risk.

This project establishes a **fracture-informed, reliability-driven design framework** for redundant TGV structures by integrating:

- Thermal analysis  
- Structural mechanics  
- Fracture mechanics  
- Manufacturing constraints  

The study moves beyond simple configuration comparison and derives physically grounded design limits.

---

## Core Research Question

> What redundant TGV configuration and taper geometry maximize thermo-mechanical reliability under RF-induced heating while satisfying fracture constraints?

---

## Research Methodology

The investigation was structured as a staged engineering framework:

---

### 1️⃣ Mesh Convergence Validation

- Element size variation study  
- Nonlinear regression using the Levenberg–Marquardt algorithm  
- Converged temperature: **T∞ = 29.763 °C**  
- Optimal setting: Refinement level 2, Transition slow  

**Purpose:**  
Ensure mesh-independent simulation credibility before structural comparison.

---

### 2️⃣ Redundant Configuration Study (Single–Penta)

Boundary conditions:

- Fixed pad width: 80 μm  
- RF-induced volumetric heat generation (25 ms transient)  
- Convection coefficient: h = 10 W/m²K  
- Bottom surface fixed support  
- Thermo-mechanical coupling  

**Result:**

- Dual redundant TGV achieved the lowest maximum principal stress (**16.4 MPa**)  
- Increasing via count reduces current per via but increases interfacial interaction  

**Engineering Insight:**  
Stress reduction is not monotonic with via count — geometric interaction dominates beyond the dual configuration.

---

### 3️⃣ Scale-Up Packaging Model

To approach realistic packaging conditions:

- Added Cu pad  
- Added upper and lower Si blocks  
- 42 dual redundant TGVs  
- Full thermo-mechanical coupling  

Fracture mechanics criterion applied:

\[
K_I = Y \sigma \sqrt{\pi a}
\]

Assumptions:

- Borosilicate glass  
- \( K_{IC} = 0.75–0.90 \, MPa \cdot m^{0.5} \)  
- Crack size \( a = 10 \, μm \)  
- Geometry factor \( Y = 1.12 \) (surface crack assumption)

Derived critical stress:

\[
\sigma_{critical} = 119.5 \, MPa
\]

Using linear regression, allowable volumetric heat generation:

\[
q'''_{max} = 0.4594 \, GW/m^3
\]

Equivalent allowable RF power:

\[
\approx 12 \, mW
\]

**Key Contribution:**  
Unlike configuration-only studies, this work derives an allowable RF power limit based on fracture mechanics applied to a realistic packaging-scale model.

---

### 4️⃣ Taper Angle Optimization (Process-Aware Design)

Manufacturing reality:

Laser-induced wet etching produces naturally tapered via geometries.

Geometric constraints:

- Opening diameter: 20 μm  
- Pad width: 80 μm  
- Aspect ratio: 10:1  

Feasible taper range:

\[
85° \leq \theta \leq 90°
\]

Process capability limit:

\[
\theta_{max} \approx 88.854°
\]

**Result:**

Optimal reliability range:

\[
87° – 88°
\]

**Insight:**  
Taper geometry affects axial stress redistribution and interfacial stress concentration, directly influencing thermo-mechanical reliability.

---

## Boundary Conditions Summary

### Thermal

- Uniform volumetric heat generation in Cu via  
- Convection: h = 10 W/m²K on external surfaces  
- Insulated lateral surfaces  

### Structural

- Fixed support at glass bottom surface  
- Linear elastic material model  
- Thermal expansion included  

---

## Engineering Contributions

- Reliability-based redundant TGV selection framework  
- Fracture-informed allowable RF power derivation  
- Process-constrained taper optimization  
- Multi-stage validation: mesh → configuration → scale-up → manufacturing  

This work provides a design guideline for next-generation high-frequency and AI semiconductor packaging systems.

---

## Limitations

- Linear elastic material assumption  
- No electro-thermal coupling  
- Constant convection coefficient assumption  
- No experimental validation  

Future work includes electro-thermal co-simulation and nonlinear fracture modeling.

---

## Repository Structure

'''bash
Reliability-Driven-TGV-Design
│
├── 01_mesh_validation/
│   ├── ANSYS setup files
│   ├── Mesh convergence data
│   └── Nonlinear regression scripts
│
├── 02_redundant_configuration_study/
│   ├── Single–Penta configuration models
│   ├── Stress comparison data
│   └── Result figures
│
├── 03_scale_up_model/
│   ├── Packaging-scale FEM model
│   ├── Fracture-based allowable power derivation
│   └── Regression analysis
│
├── 04_taper_angle_optimization/
│   ├── Process-aware geometry models
│   ├── Taper angle sensitivity analysis
│   └── Reliability comparison
│
├── docs/
│   ├── boundary_conditions.md
│   ├── methodology.md
│   ├── material_properties.md
│   └── assumptions_and_limitations.md
│
├── figures/
│   └── Key result visualizations
│
└── poster/
    └── Winter_MeSTeR_Poster.pdf
'''

---

## Research Environment

Thermal Engineering and Laser Applications (TELA) Lab  
Chung-Ang University  

Advisor: Prof. Jung Bin In  
Mentor: Ph.D. Candidate Changyoung Ryu  
Program: 2025 Winter MeSTeR (Mechanical Engineering Short-Term Research Program)

---

## Author

Kyungwoo Lee  
Undergraduate Researcher, Mechanical Engineering  
Chung-Ang University
