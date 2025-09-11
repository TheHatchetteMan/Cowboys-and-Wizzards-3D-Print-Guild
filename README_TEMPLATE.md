# <PROJECT NAME>
<One-sentence purpose/summary of the model.>

![Hero Image or Render](./images/hero.jpg)
> Optional: Replace with a photo/render, or remove this line.

---

## Table of Contents
- [Overview](#overview)
- [Files](#files)
- [Print Settings](#print-settings)
- [Assembly](#assembly)
- [Hardware & Materials](#hardware--materials)
- [Sizing & Scaling](#sizing--scaling)
- [Fit & Tolerances](#fit--tolerances)
- [Post-Processing](#post-processing)
- [Safety & Use Notes](#safety--use-notes)
- [Troubleshooting](#troubleshooting)
- [Changelog](#changelog)
- [License](#license)
- [Attribution](#attribution)

---

## Overview
**What it is:**  
<Brief description of what the part does, where it goes, and why it exists.>

**Designed for:**  
- Printer(s): <e.g., Bambu P1S / Generic FFF>
- Material(s): <e.g., PLA, PETG, ASA>  
- Environment: <e.g., indoor, outdoor/UV, high-temp, food-safe (if applicable)>

**Recommended use:**  
<Bulleted list of intended use cases.>

**Not for:**  
- <e.g., load-bearing > X kg, medical, food contact, high-heat > 60 °C, etc.>

---

## Files
| Path | Type | Notes |
|------|------|-------|
| `./stl/<part-name>.stl` | STL | Ready to slice |
| `./3mf/<project.3mf>` | 3MF | Pre-sliced plate/profiles (Orca/Bambu Studio) |
| `./step/<part-name>.step` | STEP | Editable CAD |
| `./scad/<project.scad>` | SCAD | Parametric source (if applicable) |
| `./images/` | JPG/PNG | Renders, assembly photos |

> Delete rows that don’t apply.

---

## Print Settings
> Base settings for most printers; adjust for your machine/filament.

**General**
- Nozzle: `0.4 mm`  (✅ change if different)
- Layer height: `0.20 mm` (draft `0.28`, quality `0.16`)
- Walls/Perimeters: `3` (≈1.2 mm)
- Top/Bottom: `4 / 4`
- Infill: `15–25%` <pattern> (e.g., Gyroid, Grid)
- Supports: `None` / `Touching buildplate` / `Everywhere` (specify)
- Build Plate Adhesion: `None` / `Brim` (size)
- Orientation: <Describe face-down/up; include small thumbnail if helpful>

**Material-specific**
- PLA: Nozzle `200–215 °C`, Bed `55–65 °C`
- PETG: Nozzle `235–250 °C`, Bed `70–85 °C`
- ASA/ABS: Nozzle `240–260 °C`, Bed `90–110 °C`, Enclosure recommended

**Printer-specific (Optional)**
- Bambu Studio/Orca profile: `<Profile Name>`  
- Flow calibration required: `Yes/No`  
- Max speed / vibration: <notes if ringing or elephant’s foot prone>

<details>
<summary>Advanced slicer notes (optional)</summary>

- Ironing: `On` top surfaces for <part>
- Supports: custom blockers/painted supports at <areas>
- Per-object modifiers: thicker walls at <zones>
- Tree supports (if needed): <settings>
</details>

---

## Assembly
> Skip if single-part print.

### Exploded View / Diagram
![Exploded View](./images/exploded.jpg)

### Steps
1. Dry-fit parts **A** + **B**; sand mating faces if tight.
2. Apply adhesive (see [Hardware & Materials](#hardware--materials)) and clamp for `30 min`.
3. Insert magnets with correct polarity (see [Fit & Tolerances](#fit--tolerances)).
4. Install fasteners; do not exceed `X N·m` torque.

### Time & Difficulty
- Assembly time: `~15–30 min`
- Difficulty: `Easy / Moderate / Advanced`

---

## Hardware & Materials
> Include everything beyond printed parts.

| Item | Spec | Qty | Link/Alt |
|------|------|-----|----------|
| Machine screws | M3 x 10 mm | 4 |  |
| Heat-set inserts | M3 (OD 4.6 mm) | 4 |  |
| Magnets | 6×3 mm N52 (disc) | 2 |  |
| Adhesive | CA gel / Epoxy | — |  |
| Finish | Primer + paint / Vapor-smooth (ABS/ASA) | — |  |

**Adhesives:**  
- PLA: CA gel or epoxy  
- PETG: Epoxy preferred  
- ASA/ABS: Acetone weld (ABS) / epoxy

---

## Sizing & Scaling
- Native units: **mm**
- Designed scale: `100%`  
- To fit <device/object> with dimension `<X>`: scale to `___%` (or change parameter `<name>` to `<value>` in SCAD/CAD).
- Walls ≥ `__ mm` to preserve strength.

**Gridfinity/Modular Systems (Optional)**  
- Footprint: `<e.g., 1×3 Gridfinity>`  
- Height: `<e.g., 25 mm total>`  
- Compatible tolerances per standard: `<notes>`

---

## Fit & Tolerances
> Record real-world fits so future you remembers.

- Clearance for sliding fit: `+0.20 mm`  
- Press-fit pegs: `-0.10 mm` from hole nominal  
- Heat-set insert holes: `M3 = 4.6–4.7 mm` (test on your printer)  
- Magnet pockets: `6.1–6.2 mm` for 6.0 mm discs; **mark polarity**: ⊕/⊖

**Calibration recommendation:**  
Print the included `tolerance-test.stl` to confirm fits before full part.

---

## Post-Processing
- Deburr: light scrape/knife on overhang edges
- Sand: 220 → 400 grit (wet/dry if painted)
- Prime/Paint: plastic primer → color → clear (optional)
- Anneal (if needed): `PLA 60–70 °C` 20–30 min, support/fixture to prevent warp
- Vapor smoothing (ABS/ASA): *follow safety precautions*

---

## Safety & Use Notes
- Not food-safe unless printed with food-safe filament and process controls.
- Avoid prolonged heat above `<temp> °C` (e.g., cars/boats for PLA).
- Keep magnets away from electronics/pacemakers.
- Small parts: choking hazard.

---

## Troubleshooting
| Symptom | Likely Cause | Fix |
|--------|--------------|-----|
| Tight fit / won’t assemble | Shrinkage/flow too high | Scale `102%` holes only; reduce flow by 2–3% |
| Weak tabs / layer split | Layer orientation / low walls | Reorient; increase walls to 4; raise temp 5 °C |
| Stringing on pockets | Retraction/speed | Increase retraction; lower temp 5–10 °C |
| Supports scar surface | Interface too close | Add support interface; increase Z-distance |

---

## Changelog
- **v1.0.0 – YYYY-MM-DD:** Initial release.
- **v1.1.0 – YYYY-MM-DD:** Adjusted magnet pockets to 6.2 mm; added 3MF plates.

**Versioning scheme:** MAJOR.MINOR.PATCH  
> Increment MINOR for dimension changes; PATCH for cosmetic/g-code tweaks.

---

## License
Choose one and delete the rest:

- **CC BY 4.0** – Attribution required  
- **CC BY-NC 4.0** – Non-commercial only  
- **MIT** – Permissive (for code/SCAD)  
- **Custom** – Describe terms

---

## Attribution
- Designer: <Your name/handle, link>  
- Inspiration/Remix from: <Link(s) if applicable>  
- Tools: <CAD software, slicer, printer>

---

<!--
Author Notes (remove before publishing):
- Keep images under ./images
- Provide a ready-to-print 3MF when possible
- Include a small tolerance-test STL for recurring hardware (M3 inserts, 6x3 magnets)
- If parametric: add a short HOWTO and default params in the SCAD
- Test-print once in PLA and once in target filament (PETG/ASA) if outdoor use
-->
