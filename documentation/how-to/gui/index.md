---
title: "How-To use the GUI"
description: "Introduction on performing basic tasks through the GUI of MIEZEPY "
weight: 111
subtree: /documentation/how-to/gui/
---

## How-To MIEZEPY


### Starting the Program

Right now, there is only the option to start the program via the command line. Open your command line, for example, the Anaconda-Bash. Activate your python3 environment:

```bash
$ activate miezepyenv
```

Run Python and execute:

```bash
$ from miezepy.mieze import Mieze
$ Mieze(True)
```

or just:

```bash
$ python -m miezepy.mieze
```

After the GUI starts, you can choose between the following pages, which are arranged in the order of their typical usage during data reduction: environment handling, data loading, mask creation, data reduction, result plotting, saving, and loading sessions.

### Environments
The first page allows creating and organizing the environments, which are currently opened. The current environment is highlighted and can be seen in brackets after MIEZEPY in the title of the program window. The +/- Buttons (1) allow creating and removing the environments. A proper name (2) should be selected. All the following pages can also be directly accessed through the corresponding buttons (3).

![Environment Tab](EnvironmentOverview.png)
*Fig. 1: The Environment tab: 1: create a new environment 2: name selection 3: switch to the other tabs (data import, mask creation, data reduction, and results) 4: overview of the environment parameters*

### Data Import
Here you want to fill the environment with the suitable data. Go to the data import tab and create a new dataset, typically onew would start with the resolution measurement. Fill it with the corresponding data. It is recommended to previously sort the data by measurement condition, so this step is less messy. Go through the table and identify any tof - files, where wrong metadata were loaded (A typical example would be, that the wavelength was rounded incorrectly (this is a rather common NICOS error) giving 5.997 \AA  instead of 6\AA. Such errors within the metadata can be corrected here.

The import of tof - files, which are provided by the NICOS instrument control software is handled on this page. The GUI is shown in Fig. 1. Again, with the +/- key (1), a new dataset can be added or removed. All datasets of this environment are listed in (2). Every dataset contains the following information:

- **Parameter:** Name your dataset to describe the investigated parameter in an appropriate manner.
- **Measurement:** If you have measured the same parameter (Q, T, B ...) several times, you may want to specify that by giving it different numbers.
- **Reference:** Select if this dataset is your reference/resolution measurement.
- **Background:** Select if this dataset is your background measurement.
- **Visualize (4D):** Visualize the detector images of the various foils and time channels in the dataset.
- The table summarizes all the metadata of the different tof - files. One tof - file is measured at a specific set of first frequency, second frequency, sample-detector distance (LSD), and wavelength. (Additionally, the metadata contain the monitor counts, proportional to the current neutron flux). Therefore, one tof - file corresponds to one row, where the "Echo" (short for spin echo time) is calculated from these four parameters. The "Echo" therefore serves as an index for matching same conditions from different datasets later on). For each tof-file:
    - **cbox_0a_fg_freq_value:** frequency of the first resonant flipper as read from the tof - file
    - **cbox_0b_fg_freq_value:** frequency of the second resonant flipper as read from the tof - file
    - **psd_distance_value:** sample-detector distance as read from the tof - file
    - **selector_lambda_value:** wavelength as read from the tof - file
    - **monitor1:** monitor counts as read from the tof - file
    - **Echo:** Mieze time / spin echo time, as calculated from the following four parameters:
        - **Freq. First:** manipulated value of the first frequency for calculation
        - **Freq. Second:** manipulated value of the second frequency for calculation
        - **lsd:** manipulated value of the sample-detector distance for calculation
        - **Wavelength:** manipulated value of the wavelength for calculation
        - **Monitor:** manipulated monitor counts


A list of the tof - files belonging to one dataset can be selected under "Files" (3). The current tof - file is visualized in (4) to check your selection before loading. With the "Populate this dataset" button, the data from the selected tof - file, as well as the manipulations to the metadata, can be loaded into the selected dataset. The metadata can be manipulated by writing values in the lines (Fig. 2).

- A single value will overwrite ALL entries for this metadata for this dataset.
- A comma-separated list can be used to change each entry separately (in the order they appear in the table). A comma-separated list, which is shorter than the number of entries, will only change the entries covered by the list - remaining entries are not changed.

Note: This will NOT overwrite the tof - files. Thus, your original data remains the same.

![The Data Import tab](data_import.png)
*Fig. 2:The Data Import tab: 1: create a new dataset 2: List of datasets with their information 3: tof - files to be imported into an environment 4: visualization of the integrated intensity in the selected tof - file 5: manipulation of the metadata of the selected dataset 6: validate - checks if input is valid and loads it into the environment.*

### Masks
An integral part of every data reduction is to select where the interesting signal appears on the position-sensitive detector.

![The Mask Creation tab](masks.png)
*Fig.3: The Mask Creation tab: 1: selection of the current mask, when "New..." is selected, you can type the new name in here and confirm with the "Enter" key. 2: Add a new shape to the current mask. 3: Manipulate the shapes within this mask. 4: Visualization of the current shapes.*

### Data Reduction
![Data Reduction 1](data_reduction_1.png)
*Fig. 4: Process Tab*

![Data Reduction 2](data_reduction_2.png)
*Fig. 5: Panel Tab*

![Data Reduction 3](data_reduction_3.png)
*Fig. 6: Script Tab*

### Plotting

### Save/Load



