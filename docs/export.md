# Data Saving

You can export your treatment plan from the RapidBrachy module's **Export tab**.

1. Enter the path to your desired output directory.
2. Select a file format from the list of preset configurations:
    - **RapidBrachyMC**: exports plan formatted for if you want to run a Monte Carlo simulation.
    - **Slicer**: exports plan in 3D Slicer format (scene).
    - **DICOM**: exports plan as DICOM files.
    - **brachyutils**: export as files readable by brachyutils (.nrrd and .json).
3. If you want to export the simulation files for each individual dwell position, select `Prepare for Optimization`. Otherwise, only the files for the combined plan are exported. 
4. Click `Export`.