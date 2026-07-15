# Multi-Class Term Project: End-to-End Build
This project tracks a complete product development cycle, from identifying initial engineering constraints to executing multi-CAD data integration, detailed 2D production documentation, and physical manufacturing optimization.

<p align="center">
  <img src="images/figure1.jpg" alt="Figure 1: Final Product Render" width="40%" />
</p>
<p align="center"><em>Figure 1: High-resolution rendering of the finalized assembly.</em></p>

---

## 1. Design Challenges & Solutions
Resolved physical interface constraints to minimize hardware and guarantee precise component fitment.

* **Compound Lid Profile:** Isolated and matched the container lid's spline curves through iterative physical clearance test prints.
* **Integrated Bearing Traps:** Boolean-subtracted a McMaster-Carr STEP model in Onshape, tuning clearance offsets to compensate for PETG thermal shrinkage.
* **Part Consolidation:** Designed interlocking dual-spindle rollers and a unibody base to eliminate additional hardware.

---

## 2. Multi-CAD Workflow & Configuration Strategy
Leveraged a hybrid modeling pipeline, transitioning from Onshape concept design to SolidWorks for assembly configuration.

<p align="center">
  <img src="images/figure2a.png" alt="Configuration A" width="48%" />
  <img src="images/figure2b.png" alt="Configuration B" width="48%" />
</p>
<p align="center"><em>Figure 2: Side-by-side assembly configuration.</em></p>

* **Cross-Platform Integration:** Modeled internal mechanism components in Onshape and container body/lid geometries in SolidWorks, executing data migration via STEP file imports.
* **Parametric Assembly:** Completed the final multi-part assembly in SolidWorks using robust feature trees to maintain critical component references.
* **Configuration Management:** Developed modular assembly configurations in SolidWorks to create an exploded view showcasing parts and assembly orientation.

---

## 3. ASME Production Documentation
Translated the 3D assembly into a professional, ASME-compliant 2D drawing package, utilizing precise dimensioning and limit tolerances to control critical component fitment.

<p align="center">
  <img src="images/figure3a.png" alt="Engineering Drawing Sheet 1" width="65%" /><br />
  <img src="images/figure3b.png" alt="Engineering Drawing Sheet 2" width="65%" /><br />
  <img src="images/figure3c.png" alt="Engineering Drawing Sheet 3" width="65%" />
</p>
<p align="center"><em>Figure 3: Multi-sheet 2D technical drawing package including full bill of materials (BOM).</em></p>

* **Master Assembly Sheet:** Features standard orthographic projections, isometric reference views, component balloon callouts, and an integrated Bill of Materials (BOM).
* **Detailed Part Sheets:** Focuses on critical internal components, utilizing detailed section breakouts, precise dimensioning schemes, and targeted fitment tolerances.

---
## 4. Design for Additive Manufacturing (DFAM)
Optimized model geometries and toolpaths for reliable physical fabrication, focusing on support reduction, bridge control, and material-specific shrinkage.

<p align="center">
  <img src="images/figure5.jpg" alt="Figure 5: OrcaSlicer Toolpath Preview" width="60%" />
</p>
<p align="center"><em>Figure 5: Slicing configuration preview in OrcaSlicer showcasing toolpath and layer strategy.</em></p>

* **Slicer & Support Optimization:** Tuned OrcaSlicer parameters—specifically wall loops, infill geometry, and snug support interfaces—to isolate sacrificial supports and minimize print time.
* **Bridge & Orientation Control:** Positioned the unibody base to leverage horizontal bridging limits, orienting toolpaths to span wide gaps cleanly without sagging.
* **Thermal Shrinkage Compensation:** Formulated precise scaling and clearance offsets in the CAD model to account for the physical thermal contraction behavior of PETG during high-speed printing on a custom Klipper-controlled Voron.
