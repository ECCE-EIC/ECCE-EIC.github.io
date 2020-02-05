---
title: Example 3
keywords: tutorial, example
summary: "Adding Detectors to Existing Setups"
sidebar: tutorial_sidebar
permalink: tutorials_example3.html
folder: tutorials
---

Go to your tutorial root directory

## shell commands

```console
source /cvmfs/eic.opensciencegrid.org/x8664_sl7/opt/sphenix/core/bin/eic_setup.sh -n
source /cvmfs/eic.opensciencegrid.org/x8664_sl7/opt/sphenix/core/bin/setup_local.sh $HOME/myinstall
git clone https://github.com/sPHENIX-Collaboration/macros
cd macros/macros/g4simulations
root.exe
```

## `root` commands to start the Display

```cpp
.x Fun4All_G4_EICDetector.C(-1)
.L DisplayOn.C
PHG4Reco *g4 = DisplayOn();
g4->ApplyCommand("/vis/viewer/panTo 0 100 cm")
```
