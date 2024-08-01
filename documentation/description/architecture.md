---
title: "Architecture"
description: "Description of the software architecture"
weight: 42
---

### MIEZEPY Architecture

During the development of MIEZEPY a strong emphasis was done to separate individual components. The three main components are the data, the process and reduction routines and the visualization components. Upon loading the core is initialised without any content. At this point the user can chose to initialize an arbitrary number of environments. Each one of those will initialize five distinct components:

- <b> The io handler </b> in charge of importing, exporting the data, environment variables, fitting parameters and results. It is the main worker for input output as does not contain any hardcoded references to the other objects of the environment.

- <b> The data structure </b> is a self contained instance that is capable of handing data input with associated metadata and the axes. Each data element is index to a position in the axis space. It possess setters, getters as well as reduction routines. 

- <b> The fitting class </b> is assimilated to a dictionary of functions that can perform various tasks. The base functions (the ones to be called), all get fed the environment and output the fit result into the results class.

- <b> The results class </b> holds in place the computation results of the fitting class. This allows the fitting class to stay clean of any data. The results are ordered in result objects that can be retrieved through their dictionary key. 

- <b> The procedure class </b> can be seen as the surface layout that will make all work together in a neat way. It is in charge to handle the user commands and grab the data and fitting classes to feed the result. Only the io procedures are independent from this. 

The diagram below gives a visual interpretation of the introduced classes. 
![Example image]({{ site.baseurl }}/img/architecture_diagram.png#center)

As you can also see on the present diagram the GUI component is decoupled of the Core. This has the advantage that MIEZEPY does not rely on the GUI to fucntion, thus can be launched in a Jupyter notebook. 
