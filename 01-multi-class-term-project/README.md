# Multi-Class Term Project: End-to-End Build

This project tracks a complete product development cycle, from identifying initial engineering constraints to executing multi-CAD data integration, detailed 2D production documentation, and physical manufacturing optimization.

<p align="center">
  <img src="images/figure1.jpg" alt="Figure 1: Final Product Render" width="40%" />
</p>
<p align="center"><em>Figure 1: High-resolution rendering of the finalized assembly.</em></p>

---

## 1. Design Challenges & Solutions
Resolved physical interface constraints to minimize hardware and guarantee precise component fitment.

<div>
  <strong>Key Prototyping Achievements:</strong>
  <ul>
    <li><strong>Compound Lid Profile:</strong> Isolated and matched the container lid's spline curves through iterative physical clearance test prints.</li>
    <li><strong>Integrated Bearing Traps:</strong> Boolean-subtracted a McMaster-Carr STEP model in Onshape, tuning clearance offsets to compensate for PETG thermal shrinkage.</li>
    <li><strong>Part Consolidation:</strong> Designed interlocking dual-spindle rollers and a unibody base to eliminate additional hardware.</li>
  </ul>
</div>

<br clear="left"/>
---

## 2. Parametric Modeling & Configuration Strategy

The design began as a conceptual model in Onshape before transitioning to SolidWorks for advanced configuration management and detailing. This required clean data migration, maintaining references, and managing step-file imports without geometry degradation.

<p align="center">
  <img src="images/figure2a.png" alt="Configuration A" width="38%" />
  <img src="images/figure2b.png" alt="Configuration B" width="38%" />
</p>
<p align="center"><em>Figure 2: Side-by-side assembly configuration analysis demonstrating geometric variations.</em></p>

Using SolidWorks, the model was built using robust parametric feature trees to allow rapid design changes. Multiple assembly configurations were developed to account for different operating conditions and material variations, ensuring the design remained modular and scalable.

---

## 3. Production Documentation (2D Drafting)

A design is only as good as its documentation. A complete, production-ready drawing package was generated adhering to ASME standards to ensure seamless fabrication or machine-shop handoff.

<p align="center">
  <img src="images/figure3a.png" alt="Engineering Drawing Sheet 1" width="65%" /><br />
  <img src="images/figure3b.png" alt="Engineering Drawing Sheet 2" width="65%" /><br />
  <img src="images/figure3c.png" alt="Engineering Drawing Sheet 3" width="65%" />
</p>
<p align="center"><em>Figure 3: Multi-sheet 2D technical drawing package including full bill of materials (BOM).</em></p>

The drawing package includes:
* **Main Assembly Layout:** Complete with balloon callouts, standard orthographic projections, and an itemized Bill of Materials (BOM).
* **Detailed Part Sheets:** Two representative component drawings featuring section views, isometric details, precise dimensioning, and fitment tolerances.

---

## 4. Design for Manufacturing (DFM) & 3D Printing

To bridge the gap between digital modeling and physical production, the components were optimized for print-bed orientation, strength distribution, and rapid deployment.

![Figure 5: OrcaSlicer Preview](images/figure4.png)
*Figure 5: Slicing configuration preview in OrcaSlicer showcasing toolpath and layer strategy.*

### Slicing & Hardware Optimization
* **Slicer Tuning (OrcaSlicer):** Configured with optimized wall counts, specific infill geometry to maximize directional rigidity, and targeted layer heights to ensure structural integrity.
* **Hardware Execution:** Tailored specifically for a high-speed custom Voron machine running Klipper firmware. Tolerances were tuned to account for plastic shrinkage and thermal expansion, ensuring that parts fit perfectly right off the build plate.
