# Data Saving

You can export your treatment plan from the RapidBrachy module's **Export tab**.

1. Enter the path to your desired output directory.
2. Select a file format from the list of preset configurations:
    - **RapidBrachyGUI**: Exports the plan in the RapidBrachyMCTPS format. The exported plan can be loaded using the Import Plan feature in the **Import tab**. **Note**: Plans imported this way cannot later be exported as DICOM. If you also need a DICOM version of the plan, export it now.
    - **RapidBrachyMC**: Exports plan formatted for if you want to run a Monte Carlo simulation.
    - **DICOM**: Exports plan as DICOM files. **Note**: Currently, only RTPlan dwell times are updated; all other DICOM objects are exported unchanged.
3. If you want to export the simulation files for each individual dwell position, select `Prepare for Optimization`. Otherwise, only the files for the combined plan are exported. 
4. Click `Export`.