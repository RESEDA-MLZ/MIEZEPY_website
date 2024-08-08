---
title: "Linux"
weight: 011
---

Linux is the recommended operating system since the software was mainly developed and tested there.

The GitHub repository of the MIEZEPY project can be downloaded [here](https://github.com/RESEDA-MLZ/MIEZEPY) either by downloading and unpacking the .zip version or by cloning via git. After navigating the terminal to the data by, e.g.,

```bash
$ cd /path/to/my/folder/MIEZEPY-main
```


To prevent conflicts with already installed Python packages (or installations other than the required version 3.7), we recommend the creation and activation of a new environment. Below is example code taking advantage of the anaconda package manager:

```bash
    conda create --name miezepyenv python==3.7
    conda activate miezepyenv
 ```

Afterwards, we update the pip package manager and install the setuptools package via:

```bash
    python -m pip install -U pip setuptools
```

The MIEZEPY package depends on some common (like numpy) and less common (like PyQt) python libraries. These will be downloaded and installed via pip during the installation process. To start the process:

```bash
    python setup.py install
```

Once the installation is finished, it can be tested by launching the Python interpreter through:

```bash
    python miezepy.py
```

(executed inside the MIEZEPY-main folder), which should open the program immediately.





