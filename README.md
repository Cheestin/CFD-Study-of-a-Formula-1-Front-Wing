# CFD-Study-of-a-Formula-1-Front-Wing
A short CFD study in ANSYS of the effects of front wing flap angle on aerodynamic forces, modelled with inspiration from a W16 Mercedes F1 Car.

# CFD Study of an F1 Front Wing — Flap Angle Sweep & Stall Onset

[One-paragraph hook: what you did, what you found, the headline number]

<table>
  <tr>
    <td align="center">
      <img src="Results/Cl_Cd_polar.png" alt="CL-CD Polar" width="500">
    </td>
    <td align="center">
      <img src="CAD/Final CAD W16 Front Wing Base Model.png" alt="Pressure Contours" width="500">
    </td>
  </tr>
</table>

## Key Finding
[2-3 sentences: the slope-halving result, framed as the answer to a specific question]

## Project Overview
- Modeled: 1:1 scale multi-element F1 front wing (Mercedes W16-style), Fusion 360
- Method: ANSYS Fluent CFD, k-ω SST, 0-25° flap angle sweep in 5° steps
- Tools: Fusion 360, ANSYS SpaceClaim, ANSYS Meshing, ANSYS Fluent (Student license)

## Results Summary
[Table: angle, CL, CD, L/D — the same 6-row table from your report]

## Full Report
📄 [Read the full report](report/F1_Front_Wing_CFD_Report.pdf)

## Repository Structure
- `cad/` — Fusion 360 source and per-angle STEP exports
- `mesh-setup/` — meshing settings summary
- `mesh-independence/` — mesh convergence study data
- `results/` — raw data, charts, flow visualizations
- `notes/troubleshooting-log.md` — meshing/setup debugging log

## Notes on Method & Limitations
[2-3 sentences: student license 1M-cell constraint, mesh independence caveat on drag, ride height fixed]

## What I'd Do Next
[3-4 bullets from our earlier "next steps" list]
