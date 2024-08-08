---
title: "Windows"
weight: 012
---


## Windows Installation

Since the program is based on Python, it also works under Windows, with different aspects having to be considered:

### Preparations
It is recommended to install Python via the Anaconda package. A Win10 version can be found here: [https://www.anaconda.com/download/#windows](https://www.anaconda.com/download/#windows). After you have installed Anaconda, we recommend creating a separate environment within Anaconda solely for MIEZEPY. This ensures that all packages for MIEZEPY are kept together and no dependencies are overwritten when installing other Python software. The full instructions for environments can be found here: [https://conda.io/docs/user-guide/tasks/manage-environments.html](https://conda.io/docs/user-guide/tasks/manage-environments.html).

To create an environment, open the Anaconda Prompt, which is also the recommended command line on Windows for interacting with Anaconda/Python.

![Anaconda Prompt on Windows 10](AnacondaPromptWin10.png)
*Caption*

A new environment named "miezepy", with Python 3.7 and the required modules can be created with the command:

```bash
        conda create --name miezepy python==3.7
```

Afterwards, update pip and install the most recent version of setuptools:

```bash
        python -m pip install -U pip setuptools
```

Additionally, the installation of the PyQt5 package requires the installation of C++ compiler tools, e.g., via Visual Studio. On Windows 10, open Visual Studio and select modify.

### Installing the Software

The GitHub repository of the MIEZEPY project can be downloaded here: [https://github.com/RESEDA-MLZ/MIEZEPY](https://github.com/RESEDA-MLZ/MIEZEPY). (Ideally, the git repository can also be cloned, if you are familiar with git.) As the download is completed, the user is required to unzip the .zip content and open a terminal window in the downloaded folder. This can be done by either right-clicking on an empty field within the folder and selecting "Open terminal" or by directly entering:

```bash
        cd Path/to/folder
```

in an already opened terminal window.


