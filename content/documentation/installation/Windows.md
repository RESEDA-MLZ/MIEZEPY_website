+++
title = "Windows"
weight = 23
+++

# Installing MIEZEPY on Windows OS

Currently Windows only supports an installation through the command prompt. In the following steps we will install python and the required dependencies to run the package both in scripting and GUI mode. Note that at this point the installation of MIEZEPY requires basic knowledge in command prompt.

### 1. Downloading the source

The GitHub repository of the MIEZEPY project can be downloaded here: https://github.com/scgmlz/NSE_Soft. As the download is completed the user is required to unzip the .zip content and open a terminal window in the downloaded folder. This can be done by either right clicking on an empty field within the folder and selecting Open terminal or by directly entering cd Path/to/folder in an already opened terminal window.

![Example image](/img/windows_download.png#center)

### 2. Make sure anaconda is installed

Anaconda (for Windows) can be downloaded here: https://www.anaconda.com/download/#windows
Before installing this software, it is useful to create a separate environment in anaconda. Follow the steps from: https://conda.io/docs/user-guide/tasks/manage-environments.html to create an environment with the current version of python3 (3.7 at 18.12.2018).
Activate this environment.

![Example image](/img/windows_env.png#center)

### 3. Check pip and python installation

In order to install the miezepy package and run it as intended we recommend to use the last versions of python and pip. To check the current version type the following commands into the command prompt window:
```bash
$ python --version
$ pip --version
```
![Example image](/img/windows_python_version.png#center)

### 4. Installing the requirements

The MIEZEPY package has dependencies on some common (like numpy) and less common (like PyQt5) python libraries. These need to be installed in order to launch the package. In any terminal window enter the following commands:

```bash
$ pip install -r requirements.txt
```

On windows, some packages have been specifically compiled to run on the platform and can be installed through the conda repositories. if any of the requirements (listed in requirements.txt) is missing you can attempt to mannually install it. This is, for example, the case of the iminuit minimizer package which can then be installed as follows:

```bash
$ conda install iminuit
```

In the event that you which to completely use the anaconda package manager you can proceed to the following command:

```bash
$ conda install --yes --file requirements.txt 
```

![Example image](/img/windows_requirements.png#center)

It may be necessary to install some packages separately via this installation route as well. Once the requirements are installed a graphical PyQt library and plotting library derived from PyQt and pyqtgraph, can be installed:

```bash
$ pip install git+https://github.com/pyqtgraph/pyqtgraph.git
$ pip install git+https://github.com/AlexanderSchober/simpleplot_qt.git
```

### 5. Installing the software

Finally, the software can be installed through the command:
```bash
$ python setup.py install
```

### 6. Testing the installation

Once the installation is finished the software can be tested by launching the python interpreter through:

```bash
$ python3
    >> import miezepy
    >> miezepy.__version__
```
![Example image](/img/windows_version_test.png#center)