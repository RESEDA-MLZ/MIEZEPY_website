---
title: "Windows"
weight: 23
---

# Installing MIEZEPY on Windows OS

Currently Windows only supports an installation through the command prompt. In the following steps we will install python and the required dependencies to run the package both in scripting and GUI mode. Note that at this point the installation of MIEZEPY requires basic knowledge in command prompt.

### 1. Downloading the source

The GitHub repository of the MIEZEPY project can be downloaded here: https://github.com/RESEDA-MLZ/miezepy. As the download is completed the user is required to unzip the .zip content and open a terminal window in the downloaded folder. This can be done by either right clicking on an empty field within the folder and selecting Open terminal or by directly entering cd Path/to/folder in an already opened terminal window.


### 2. Make sure anaconda is installed

Anaconda (for Windows) can be downloaded here: https://www.anaconda.com/download/#windows
Before installing this software, it is useful to create a separate environment in anaconda. Follow the steps from: https://conda.io/docs/user-guide/tasks/manage-environments.html to create an environment with version 3.7 of python. Currently (02.08.2024) newer version are not supported due to some requirement conflicts with simpleplot_qt(https://github.com/AlexanderSchober/simpleplot_qt.git). We are working on fixing this issue. 
Activate this environment.

### 3. Check pip and python installation

In order to install the miezepy package and run it as intended we recommend to use the last versions of python and pip. To check the current version type the following commands into the command prompt window:
```bash
$ python --version
$ pip --version
```

### 4. Installing the requirements

Good news: It is no longer necessary to separately install the requirements. It is done during the installation.

### 5. Installing the software

Finally, the software can be installed through the command:
```bash
$ python setup.py install
```

### 6. Testing the installation

Once the installation is finished the software can be tested by launching the python interpreter through:

```bash
$ python miezepy.py
```
