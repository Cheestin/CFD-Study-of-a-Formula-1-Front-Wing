A short CFD study in ANSYS of the effects of front wing flap angle on aerodynamic forces, modelled with inspiration from a W16 Mercedes F1 Car.

# CFD Study of an F1 Front Wing, Investigating the Relationship Between Flap Angle & Aerodynamic Forces

[One-paragraph hook: what you did, what you found, the headline number]

<table>
  <tr>
    <td align="center">
      <img src="Results/Cl_Cd_polar.png" alt="CL-CD Polar" width="500">
    </td>
    <td align="center">
      <img src="CAD/Final CAD W16 Front Wing Base Model.PNG" alt="Pressure Contours" width="500">
    </td>
  </tr>
</table>

## Key Finding
[2-3 sentences: the slope-halving result, framed as the answer to a specific question]

## Project Overview
- Modeled: 1:1 scale multi-element F1 front wing with inspiration from the 2025 W16 Mercedes car in Fusion 360
- Method: ANSYS Fluent CFD Workflow, utilised the k-ω SST model, ran simulations for a 0-25° flap angle sweep in 5° steps
- Tools: Fusion 360, ANSYS SpaceClaim, ANSYS Meshing, ANSYS Fluent (Student license)

## Results Summary

| Flap Angle | Lift | Drag | CL | CD |
|------------:|----:|----:|-----:|
| 0°         | 1538.71 |	464.23 |	0.55 |	0.166 |
| 5°         | 1936.37	| 602.28 |	0.69 |	0.216 |
| 10°         | 2354.06 |	825.94 |	0.84 |	0.296 |
| 15°         | 2845.84 |	1009.92 |	1.02 |	0.362 |
| 20°         | 3097.13 |	1165.16 |	1.11 |	0.417 |
| 25°         | 3341.50 |	1288.50 |	1.20 |	0.462 |

## Full Report
📄 [Read the full report here](report/F1_Front_Wing_CFD_Report.pdf)

## Repository Structure
- `CAD/` — Fusion 360 file and per-angle STEP exports
- `Meshing/` — Mesh settings, Body Of Influence orientations, Mesh cross sections
- `Results/` — Raw data, mesh-independence analysis data, lift-drag plots, flow visualizations
- `Notes/` — Troubleshooting and debugging log

## Notes on Method & Limitations
[2-3 sentences: student license 1M-cell constraint, mesh independence caveat on drag, ride height fixed]

## What I'd Do Next
[3-4 bullets from our earlier "next steps" list]
