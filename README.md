# Reliability-Driven-TGV-Design
Reliability-driven thermo-mechanical optimization of redundant Through-Glass Via (TGV) structures under RF-induced volumetric heat generation using FEM simulation.

# Reliability-Driven Optimization of Redundant Through-Glass Via (TGV)

This research was conducted during a 10-week intensive research program in the lab of **Prof. Jung Bin In, Chung-Ang University**.

Supervised by Ph.D. candidate Changyoung Ryu.

---

## Research Context

With the rapid growth of AI and high-frequency RF systems, glass interposers with Through-Glass Vias (TGVs) are emerging as a next-generation packaging technology due to:

- Low dielectric constant (reduced signal loss)
- High-frequency compatibility
- Laser-based microfabrication capability

However, glass substrates exhibit:

- Low thermal conductivity
- Brittle fracture behavior
- Severe thermo-mechanical stress concentration at the Cu–glass interface

Under RF-induced volumetric heat generation, these characteristics significantly increase crack initiation risk.

This project aims to establish a **reliability-driven geometric design framework** for redundant TGV structures.

---

## Core Research Question

> What redundant TGV configuration and taper geometry maximize thermo-mechanical reliability under RF-induced volumetric heat generation while satisfying fracture constraints?

---

## Research Strategy

The project was structured as a staged engineering investigation:

### 1. Mesh Convergence Validation
- Element size variation study
- Nonlinear regression using Levenberg–Marquardt algorithm
- Converged temperature: T∞ = 29.763 °C
- Optimal setting: Refinement level 2, Transition slow

Purpose:
Ensure simulation credibility before structural comparison.

---

### 2. Redundant Configuration Study (Single–Penta)

- 80 μm fixed pad width
- 25 ms RF-induced volumetric heat generation
- Convection coefficient h = 10 W/m²K
- Bottom surface fixed support
- Thermo-mechanical coupling

Result:
- Dual redundant TGV showed the lowest maximum principal stress (16.4 MPa)
- Increasing via count reduces current per via but increases interfacial interaction

Engineering Insight:
Stress reduction is not monotonic with via count — geometric interaction dominates beyond dual configuration.

---

### 3. Scale-Up Packaging Model

To approach realistic packaging conditions:

- Added Cu pad
- Added upper/lower Si blocks
- 42 dual redundant TGVs
- Full thermo-mechanical coupling

Fracture criterion applied:

K_I = Y σ √(πa)

Assumptions:
- Borosilicate glass
- K_IC = 0.75–0.90 MPa·m^0.5
- Crack size a = 10 μm
- Y = 1.12 (surface crack)

Derived critical stress:
σ_critical = 119.5 MPa

Using linear regression:
Allowable volumetric heat generation:

q'''_max = 0.4594 GW/m³

Equivalent allowable RF power:
≈ 12 mW

---

### 4. Taper Angle Optimization (Process-Aware Design)

Manufacturing constraint:
Laser-induced wet etching produces tapered via geometry.

Geometric constraints:
- Opening diameter = 20 μm
- Pad width = 80 μm
- Aspect ratio = 10:1

Feasible range:
85° ≤ taper ≤ 90°

Process capability:
Max achievable ≈ 88.854°

Result:
Optimal reliability range:
87°–88°

Insight:
Taper geometry affects axial stress redistribution and interfacial stress concentration.

---

## Boundary Conditions Summary

Thermal:
- Uniform volumetric heat generation in Cu via
- Convection h = 10 W/m²K on external surfaces
- Insulated lateral surfaces

Structural:
- Fixed support on glass bottom
- Linear elastic materials
- Thermal expansion included

---

## Engineering Contributions

- Reliability-based redundant TGV selection framework
- Fracture-informed allowable RF power derivation
- Process-constrained taper optimization
- Multi-stage validation (mesh → configuration → scale-up → manufacturing)

This work provides a design guideline for next-generation high-frequency and AI packaging systems.

---

## My Role

- Designed and built all ANSYS FEM models
- Performed mesh convergence validation
- Implemented nonlinear regression scripts in Python
- Derived fracture-based allowable power limits
- Conducted taper geometry optimization study
- Structured the staged engineering investigation

---

## Limitations

- Linear elastic material assumption
- No electro-thermal coupling
- No experimental validation
- Constant convection coefficient assumption

Future work includes electro-thermal co-simulation and nonlinear fracture modeling.

---

## Repository Structure

01_mesh_validation/  
02_redundant_configuration_study/  
03_scale_up_model/  
04_taper_angle_optimization/  
docs/  
poster/

---

## Program Information

2025 Winter MeSTeR (Mechanical Engineering Short-Term Research Program)  
Chung-Ang University

---

## Author

**Kyungwoo Lee**  
Undergraduate Student, Mechanical Engineering
