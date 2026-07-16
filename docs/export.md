# Data Saving

You can export your treatment plan from the RapidBrachy module's **Export tab**.

1. Enter the path to your desired output directory.
2. Select a file format from the list of preset configurations:
    - **RapidBrachyGUI**: exports plan formatted for RapidBrachyMCTPS. It can be easily loaded using the Import Plan feature in the **Import tab**.
    - **RapidBrachyMC**: exports plan formatted for if you want to run a Monte Carlo simulation.
    - **DICOM**: exports plan as DICOM files.
3. If you want to export the simulation files for each individual dwell position, select `Prepare for Optimization`. Otherwise, only the files for the combined plan are exported. 
4. Click `Export`.