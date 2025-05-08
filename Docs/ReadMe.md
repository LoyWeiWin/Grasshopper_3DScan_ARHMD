# 3D Scanning Workflow using Microsoft HoloLens 2 & Grasshopper

This repository provides a Grasshopper-based workflow for 3D scanning physical artifacts using the Microsoft HoloLens 2. The captured data is converted into point clouds, enabling real-time visualization and further geometric processing in Grasshopper.

<img src="https://github.com/LoyWeiWin/Grasshopper_3DScanning/blob/main/Assets/Thumbnails/Img_3DScanningProcedure_UsingMicrosoftHololens2.jpg?raw=true" alt="Scanning Built Artifact" width="500">
*Figure 1: Overview of the scanning process using Microsoft HoloLens 2.*

---

## Table of Contents
- [Key Features](#key-features)
- [Tools & Software Requirements](#tools--software-requirements)
- [Repository Structure](#repository-structure)
- [Getting Started](#getting-started)
- [Launching the Application](#launching-the-application)
- [Using the Computational Workflow](#using-the-computational-workflow)
- [Saving Scanned Data](#saving-scanned-data)
- [Tips for Optimal Performance](#tips-for-optimal-performance)
- [Contributing](#contributing)
- [Acknowledgements](#acknowledgements)

---

## Key Features

- Real-time 3D scanning using mixed reality
- Seamless integration between HoloLens 2 and Rhino/Grasshopper
- Visual feedback and bounding box representations during scanning
- Optional post-processing of point cloud data within Grasshopper

<img src="https://github.com/LoyWeiWin/Grasshopper_3DScanning/blob/main/Assets/Video/Vid_3DScannedStructure.gif?raw=true" alt="Example GIF" width="500">

---

## Tools & Software Requirements

To use this workflow, ensure the following hardware and software are available and properly set up:

### Hardware
- **Microsoft HoloLens 2**  
  - Install the [Fologram app](https://docs.fologram.com/d19731141fc648d08681b02e48652abf).
  - Link the device to your Fologram account.
  - Enable [Research Mode](https://docs.fologram.com/e0299e1613584158b8c9a5ec6d1bfad5#Enabling_Research_Mode) to access depth camera data.

- **Workstation**  
  - Capable of running Rhino 8 and Grasshopper smoothly (moderate to high-spec recommended).

### Software
1. **Rhino 8**  
   - Download trial or full version from [rhino3d.com](https://www.rhino3d.com/download/).

2. **Grasshopper**  
   - Pre-installed with Rhino 8. No separate installation required.

3. **Fologram Plugin for Rhino/Grasshopper**  
   - [Download](https://fologram.com/) and follow [setup instructions](https://docs.fologram.com/06a14a21e33a4406ba047ad84e03c53b#Fologram_for_Rhino).

4. **Volvox Plugin (Optional)**  
   - [Download Volvox](https://www.food4rhino.com/en/app/volvox) if you intend to post-process point cloud data directly in Grasshopper.
   - Alternatively, export point clouds as `.ply` files and use [CloudCompare](https://www.danielgm.net/cc/) for external processing.

---

## Repository Structure

```plaintext
├── GrasshopperFiles/   # Grasshopper scripts for the scanning workflow
├── Assets/             # Images, GIFs, and media files
├── Docs/               # Supplementary documentation and references
```

---

## Getting Started

1. Follow the setup steps for Rhino, Fologram, and HoloLens listed above.
2. Ensure all plugins are correctly installed before proceeding to launch.

---

## Launching the Application

1. **Prepare Your Setup**
   - Open the [Grasshopper definition](https://github.com/LoyWeiWin/Grasshopper_3DScanning/blob/main/GrasshopperFiles/GH_LidarScanningWithFologram.gh).
   - Ensure HoloLens is powered on and Research Mode is enabled.
   - Launch the **Fologram** app on your HoloLens.

   <img src="https://github.com/LoyWeiWin/Grasshopper_3DScanning/blob/main/Assets/Img/IMG_Hololens_DeveloperMode.jpg?raw=true" width="500">

2. **Establish Connection**
   - In Rhino, type `Fologram` in the command line.
   - Open the Fologram panel and click **Connect**.
   - Scan the generated QR code with your HoloLens.

   <img src="https://github.com/LoyWeiWin/Grasshopper_3DScanning/blob/main/Assets/Video/Vid_RegisterCyberPhysicalRealm.gif?raw=true" width="500">

---

## Using the Computational Workflow

1. **Access the Fologram Menu**
   - Raise your palm to access the in-app menu on HoloLens.
   - Tap the purple button for scanning options.

   <img src="https://github.com/LoyWeiWin/Grasshopper_3DScanning/blob/main/Assets/Img/IMG_FologramMenuButton.png?raw=true" width="500">

2. **Begin Scanning**
   - In Grasshopper, activate `00_ClickToScan`.

   <img src="https://github.com/LoyWeiWin/Grasshopper_3DScanning/blob/main/Assets/Img/IMG_FologramInterface.png?raw=true" width="500">

   - Captured objects appear with bounding boxes in AR.

   <img src="https://github.com/LoyWeiWin/Grasshopper_3DScanning/blob/main/Assets/Img/IMG_FologramAfterRecording.png?raw=true" width="500">

3. **Visualize Scanned Regions** *(Optional)*
   - Activate `01_VisualiseScannedRegion` in Grasshopper.

   <img src="https://github.com/LoyWeiWin/Grasshopper_3DScanning/blob/main/Assets/Img/IMG_ActivateScanningVisibility.png?raw=true" width="500">

   > **Note:** This step may reduce performance on some devices.

4. **Reset Scanned Data**
   - Press `02_Reset` to clear all scanned data.

   <img src="https://github.com/LoyWeiWin/Grasshopper_3DScanning/blob/main/Assets/Video/Vid_ResetInputData.gif?raw=true" width="500">

---

## Saving Scanned Data

1. **Internalize Point Cloud Data**
   - After scanning, right-click on the Grasshopper component and choose `Internalize Data`.

   <img src="https://github.com/LoyWeiWin/Grasshopper_3DScanning/blob/main/Assets/Video/Vid_InternalisedData.gif?raw=true" width="500">

---

## Tips for Optimal Performance

- Turn off the visualisation of bounding boxes if you experience lag.
- Keep the HoloLens fully charged during scanning.
- Use the system in a well-lit environment for best results.
- If you are still experiencing issue feel free to read the troubleshooting page.

---

## Contributing

Contributions are welcome and appreciated!

### How to Contribute

- Fork this repository and create a feature branch.
- Make your changes and ensure code consistency.
- Submit a pull request with a descriptive summary.

### Reporting Issues

- Use the [GitHub Issues](https://github.com/LoyWeiWin/Grasshopper_3DScanning/issues) tab.
- Provide context, screenshots, or error logs if applicable.

---

## Acknowledgements

This project was independently developed as a personal research initiative, with the aim of advancing digital fabrication workflows and spatial computing applications.
