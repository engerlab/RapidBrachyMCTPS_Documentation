# Getting Started

## Installation Guide
There are two options when installing RapidBrachyMCTPS:

1. **Installing the RapidBrachyMCTPS standalone application.**
2. **Running the RapidBrachy software as a custom module in 3D Slicer.**

We recommend the **Standalone Application** for users who want a streamlined, turnkey experience, and the **Custom Slicer Module** for users who want to take advantage of the full 3D Slicer ecosystem, including its extensive collection of extensions.

| Feature | Standalone App | Custom Module (3D Slicer) |
|---|---|---|
| **Best For** | Streamlined, turnkey workflows | Advanced workflows with the full 3D Slicer ecosystem |
| **Setup** | Download and run | Requires 3D Slicer, brachyutils, and RapidBrachy installations |
| **Interoperability** | Isolated environment | Works alongside other Slicer extensions |

---
### Standalone Application
This version includes everything you need to run RapidBrachyMCTPS right out of the box.

1. Download the latest release from the OneDrive (provided from engerlab).
2. Extract the downloaded archive to your preferred directory.
3. Run the `RapidBrachyMCTPS` executable file.


### 3D Slicer Custom Module
If you prefer to use 3D Slicer's full capabilities while still utilizing the features from RapidBrachyMCTPS or you already use 3D Slicer and want to add RapidBrachyMCTPS to your existing toolkit, you can do so by installing RapidBrachy as a custom module.

To get started, install [3D Slicer](https://www.slicer.org/). Then clone the repositories [RapidBrachyGUI](https://github.com/engerlab/RapidBrachyGUI.git) and [brachyutils](https://github.com/engerlab/brachyutils). We recommend the location `${HOME}/Software/` for cloning these repositories.

#### Install brachyutils
You'll need to install brachyutils inside 3D Slicer's python environment. Launch the 3D Slicer interface and inside the Python Console, run:
```python
from slicer.util import pip_install
pip_install("-e /Path/To/brachyutils")
```
Note: if you are using **Windows**, the Path/To/brachyutils should take forward slashes '/' and not backslashes '\\'.

Restart 3D Slicer, then run 
```python
import brachyutils
``` 
in the Python console to make sure the module is installed. You may get pydantic warnings, ignore them.

#### Install SlicerRT
Next, you'll need to install SlicerRT. Open 3D Slicer, click on `Extension Manager` ![extension_manager](img/extension_manager.png){ width="25" } and type SlicerRT in the search bar. Install SlicerRT and restart 3D Slicer.

#### Install RapidBrachyGUI
Next, you'll need to install RapidBrachyGUI. Open 3D Slicer, click on `Edit`, then open `Application Settings`. On the left panel, click `Modules`, go to the `Additional module paths:` and add the path to RapidBrachyGUI. Then restart 3D Slicer.

![edit](img/edit.png){ width="400" }

![modules](img/modules.png){ width="600" }

![add](img/add.png){ width="600" }

![path](img/path.png){ width="600" }


To access the RapidBrachy module, either search for it using the module search bar or select `Brachytherapy` from the module dropdown menu and choose RapidBrachy.

For easier access, it is recommended to add RapidBrachy to your favorites toolbar. To do this, once again open `Edit`>`Application Settings`>`Modules`. This time, in the Modules list, scroll down to find RapidBrachy, then drag and drop it into the Favorite Modules list and click OK.

RapidBrachy will now appear in the toolbar at the top of the screen, allowing you to access it quickly at any time.

### Installing RapidBrachyMC
If you will want to run Monte Carlo simulations, you will need to install [RapidBrachyMC](https://github.com/engerlab/RapidBrachyMC), the Geant4-based Monte Carlo engine. You have two options when installing RapidBrachyMC:

1. Installing the RapidBrachyMC Docker image.
2. Installing RapidBrachyMC from source.

#### Using Docker Image (Recommended)
Download the docker image (rapidbrachy_mc.tar) from the OneDrive and place it in your desired location. 

* If you are using **Linux**, you will need to install [Docker Engine](https://docs.docker.com/engine/install/).
* If you are using **Windows**, you will need to install [Docker Desktop](https://docs.docker.com/desktop/setup/install/windows-install/). 

Then run this command in the Terminal/PowerShell:
```sh
docker load -i Path/To/rapidbrachy_mc.tar
```

#### Installing from source
You will need permission from engerlab to clone the [RapidBrachyMC GitHub Repository](https://github.com/engerlab/RapidBrachyMC) to install from source. Installation instructions are found in the README file of the repository.

### For Developers
If you are developing this module, enable Developer Mode in Slicer by navigating to `Edit` > `Application` > `Settings` > `Developer` and clicking `Enable developer mode`.

## Dark Mode
Dark mode is recommended, but it is up to personal preference. You can select the appearance mode by clicking **Edit** on the top left and navigating to **Application Settings > Appearance**, under **Style**, select your preferred style.