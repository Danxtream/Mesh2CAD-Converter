# Mesh2CAD Converter
## Unified STL/STEP Processing Tool

**Version:** 1.0.0  
Please consider donating if you enjoy using the product.
\
**Website:** https://danxtream.gumroad.com/l/Mesh2CADConverter

---

## Overview

Mesh2CAD Converter is a comprehensive tool for processing and converting 3D mesh files (STL) and STEP files with plane and cylinder detection capabilities. The software transforms triangulated meshes into parametric CAD-ready geometry through intelligent surface recognition and reconstruction.

---


## Examples

### Before

### After

### Before

### After

### Before

### After

---

## Key Features

### File Processing
- **STL to STEP Conversion**: Convert triangulated STL meshes to exact triangular STEP format
- **STEP Processing**: Load and process existing STEP files with mesh tessellation
- **Batch Processing**: Process multiple files simultaneously
- **Drag & Drop Support**: Easy file import via drag and drop

### Geometry Detection
- **Plane Detection**: Automatically identify and reconstruct planar surfaces
  - Adjustable angle tolerance (0.1° - 45°)
  - Configurable projection tolerance

  
- **Cylinder Detection**: Advanced primitive fitting for cylindrical surfaces
  - Configurable fitting tolerances
  - Works in combination with plane detection

### Advanced Options
- **Custom Presets**: Save and manage multiple configuration presets
- **Stitching**: Automatic face stitching with configurable tolerances
- **Mixed File Support**: Process STL and STEP files together

---

## Installation

1. Download the Mesh2CAD Converter executable
2. Extract Mesh2CAD folder to a folder of your choice
3. Run `Mesh2CAD.exe`
4. No additional installation required - all dependencies are bundled
   

**Note**: The executable is portable and does not require administrator privileges for normal operation.

---

## Usage Guide

### Basic Workflow

1. **Import Files**
   - Click "Import Files (STL or STEP)" or drag files into the window
   - Supports .stl, .STL, .step, and .STEP formats
   - Multiple files can be processed in batch

2. **Select Processing Options**
   - Enable "Detect Planes" for planar surface reconstruction
   - Enable "Detect Cylinders" for cylindrical surface detection
   - Adjust tolerance parameters as needed

3. **Configure Parameters**
   - **Angle Tolerance**: Maximum angle difference for merging faces
   - **Tolerance (mm)**: Maximum projection distance for validation
   - **Stitch Tolerance**: Face stitching tolerance after detection

4. **Start Processing**
   - Click "Start Processing" to begin
   - Monitor progress in the processing dialog
   - Cancel operation if needed

5. **Export Results**
   - View processed files in the "Export Files" section
   - Use "Export All" or "Export Selected" to save results
   - Files can be renamed by double-clicking in the list

### Working with Presets

- **Create Preset**: Click "New" button next to the preset dropdown
- **Load Preset**: Select from dropdown menu
- **Delete Preset**: Click "Delete" button (cannot delete "Defaults")
- Presets are saved automatically and persist between sessions

### Tips for Best Results

#### Plane Detection
- Start with low angle tolerance (0.5°) for precise surfaces
- Increase tolerance for rough or noisy meshes
- Lower projection tolerance for stricter validation
- Use higher stitch tolerance for meshes with gaps

#### Cylinder Detection
- **Important**: Cylinder detection requires plane detection to be enabled first for STL files
- For STEP files with existing planes, cylinder detection can run independently
- Increase angle tolerance (2-5°) for better curved surface capture
- Adjust tolerance based on cylinder radius and mesh quality

#### Performance
- Process files in smaller batches for very large meshes
- Close other applications to free up memory

---

## Interface Guide

### Main Sections

1. **Import Files**
   - File list with drag & drop support
   - Remove selected files button
   - File count display

2. **Processing Options**
   - Scrollable parameter panel
   - Separate plane and cylinder configuration
   - Preset management
   - Start processing button

3. **Export Files**
   - Output file list
   - Export all/selected buttons
   - File renaming support
   - Remove selected files

### Keyboard Shortcuts

- **Ctrl+V**: Paste files (in Import section)
- **Ctrl+C**: Copy files (in Export section)
- **Double-Click**: Rename output file
- **Delete**: Remove selected file

### Context Menus

- **Right-click Import List**: Paste, Remove Selected
- **Right-click Export List**: Copy Files, Remove Selected

---

## Dark Mode

Toggle dark mode via the Settings button (gear icon):
- **Light Mode**: Traditional light interface with blue accents
- **Dark Mode**: Dark grey interface optimized for low-light use

Settings are saved automatically between sessions.

---

## Configuration Files

Application data is stored in:
```
%LOCALAPPDATA%\Mesh2CAD\
```

Contains:
- `configs.json`: User presets and settings
- `temp_output\`: Temporary processing files (auto-cleaned)


## Troubleshooting

### Possible Issues

**Program won't start**
- Ensure all files were extracted from the archive
- Check Windows Defender/antivirus hasn't quarantined files
- Try running as administrator

**Processing fails**
- Verify input files are valid STL/STEP formats
- Check file isn't corrupted or password-protected
- Ensure sufficient disk space in temp directory
- Try processing files individually

**Cylinder detection errors**
- Enable plane detection first for STL files
- Verify STEP files have existing plane surfaces
- Increase angle tolerance for rough surfaces
- Check mesh quality and repair if needed

**Export access denied**
- Choose a different export folder
- Run program as administrator
- Check folder permissions
- Close files if open in other programs

**Memory errors**
- Process fewer files at once
- Close other applications
- Restart the program
- Use smaller mesh files or simplify geometry


## Limitations

- Maximum recommended mesh size: 10 million triangles
- Cylinder detection requires prior plane detection (STL only)
- Complex non-planar surfaces may not reconstruct perfectly
- Very small features (< 0.1mm) may be filtered out
- Stitching may fail on meshes with large gaps or inconsistent normals

---

## Support

I will not promise any support for this product. Use it as is, or dont.

---

## License

This software is licensed for commercial and personal use.  
See LICENSE.txt for full terms and conditions.  
Source code for the compiled executable is proprietary and not open source.  


---

## Version History

**v1.0** (Initial Release)
- STL to STEP conversion
- Plane detection with region growing
- Cylinder detection
- Batch processing
- Custom presets
- Dark mode support
- Drag & drop interface
