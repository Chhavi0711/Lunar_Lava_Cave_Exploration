# Lunar Lava Cave Exploration System - Airbag-Based Lander

**Author:** Chhavi Tanwar
**Faculty Advisor:** Rachana Agrawal
**Timeline:** Jan '26 - Apr '26 (UGP-I)

## Objective

To design a lightweight, robust airbag-based landing system for an 8U CubeSat rover for lunar surface deployment.

## Motivation

Lunar lava caves are promising sites for future habitation and exploration, offering shelter from solar radiation, micrometeorites, and extreme temperature swings. Exploring them requires landers that can touch down safely without the mass and complexity of traditional soft-landing mechanisms. Airbag-based landing systems, proven on missions like Mars Pathfinder and the Mars Exploration Rover, offer a lightweight alternative for small-scale lunar missions.

## Approach

- Built physics-based analytical models using energy balance to estimate landing impact forces and airbag pressure, evaluated at an impact velocity of 7.2 m/s under a 40g design impact.
- Compared structural configurations (tetrahedral vs. cubic) to analyze load transfer (axial vs. bending behavior).
- Derived sizing relations incorporating material properties (σy ≈ 270 MPa), a factor of safety of 1.5, and geometry (compression stroke Δx = 40 cm, panel length L = 85 cm) to estimate thickness, for a system mass of 26 kg (16 kg lander + 10 kg rover and subsystems).
- Designed integrated CAD models (stowed and deployed, 4-petal tetrahedral structure) and performed material trade-offs across three candidate materials (aluminum 6061-T6, aluminum honeycomb, mild steel) for mass optimization.

## Result

- Conducted a detailed literature survey of airbag-based landing systems (Luna 9, Mars Pathfinder, MER) to inform structural configuration and design parameter choices.
- Formulated preliminary analytical relations for impact force and structural thickness, indicating tetrahedral geometry as directionally more mass-efficient than cubic.
- Produced a preliminary lander concept (stowed and deployed CAD) integrating rover, airbag, and structural subsystem components.

## Methodology Summary

1. **Energy balance:** (1/2)MV² = F·Δx → F = MV²/(2Δx); converted to pressure via P = F/A.
2. **Structural analysis:**
   - Tetrahedral structure modeled as an axial-loading (membrane stress) problem.
   - Cubic structure modeled as plate sections under bending.
3. **Material sizing:** allowable stress σ_allow = FOS · σy, used to derive thickness as a function of load, geometry, and material.
4. **Key finding:** buckling - not yield stress alone - governs the required thickness in both geometries; the tetrahedral configuration consistently requires less thickness (and material) than the cubic configuration for the same design load.

## Design Comparison Tables

### Material Comparison

| Material | Density (kg/m³) | Young's Modulus (GPa) | Yield Strength (MPa) | Allowable Stress (MPa, FOS=2) |
|---|---|---|---|---|
| Aluminum 6061-T6 | 2700 | 69 | 270 | 135 |
| Aluminum Honeycomb (1–5 mm) | 80 | 0.95 | 2.1 | 1.05 |
| Steel (mild) | 7850 | 200 | 250 | 125 |

### Structural Frame Geometry Comparison

| Parameter | Tetrahedral Frame | Cubic Frame |
|---|---|---|
| Basic Geometry | 4 triangular faces | 6 square faces |
| Primary Load Type | Axial (truss-like) | Bending (plate) |
| Structural Efficiency | Very High | Moderate |
| Thickness Requirement | Lowest | Highest |
| Buckling Susceptibility | Very Low | High |
| Mass Efficiency | Best (least material needed) | Worst |
| Integration with Airbags | Proven (used in Mars Pathfinder) | Less common |
| Failure Mode | Member failure (rare) | Panel bending + buckling |

## Repository Status

This repository reflects a UGP-I (undergraduate project, first phase) milestone: a literature-grounded problem formulation, preliminary analytical sizing relations, and an initial CAD concept. Simulation-based optimization and extension to more complex structures are identified as next steps.

## References

See [`references.md`](./references.md) for the full literature list underlying this work.
