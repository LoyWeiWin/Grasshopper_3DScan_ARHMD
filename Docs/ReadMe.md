# 3D Scanning Workflow using Microsoft HoloLens 2 & Grasshopper

This repository provides a Grasshopper-based workflow that enables 3D scanning of physical artifacts using Microsoft HoloLens 2. The workflow converts scanned data into point clouds for real-time visualization and further geometric processing within Grasshopper.

<img src="https://github.com/LoyWeiWin/Grasshopper_3DScanning/blob/main/Assets/Thumbnails/Img_3DScanningProcedure_UsingMicrosoftHololens2.jpg?raw=true" alt="Scanning Built Artifact" width="500">
*Figure 1: Workflow overview of the scanning process using HoloLens 2.*

## Key Features
<img src="https://github.com/LoyWeiWin/Grasshopper_3DScanning/blob/main/Assets/Video/Vid_3DScannedStructure.gif?raw=true" alt="Example GIF" width="500">

## Tools & Equipment
1. **Microsoft HoloLens 2**: Install the Fologram plugin on the HoloLens 2 device and link your Fologram account to the device.
<<<<<<< HEAD
2. **Workstation**: Capable of operating Rhino & Grasshopper.
=======
2. **Fologram Plugin**: Install the Fologram plugin for Grasshopper. This is essential for enabling communication between HoloLens 2 and Grasshopper.
   - [Download and install Fologram](https://fologram.com/)
3. **Volvox Plugin**: [Download](https://www.food4rhino.com/en/app/volvox). Only download this plugin if you wish to use Grasshopper for post-processing your pointcloud.
>>>>>>> b1a209a1e25c58b54117b806671b8ac5019c47ec

## Repository Structure
- **`GrasshopperFiles/`**: Contains the Grasshopper scripts for setting up the scanning workflow.
- **`Assets/`**: Includes supporting files and images for documentation.
- **`Docs/`**: Includes documentation and references.

<<<<<<< HEAD
## Getting Started

### Tool and Software Requirements
1. Download a trial version of [Rhino 8](https://www.rhino3d.com/download/).
2. Install the [Fologram](https://fologram.com/download) plug-in by following [these](https://docs.fologram.com/06a14a21e33a4406ba047ad84e03c53b#Fologram_for_Rhino) instructions:
4. Install [Volvox](https://www.food4rhino.com/en/app/volvox) plugin if you wish to use the post-processing Grasshopper definition. Alternatively, feel free to export the pointcloud as a ply. file and import to [cloudcompare](https://www.danielgm.net/cc/) for post-processing..

### Connecting to the Microsoft Hololens 2

> Begin by powering on and starting the Hololens.

1. Once the robot is fully powered on, check if `Fologram` is installed in the device

> [!IMPORTANT]  
> If `Fologram` app is not yet been installed. See the installation tips [here](https://docs.fologram.com/d19731141fc648d08681b02e48652abf).

2. Attach the Microsoft Hololens 2 to the [Fologram account](https://docs.fologram.com/dbd97d5d8d2a4233b7a5181a49a3e37d#Attaching_devices_to_your_Fologram_account).

3. Research Mode must be enabled on the HoloLens 2 to access the infrared (IR) camera, which is critical for scanning. Follow the instructions here to enable Research Mode: [Fologram Research Mode Guide](https://docs.fologram.com/e0299e1613584158b8c9a5ec6d1bfad5#Enabling_Research_Mode)

## Launch Application
1. **Prepare Your Setup**
   - Open the [Grasshopper definition](https://github.com/LoyWeiWin/Grasshopper_3DScanning/blob/main/GrasshopperFiles/GH_LidarScanningWithFologram.gh) file provided in this repository.
   - Power on your Microsoft HoloLens 2 and ensure it is properly set up. Ensure **Research Mode** is activated.  
      <img src="https://github.com/LoyWeiWin/Grasshopper_3DScanning/blob/main/Assets/Img/IMG_Hololens_DeveloperMode.jpg?raw=true" alt="Scanning XRStart" width="500">
   - Launch the **Fologram** application on your HoloLens.

2. **Establish Connection**
   - In the Rhino command bar, type `Fologram` to activate the Fologram panel.
   - Click the **Connect** button in the panel. A QR code will appear in Grasshopper.  
   - Scan the QR code with your HoloLens to establish a connection between the HoloLens and Grasshopper.  

      <img src="https://github.com/LoyWeiWin/Grasshopper_3DScanning/blob/main/Assets/Video/Vid_RegisterCyberPhysicalRealm.gif?raw=true" alt="Scanning QR" width="500">


## Using the Computational Workflow / Script(s)
1. **Access the Fologram Menu**
   - Raise your palm facing toward you to pull up the Fologram menu on your HoloLens.  
      <img src="https://github.com/LoyWeiWin/Grasshopper_3DScanning/blob/main/Assets/Img/IMG_FologramMenuButton.png?raw=true" alt="ActivateMenu" width="500">
   - Select the **purple button** to access scanning options.

2. **Begin Scanning**
   - Press the `00_ClickToScan` button in the Grasshopper definition to start scanning.  
      <img src="https://github.com/LoyWeiWin/Grasshopper_3DScanning/blob/main/Assets/Img/IMG_FologramInterface.png?raw=true" alt="Scanning Button" width="500">

   - As you scan, a bounding box will appear around each captured object in the augmented reality (AR) environment.  
      <img src="https://github.com/LoyWeiWin/Grasshopper_3DScanning/blob/main/Assets/Img/IMG_FologramAfterRecording.png?raw=true" alt="ScanningWithBox" width="500">

3. **Visualize Scanned Regions** *(Optional)*  
   - Activate `01_VisualiseScannedRegion` in Grasshopper to view previously scanned regions.  

      <img src="https://github.com/LoyWeiWin/Grasshopper_3DScanning/blob/main/Assets/Img/IMG_ActivateScanningVisibility.png?raw=true" alt="Scanning XRStart" width="500">

   - **Note**: This feature requires significant computational power. If you experience glitches or reduced performance on HoloLens, deactivate this function to improve stability.

4. **Reset Scanned Data**  
   - If you want to discard previously scanned data, press the `02_Reset` button in the Grasshopper definition.
      <img src="https://github.com/LoyWeiWin/Grasshopper_3DScanning/blob/main/Assets/Video/Vid_ResetInputData.gif?raw=true" alt="Scanning ResetInput" width="500">

## Saving Scanned Data
1. **Internalize Point Cloud Data**
   - Once scanning is complete, internalize the point cloud data in Grasshopper to save it.  
         <img src="https://github.com/LoyWeiWin/Grasshopper_3DScanning/blob/main/Assets/Video/Vid_InternalisedData.gif?raw=true" alt="Scanning InternalisedInput" width="500">

## Tips for Optimal Performance
- If you encounter glitches or performance issues while scanning, consider deactivating bounding box visibility. This can significantly improve the AR experience.  
- Ensure the HoloLens is fully charged and operating in a well-lit environment for best results.



=======
>>>>>>> b1a209a1e25c58b54117b806671b8ac5019c47ec
## Contributing
Contributions to improve this workflow are welcome! 

### How to Contribute
- Fork the repository and create a new branch for your changes.
- Ensure code adheres to the existing style and conventions.
- Submit a pull request with a clear description of your changes.

### Reporting Issues
- Use the GitHub Issues tab to report bugs or suggest features.
- Provide a detailed description, including screenshots or logs if possible.

## Acknowledgements
This project was independently developed as part of my personal initiative and commitment to advancing this field.
