# 3D Scanning Workflow for Microsoft HoloLens 2 with Grasshopper

This repository contains a Grasshopper workflow designed to enable Microsoft HoloLens 2 to perform 3D scanning of physical artifacts and convert them into point cloud data. It leverages the capabilities of the HoloLens 2 and integrates seamlessly with Grasshopper for visualization and further processing.

## Features
![ScanningBuiltArtefact](https://github.com/LoyWeiWin/Grasshopper_3DScanning/blob/main/Assets/Thumbnails/Img_3DScanningProcedure_UsingMicrosoftHololens2.jpg?raw=true)
- Capture real-world physical objects and generate point cloud data.
- Seamless integration with Grasshopper for advanced visualization and manipulation.
- Ideal for research, design, and digital reconstruction applications.
![Example](https://github.com/LoyWeiWin/Grasshopper_3DScanning/blob/main/Assets/Video/Vid_3DScannedStructure.mp4).

## Prerequisites
1. **Microsoft HoloLens 2**: Install Fologram plugin to Microsoft HoloLens 2 device & link Fologram account to the device.
2. **Fologram Plugin**: Install the Fologram plugin for Grasshopper. This is essential for enabling communication between HoloLens 2 and Grasshopper.
   - [Download and install Fologram](https://fologram.com/)
3. **Research Mode**: Research Mode must be enabled on the HoloLens 2 to access the infrared (IR) camera, which is critical for scanning.
   - Follow the instructions here to enable Research Mode: [Fologram Research Mode Guide](https://docs.fologram.com/e0299e1613584158b8c9a5ec6d1bfad5#Enabling_Research_Mode)

## Installation
1. Clone this repository to your local machine:
   ```bash
   git clone https://github.com/yourusername/grasshopper_3dscanning.git
   ```
2. Open the Grasshopper files included in the repository using Grasshopper for Rhino.
3. Ensure that the Fologram plugin is installed and properly configured.
4. Enable Research Mode on your HoloLens 2 if not already done.

## Usage
1. Connect the HoloLens 2 to Grasshopper via the Fologram plugin.
2. Launch the scanning workflow provided in the Grasshopper file.
3. Use the HoloLens 2 to scan your physical artifact. The resulting point cloud will be visualized in Grasshopper in real time.
4. Export or process the point cloud data as needed for your research or design purposes.

## Folder Structure
- **`GrasshopperFiles/`**: Contains the Grasshopper scripts for setting up the scanning workflow.
- **`Assets/`**: Includes any supporting files or images for documentation.

## Notes
- Make sure Research Mode is enabled before attempting to use the IR camera for scanning. Refer to [this guide](https://docs.fologram.com/e0299e1613584158b8c9a5ec6d1bfad5#Enabling_Research_Mode) for step-by-step instructions.
- Check the Fologram website for updates and additional support: [https://fologram.com/](https://fologram.com/)

## Contributing
Contributions to improve this workflow are welcome! Please submit pull requests or open issues to share your feedback or enhancements.

---

For any inquiries or assistance, feel free to reach out or open an issue in the repository.
