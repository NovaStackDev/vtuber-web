# VTuber Base Mesh Web Interface

This is a clean, minimal project structure to load a static base VTuber mesh and swap outfits and eyes using Three.js. 

## Project Scope
**What this project contains:**
- A static base body mesh of the VTuber.
- A wardrobe system for toggling outfits, hair, and eyes.
- The web viewer environment with lighting and orbit controls.

**What this project DOES NOT contain:**
- The full armature / rigging (bones).
- Facial shapekeys for talking or expressions (blendshapes).
- Any animation capability.
- The base `.blend` file or master `.vrm`.

## Why are eyes loaded separately?
The VRM model was exported without the internal eyes meshes because the customized eyes were built as separate `.glb` assets. This allows us to easily swap eye variations in the web interface by loading them dynamically and parenting them to the head region, rather than having them baked directly into the static skin mesh. 

## Contents
- `/animations/` - An empty folder reserved for future animation files (if rigging is ever restored).
- `/characters/` - Contains the base VTuber model `Yuffie.vrm` (No skeleton).
- `/eyes/` - Contains the external GLB eyeball `eyes.glb`.
- `/outfits/` - Contains external GLB outfit and hair models.
- `/src/` - Contains the Three.js web interface (`index.html`).
- `main.py` - Simple Python script to run a local HTTP server.

## How to Run

1. Open your terminal in this directory.
2. Run the server using Python:
   ```bash
   python3 main.py
   ```
3. Open your web browser and go to:
   **http://localhost:8000/src/index.html**
