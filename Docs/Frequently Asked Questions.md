# Frequently Asked Question(s)
1. "Why is my scan not appearing in Grasshopper?"
- Potential root cause: Ensure the HoloLens is properly connected to the computer.
- Potential root cause: Visibility of the bounding boxes is deactivated. 
   <img src="https://github.com/LoyWeiWin/Grasshopper_3DScanning/blob/main/Assets/Img/IMG_ActivateScanningVisibility.png?raw=true" alt="Fail" width="500">


2. "How can I improve scan quality?"
- Solution: Ensure sufficient lighting in the scanned environment.
- Alt Solution: Using visual market (e.g) to improve the spatial anchoring.

3. "Why Microsoft Hololens 2 does not appear within the Grasshopper environment?" or "My device failed to connect to the Fologram session"  
   <img src="https://github.com/LoyWeiWin/Grasshopper_3DScanning/blob/main/Assets/Img/IMG_Fologram_Fail1.png?raw=true" alt="Fail" width="500">

- Issue: Connection errors between Microsoft HoloLens and Grasshopper. 
- Solution: Use `XR Start` in the Rhino command, then select `Start New Session`. 

   <img src="https://github.com/LoyWeiWin/Grasshopper_3DScanning/blob/main/Assets/Img/IMG_Fologram_Fail1_Solution1.1.png?raw=true" alt="Scanning XRStart" width="500">  
   <img src="https://github.com/LoyWeiWin/Grasshopper_3DScanning/blob/main/Assets/Img/IMG_Fologram_Fail1_Solution1.2.png?raw=true" alt="RestartScanning" width="500">

4. "Why my scanned data is incomplete?"
- Issue: IR camera has limited field of view, so make sure you thoroughly scan the built artefact from different angles. 