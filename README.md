# SLA Hydrogel Printing for Quantitative MRI Phantoms

This repository documents the workflow and material formulations used to fabricate quantitative MRI phantoms using **stereolithography (SLA)** printing. The approach enables automated production of anatomically inspired hydrogel models with realistic T₁ and T₂ contrast using affordable, desktop-scale resin printers.

---

## 📘 Overview

MRI phantoms are essential tools for validating pulse sequences, testing reconstruction methods, and calibrating scanner hardware.  
While commercial phantoms such as those from **NIST** and **ACR** offer reliable calibration standards, they are typically limited to simple geometries (e.g., spheres or cylinders). These do not reproduce the complex biophysical structure or relaxation behavior of biological tissue.

This project demonstrates a **hydrogel-based SLA printing method** for constructing anatomically inspired, quantitative phantoms with tunable T₁/T₂ values. The workflow provides an **accessible**, **reproducible**, and **low-cost** route for any MRI laboratory to design and produce realistic tissue-mimicking models.

---

## 🧪 Materials

All reagents are water-soluble and commonly available through major suppliers.

| Component | Role | Example Material / Source |
|------------|------|----------------------------|
| **Monomers** | Form polymer network | Acrylamide (AM), Acrylic acid (AA) — Sigma Aldrich |
| **Crosslinker** | Connect polymer chains, controls stiffness | Poly(ethylene glycol) diacrylate (PEGDA 700) — Sigma Aldrich |
| **Photoinitiator** | UV-activated radical initiator | Lithium phenyl-2,4,6-trimethylbenzoylphosphinate (LAP) — Arctom Scientific |
| **Additives** | Modify viscosity and elasticity | Poly(vinyl alcohol) (PVA), Poly(acrylic acid) (PAA) — Sigma Aldrich |
| **Photoinhibitor dyes** | Prevent overcuring and improve layer resolution | Brilliant Green, Methyl Red, Quinoline Yellow |
| **T₁/T₂ dopants** | Tune relaxation properties | PEGDA (affects T₁), MICR Ink (Versaink; contains iron-oxide nanoparticles, affects T₂) |
| **Solvent** | Base medium | Deionized water (DIW) |

All solutions are mixed under gentle stirring at room temperature and stored in **amber bottles** to prevent premature polymerization.

---

## ⚙️ Equipment

- **Printer:** Elegoo **Saturn 4 Ultra** MSLA printer (used without modification)  
- **UV source:** Integrated 405 nm light engine  
- **MRI Scanner:** GE MR750W 3 T system with 8-channel flexible knee coil  
- **Mixing tools:** Magnetic stirrer, pipettes, beakers  
- **Containers:** Amber vials or bottles (light-protected)

---

## 🧫 Hydrogel Preparation

1. Dissolve monomers, crosslinker, photoinitiator, dyes, and additives in deionized water.  
2. Mix thoroughly until fully dissolved.  
3. Store stock solutions in light-protected amber bottles until printing.

During UV exposure (405 nm), the photoinitiator **LAP** produces radicals that polymerize AM and AA into a crosslinked hydrogel matrix via PEGDA.  
Additives (PVA, PAA) adjust print viscosity and flexibility, while dyes limit excess curing to preserve layer resolution.

---

## 🖨️ Printing Parameters

**Typical Settings**
- **Layer height:** 0.25 mm  
- **Exposure time:** 10–20 s/layer (depends on monomer & crosslinker concentration)  
- **Build plate adhesion:** Improved with 0.2 % PAA additive  
- **Supports:** Optional; overhangs ≤ 30° may droop in low-PEGDA gels  

**Performance observations**
- High-PEGDA (≥ 20 %) gels print stiff structures with stable overhangs but may become brittle.  
- Low-PEGDA (≤ 1 %) formulations remain flexible but prone to deformation.  
- Dimensional accuracy typically within **1–2 % (XY)** and **1–3 % (Z)**.

---

## 🧬 T₁/T₂ Parameter Targeting

Relaxation times are tuned by adjusting key chemical ratios:

| Property | Controlled by | Example Range |
|-----------|----------------|---------------|
| **T₁** | Monomer & crosslinker (AM, PEGDA) | 10–30 % AM, 0.2–20 % PEGDA |
| **T₂** | MICR ink concentration | 0–1 % (v/v) depending on desired contrast |

Calibration involves curing test vials for 1 min under UV and scanning them with:
- **Inversion Recovery Spin-Echo (IRSE):** TI = 100–2000 ms, TR = 5000 ms  
- **Spin-Echo (SE):** TE = 25–800 ms, TR = 5000 ms  

**Target relaxation values** (based on *Stanisz et al.*):  
- White Matter: **T₁ ≈ 1080 ms, T₂ ≈ 70 ms**  
- Gray Matter: **T₁ ≈ 1820 ms, T₂ ≈ 100 ms**  

Example formulations:
- **Gray Matter:** 20 % AM + 1 % PEGDA + 0.15 % LAP  
- **White Matter:** 20 % PEGDA + 0.15 % LAP  

---

## 💰 Cost and Accessibility

- **Printer cost:** ≈ $500  
- **Hydrogel batch (500 mL):** ≈ $21  
- All reagents and tools are accessible to standard university or research laboratories.

---

## 🧭 Summary

This workflow provides a **practical, cost-effective**, and **open** framework for producing SLA-printed MRI phantoms with tunable relaxation properties and anatomical realism.  
The method combines reproducible chemistry, automated manufacturing, and quantitative MRI validation, **laying the groundwork for reproducible, anatomically accurate MRI calibration and validation tools**—and future extensions to anisotropic microstructures or biochemical contrast systems.

---

### 📄 Citation

If you use or adapt this workflow, please cite the corresponding abstract:

> Gopalan, K., *et al.* “Automated fabrication of quantitative hydrogel MRI phantoms using stereolithography.” ISMRM 2025.

---

### 📷 Figures (optional)
Add figures or reference images (e.g., print test geometries, T₁/T₂ calibration curves) in a `/figures` directory and link them below:

```markdown
![Printability Tests](figures/printability.png)
![Relaxation Calibration](figures/relaxivity_curve.png)

