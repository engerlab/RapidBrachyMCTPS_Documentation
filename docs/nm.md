# Nuclear Medicine

The RapidBrachyMCTPS standalone app also comes equipped a nuclear medicine module called RapidTheraDose. To access the module, click the **RapidTheraDose Module** ![Logo](img/Logo.png){ width="25" }. In the standalone application, it is available in the top module tab by default. Otherwise, you can find it in the module dropdown under `Nuclear Medicine` > `RapidTheraDose`, or use the `Find Module` button and search for "RapidTheraDose" if you are using RapidBrachyMCTPS as a 3D Slicer custom module.

## Import Tab
Once in the **RapidTheraDose Module**, open the **Import tab**. Here, you can load the required images, structures, and dose files for your plan. **Note**: Your DICOM files must already have be loaded into the Slicer scene before initializing a plan; see the [loading DICOM data section](import.md#loading-and-viewing-data).

Once the DICOM files are loaded into the scene, select an `Image Volume` (CT, MRI, or US Image), `Structure set` (contours), and optionally a `SPECT/PET Volume` or `Dose volume`. Then click `Initialize Plan`, this will enable all other tabs.

## Phantom Tab
The Phantom tab allows you to generate a phantom object, assign materials and densities to contoured structures, and define the phantom resolution. Creating a phantom is required before performing dose calculations or generating EGSphant and `.mac` files.

The typical workflow for creating a phantom is:

1. **Upload a materials table**. The materials table is a plain-text (.txt) file with the same format described in the [Assigning Material and Density section](phantom.md#assigning-material-and-density). The `Hounsfield_Unit` column is not used during in this module, but each row must contain a placeholder numeric value (integer or floating-point) in that column. These values must increase monotonically from top to bottom.
2. **Assign materials to contour structures**. In the Material column, select the desired material for each structure. The corresponding density is automatically populated from the materials table but can be adjusted manually if needed.
3. **Set the phantom resolution**. Specify the voxel resolution in the X, Y, and Z directions.
4. **Click Initialize Phantom**.

## Dose Tab
There are two options for dose calculations:

1. **LDM** (Local Deposition Method).
2. **VSV** (Voxel S-Value).

### LDM
Input the appropriate source metrics and click `Calculate LDM Dose`.

### VSV
TBD

## Export Tab
The export tab allows you to output the following files:

* **EGSphant**: A `.egsphant` file for the phantom generated in the **Phantom tab**.
    * You must enter a name for the `.egsphant` file. The default is `phantom`.
* **CT Plan**: A `.plan` file with uniform activity from a CT contour.
    * You must select an organ/contour to use.
* **NM Plan**: A `.plan` file from a nuclear medicine image (PET or SPECT).
    * You must enter a threshold value: the percentile threshold for selecting hottest voxels.
* **MAC File**: A `.mac` file required to run a Monte Carlo simulation. **Note**: An EGSphant file is also required for Monte Carlo simulations.
    * You must enter the number of computer threads to use during the simulation, the number of histories (number of events/particles to simulate), the atomic mass, and the atomic number.
* **Dose File**: A `.nrrd` dose file for each contour structure as well as the whole image.
* **Metrics JSON File**: A `.json` file containing a summary of the files exported.

