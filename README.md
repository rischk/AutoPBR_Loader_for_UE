# Auto PBR Loader for Unreal Engine (v3)

This Python script automates the process of importing and assigning PBR texture sets in **Unreal Engine 5**. It supports material creation, reuse, and displacement mapping (if supported by your project setup).

## Features

- Automatically scans a folder for PBR texture sets.
- Creates material instances or base materials.
- Assigns basecolor, normal, roughness, metallic, AO, emissive, opacity, specular, and height/displacement maps.
- Works recursively within folders.
- Updates displacement slot if previously missing.
- Controlled by an external `stop.txt` file (for safe exit from infinite loop).

## Requirements

- Unreal Engine 5+
- Python scripting enabled in the editor
- Valid PBR texture sets with filenames like:  
  `floor_diffuse.jpg`, `floor_normal.jpg`, `floor_disp.jpg`, etc.

## Configuration

Edit the following variables inside the script:

```python
ROOT_DIR = r"D:\Work\Assets\Textures"
DEST_ROOT = "/Game/Materials/Imported"
PARENT_MATERIAL = "/Game/M_Master_PBR"  # Leave empty to create base materials
STOP_FILE = r"D:\Work\Assets\stop.txt"
```

## Usage

1. Place the script into your UE Python scripts directory.
2. Open UE5 and run the script via Python console.
3. To **stop** the loop safely, create an empty file at the `STOP_FILE` path.

---

© 2025 – MIT License. Contributions welcome!
