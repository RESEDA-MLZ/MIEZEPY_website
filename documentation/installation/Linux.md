---
title: "Linux"
weight: 6
parent: installation
order: 1
---

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MIEZEPY Installation Guide</title>
</head>
<body>

<h1>Installation Guide for MIEZEPY</h1>

<p>Linux is the recommended operating system since the software was mainly developed and tested there.</p>

<p>The GitHub repository of the MIEZEPY project can be downloaded from <a href="https://github.com/RESEDA-MLZ/MIEZEPY">https://github.com/RESEDA-MLZ/MIEZEPY</a> either by downloading and unpacking the .zip version or by cloning via git. After navigating the terminal to the data by e.g.,</p>

<pre>
<code>
$ cd /path/to/my/folder/MIEZEPY-main
</code>
</pre>

<p>To prevent conflicts with already installed Python packages (or installations other than the required version 3.7), we recommend the creation and activation of a new environment. Below is example code taking advantage of the anaconda package manager:</p>

<pre>
<code>
conda create --name miezepyenv python==3.7
conda activate miezepyenv
</code>
</pre>

<p>Afterwards, we update the pip package manager and install the setuptools package via:</p>

<pre>
<code>
python -m pip install -U pip setuptools
</code>
</pre>

<p>The MIEZEPY package depends on some common (like numpy) and less common (like PyQt) python libraries. These will be downloaded and installed via pip during the installation process. To start the process:</p>

<pre>
<code>
python setup.py install
</code>
</pre>

<p>Once the installation is finished, it can be tested by launching the Python interpreter through:</p>

<pre>
<code>
python miezepy.py
</code>
</pre>

<p>(executed inside the MIEZEPY-main folder), which should open the program immediately.</p>

</body>
</html>




