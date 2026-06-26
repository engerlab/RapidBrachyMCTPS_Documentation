# Dose

Importing and calculating doses can be performed from the **Dose tab** of the RapidBrachy module.

## Importing Dose Files
You can import an individual dose file or an entire dose directory by entering the file path into either the `Load Dose File` or `Load Dose Folder` fields.

## Calculating a Dose
Before running a dose calculation, verify that you have completed your setup. Ensure you have:

* Configured all catheters and applicators (if applicable)
* Defined the brachytherapy source
* Initialized your phantom

Enter the desired prescription dose in Grays. Select your desired algorithm for the dose calculation; RapidBrachyMCTPS is equipped with both the conventional TG-43 formalism and a Geant4-based Monte Carlo (MC) engine.

#### TG-43
1. Enter the path to the TG-43 parameter data, it should have a default path.
2. Click `Calculate Dose`.
3. The dose will be loaded and the catheter table will be populated. The catheter table dwell times can be manually modified.

#### MC
To perform Monte Carlo simulations, you will need to have installed RapidBrachyMC. See the instructions on [installing RapidBrachyMC](installation.md#installing-rapidbrachymc) for details.

1. Enter the path to the RapidBrachyMC executable.
    - If you installed RapidBrachyMC from source, set the path to the executable named `RapidBrachyMC`.
    - If you are using the RapidBrachyMC Docker image, the path should be automatically set to **http://172.30.10.11:8000/calculate_dose_mc**
        - **Note**: if you are using Windows and you are running Docker Desktop, you will need to manually change the path to **http://127.0.0.1:8000/calculate_dose_mc**
2. Enter the path to the desired output directory.
3. Enter the desired number of histories. This refers to the number of simulation trials.
4. Enter the number of threads (computer cores).
5. Enter a random seed for the simulation.
6. Click `Calculate Dose`.
7. The dose will be loaded and the catheter table will be populated. The catheter table dwell times can be manually modified.