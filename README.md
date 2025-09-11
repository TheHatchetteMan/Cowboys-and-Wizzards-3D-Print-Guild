# Cowboys-and-Wizzards-3D-Print-Guild
<img width="960" height="960" alt="image" src="https://github.com/user-attachments/assets/1cb55423-05b0-4d49-ba4e-be40180a7b00" />

A shared workshop for cowboys 🐎 and wizards 🪄 who design, remix, and 3D print useful things—then share them with the world.
## Goals
- Keep models organized, reproducible, and easy to print.
- Encourage collaboration, remixing (when allowed), and learning.
- Respect creators’ rights and safety guidelines.

## Model folder naming
- Use snake_case: models/Gridfinity/usb_holder_v2/
- Include a simple version if you expect iterations: -v2, -v3
- Avoid spaces and special characters.

## How to add a new model
### 1. Pick a category
- Place the model under models/<Category>/<model_name>/. Create the category only if it doesn’t exist and is broadly useful.

### 2. Include these files
- README.md using the README_TEMPLATE.md (copy, fill, and delete unused sections).
- images/ with clear photos/renders of the final print and any assembly steps.
- Model files:
     - Printable: stl/ (or .stl in root if simple)
     - Slicer projects: 3mf/ (Bambu, Prusa, etc.)
     - Source CAD: step/ (preferred), plus source/ (SCAD/F3D/etc.)
     - Any scripts or generator files.
### 3. Document clearly (in your model README.md)
- Printer/material used, nozzle size, layer height, infill, walls, supports.
- Orientation and any part-specific settings.
- Assembly instructions, hardware (e.g., magnets/screws), and tolerances.
- License and attribution (if remixing), including links.
### 4. Quality checklist (before you commit)
- [ ] Manifold/watertight STL (no non-manifold edges).
- [ ] Units in millimeters and 1:1 scale.
- [ ] Oriented for sane supports; mark “support-free” if true.
- [ ] Tolerances noted (e.g., +0.2 mm for press-fit).
- [ ] Printed and test-fit (if feasible).
- [ ] README.md filled and images added.

## Contribution workflow
- Fork or branch, make your changes, then open a Pull Request.
- Use clear commit messages (e.g., gridfinity: add usb-holder-v2 (press-fit update)).
- If your change breaks compatibility (e.g., different hole size), bump the model version (-v3) and explain why in the model README.

## What not to upload
- Copyrighted or trademarked content you don’t own rights to (including logos/characters).
- Illegal or restricted items, or parts primarily intended to enable illegal activity.
- Models that violate the original creator’s license (e.g., “no-derivatives” or disallowing remixes).

## Safety notes
3D printed parts can fail. Do not rely on prints for critical loads, safety gear, medical devices, or anything that could injure people or damage property. Use at your own risk.

## Quick printing tips (house style)
- Orient for strength along load paths; avoid tall, thin towers.
- Prefer 0.2 mm layer height unless otherwise stated.
- Note magnet/screw standards (e.g., Ø6×3 mm magnet, M3x8).
- Include a test piece for tight tolerances when applicable.

## Community
Open an issue or PR to propose categories, templates, or style updates. Be kind, constructive, and have fun. 🤠✨
