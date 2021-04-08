---
title: Modular Full Detector Simulation
keywords: [tutorial, example]
tags: [tutorial]
summary: "How to run the Modular Full Detector Simulation"
sidebar: tutorial_sidebar
permalink: tutorials_modular.html
folder: tutorials
---

**Please removet the text and write the Modular detector instruction**

Go to your tutorial root directory

## shell commands

```
source /cvmfs/eic.opensciencegrid.org/ecce/gcc-8.3/opt/fun4all/core/bin/ecce_setup.sh -n
source /cvmfs/eic.opensciencegrid.org/ecce/gcc-8.3/opt/fun4all/core/bin/setup_local.sh $HOME/myinstall
git clone https://github.com/ECCE-EIC/macros
cd macros/detectors/EICDetector
```

## Enable event display

Please edit Fun4All_G4_EICDetector.C to change flag [Enable::DISPLAY = true](https://github.com/ECCE-EIC/macros/blob/bbc89b3341a0de57ca48a80666b39ec1cd65c12f/detectors/EICDetector/Fun4All_G4_EICDetector.C#L234)


## `root` commands to start the Display

```cpp
root
.x Fun4All_G4_EICDetector.C()
se->run(1)
g4->ApplyCommand("/vis/viewer/refresh");
displaycmd() # this one show more Geant4 command we can run from the ROOT prompt
```

{% include links.html %}
