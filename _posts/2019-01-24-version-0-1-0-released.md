---
type: "post"
title: "Version 0.1.0 released"
description: "This is the first fully functional version of MIEZEPY"
date: 2019-01-24
draft: false
author: "Alexander Schober"
---

# Version 0.1.0 released

This is the first major fully functional release of the miezepy package. It will now enter a life cycle of small feature additions and extensions as well as case optimisation and GUI tweaks. The major additions following version 0.0.1 are the following:

- The addition of a mask editor. It supports the positioning and editing of square, arc and triangular shapes on their own but also as linear and radial compositions. These can be saved/loaded in either during the session save/load or on their own. Note that the file results of a json.dump of a dictionary type structure.

- The addition of a result viewer allows the user to select the reduction result data structure and display it in a simple plot canvas. When the canvas supports 3D surface plotting, a 3D view can be imagined. This allows a more interactive view one the reduced data.

- The reduction panel that consisted merely of script views in v 0.0.1 has now been heavily backed by GUI elements. Yet the script part has not been left out in a way that the GUI write the editable parts of the script and the script can dictate the state of the GUI. This allows to perform hard to implement tasks in the GUI within the script and keep the GUI about essential properties.

#### The future updates a expected to incorporate the following:
- update to the environment widgets visual
- coherent naming of its buttons
- addition of a high exposure foil shape retrieval
- other minor aesthetic and core fixes and modifications
