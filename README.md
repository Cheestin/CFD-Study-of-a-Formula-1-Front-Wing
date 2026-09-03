# CFD Study of an F1 Front Wing, Investigating the Relationship Between Flap Angle & Aerodynamic Forces

A CFD study of a 1:1 scale F1 front wing, inspired by the 2025 Mercedes W16 car, varying the flap angle from 0° to 25° at 5° increments to find when the angle increase stops paying off. The lift coefficient nearly doubled across the experiment but there was a slight drop off in aerodynamic performance beyond 15° indicating a possibility of aerodynamic stall and flow separation on the wing elements. The project was built in Fusion 360, simulated in ANSYS Fluent, including a mesh independence study to ensure the results were reliable. 

<table>
  <tr>
    <td align="center">
      <img src="CAD/Final CAD W16 Front Wing Base Model.PNG" alt="Pressure Contours" width="500">
    </td>
    <td align="center">
      <img src="Results/Cl_Cd_polar.png" alt="CL-CD Polar" width="500">  
    </td>
  </tr>
</table>

## Key Finding
The lift coefficient increased from 0.551 at 0° to 1.197 at 25°, more than doubling across the experiment. However, the increase was not linear, as beyond 15°, there was a noticeable drop off of about 50% in the lift-curve slope. This was a clear indication of progressive flow separation on the wing elements, rather than a hard stall break. The L/D fell from 3.31 to 2.59 over the same range as well, further confirming that beyond 15°, any addition to the flap angle would bring diminishing returns. 

## Project Overview
- Modeled: 1:1 scale multi-element F1 front wing with inspiration from the 2025 W16 Mercedes car in Fusion 360
- Method: ANSYS Fluent CFD Workflow, utilised the k-ω SST model, ran simulations for a 0-25° flap angle sweep in 5° steps
- Tools: Fusion 360, ANSYS SpaceClaim, ANSYS Meshing, ANSYS Fluent (Student license)

## Results Summary

| Flap Angle | Lift | Drag | CL | CD |
|:------------|----:|----:|-----:|-----:|
| 0°         | 1538.71 |	464.23 |	0.55 |	0.166 |
| 5°         | 1936.37	| 602.28 |	0.69 |	0.216 |
| 10°         | 2354.06 |	825.94 |	0.84 |	0.296 |
| 15°         | 2845.84 |	1009.92 |	1.02 |	0.362 |
| 20°         | 3097.13 |	1165.16 |	1.11 |	0.417 |
| 25°         | 3341.50 |	1288.50 |	1.20 |	0.462 |

## Full Report
📄 [Read the full report here](Report/CFD_Analysis_of_F1_Front_Wing.pdf)

## Repository Structure
- `CAD/` — Fusion 360 file and per-angle STEP exports
- `Meshing/` — Mesh settings, Body Of Influence orientations, Mesh cross sections
- `Results/` — Raw data, mesh-independence analysis data, lift-drag plots, flow visualizations
- `Notes/` — Troubleshooting and debugging log

## Notes on Method & Limitations
- Mesh resolution was limited by ANSYS Fluent Student License's 1,000,000-cell limit, which resulted in a coarsening of initial refinement targets in the element sizes throughout the mesh, and relying on capture proximity/curvature adaptive sizing rather than manual refinement everywhere.
- The mesh independence study on the 0° baseline showed downforce converging well, with a 1% change between the two finest meshes, but the drag still showed greater sensitivity at about a 4% change, which meant that the absolute drag/CD values may be a bit more uncertain than the lift values throughout the study.
- The ride height of 75mm was fixed across the entire experiment. This would have been different from the actual car, as it did not account for factors like fuel burn, aerodynamic load and how the track surface may vary. 
 
## What I'd Do Next
- Transient Simulation - to capture vortex shedding and oscillation beyond stall onset, something steady-state RANS cannot resolve.
- Ride Height Sensitivity Study - vary the clearance between 50-100mm to find the downforce/ground clearance relationship, understanding the real-world setup conditions and requirements.
- Full Car Integration - add a simplified car body or open wheels to be able to capture tire wake interaction and how the front wing can influence underbody flow of the car.
