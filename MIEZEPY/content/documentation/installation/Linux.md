+++
title = "Linux"
weight = 21
+++

# Installing MIEZEPY on Linux
Currently Linux only supports an installation through the terminal. In the following steps we will install python and the recquired dependencies to run the package both in scripting and GUI mode. Note that at this point the installation of MIEZEPY requires basic knowlege in terminal input.

### 1. Downloading the source
![Example image](/img/Linux_open_terminal.png#floatright)The GitHub repository of the MIEZEPY project can be downloaded [here](https://github.com/scgmlz/NSE_Soft). As the download completes the user is recquired to unarchive the .zip content and open a terminal window in the downloaded folder. This can be done by either rightclicking an empty field within the folder and selecting ```Open terminal``` or directly entering ```cd Path/to/folder``` in an already opened terminal window.

### 2. Installing Python 3
The MIEZEPY package has been written exclusively in python and supports only python 3. To this effect an installation of python 3 is reqcuired to run the software. If not already present it is possible to install it through the following command:
```bash
$ sudo apt-get install python3.7
```

Furthermore, we require to install a common package manager for python called pip through:
```bash
$ sudo apt-get install python3-pip
```
The last step might not be necessary as for some python versions pip is included by default. If the installation is sucessfull we can proceed by checking the installation versions:
```bash
$ python3 --version
$ pip3 --version
```
If the above command fails try to replace pip3 ith pip as pip not being installed by default on linux it might select the former namespace. Finnally, the output should be the version numbers of python and pip above 3.6.6 and 18.1 (at the time of writting) respectively.

![Example image](/img/linux_version_test.png#center)


### 3. Installing the dependencies and software
The MIEZEPY package has dependencies on some common (like numpy) and less common (like PyQt) python libraries. These need to be installed in order to launch the package. In any terminal window enter the following commands:

```bash
$ sudo pip3 pip3 install -r requirements.txt
$ sudo pip3 install git+git://github.com/pyqtgraph/pyqtgraph.git
$ sudo pip3 install git+git://github.com/AlexanderSchober/simpleplot_qt.git
```

The first command installs the requirements defined in the requirements.txt file included in the repository. The second line installs a graphical PyQt library and the third command install the ploting library derived from PyQt and pyqtgraph. Finnally the software can be installed through the command:
```bash
$ python3 setup.py install
```

### 4. Testing the installation
Once the installation is finished the software can be tested by launching the python interpreter through:
```bash
$ python3
    >> import miezepy
    >> miezepy.__version__
```
This should provided the version number of the downloaded distribution.



