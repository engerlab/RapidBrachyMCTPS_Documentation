# Nuclear Medicine

The RapidBrachyMCTPS standalone app also comes equipped a nuclear medicine module called RapidTheraDose. To access the module, click the **RapidTheraDose Module** ![rapidbrachyModule](img/rapidbrachyModule.png){ width="25" }. In the standalone application, it is available in the top module tab by default. Otherwise, you can find it in the module dropdown under `Nuclear Medicine` > `RapidTheraDose`, or use the `Find Module` button and search for "RapidTheraDose" if you are using RapidBrachyMCTPS as a 3D Slicer custom module.

## Import Tab
Once in the **RapidTheraDose Module**, open the **Import tab**. Here, you can load the required images, structures, and dose files for your plan. **Note**: Your DICOM files must already have be loaded into the Slicer scene before initializing a plan; see the [loading DICOM data section](import.md#loading-and-viewing-data).

Once the DICOM files are loaded into the scene, select an `Image Volume` (CT, MRI, or US Image), `Structure set` (contours), and optionally a `SPECT/PET Volume` or `Dose volume`. Then click `Initialize Plan`.