---
title: Example 2
keywords: [tutorial, example]
tags: [tutorial]
summary: "Fast Momentum Resolution Estimate during Design Stage"
sidebar: tutorial_sidebar
permalink: tutorials_example2.html
folder: tutorials
---

Go to your tutorial root directory

## shell commands

```
source /cvmfs/eic.opensciencegrid.org/x8664_sl7/opt/sphenix/core/bin/eic_setup.sh -n
git clone https://github.com/sPHENIX-Collaboration/tutorials
cd tutorials/Momentum
root.exe
```

## `root` commands to start the Geant4 QT Gui

```cpp
.x Fun4All_G4_Momentum.C(-1)
.L DisplayOn.C
PHG4Reco *g4 = QTGui();
```

## `Geant4` commands

```
/Fun4All/run 1
```

`x-kill` the `Geant4` window and `.q` root when you get the prompt back



{% include links.html %}
