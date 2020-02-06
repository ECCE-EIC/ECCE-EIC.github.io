---
title: Example 1
keywords: [tutorial, example]
tags: [tutorial]
summary: "A simple Detector with Hardcoded Geometry"
sidebar: tutorial_sidebar
permalink: tutorials_example1.html
folder: tutorials
---

## shell commands

```
source /cvmfs/eic.opensciencegrid.org/x8664_sl7/opt/sphenix/core/bin/eic_setup.sh -n
git clone https://github.com/EIC-Detector/g4exampledetector
cd g4exampledetector/simple/source
mkdir build
cd build
../autogen.sh --prefix=$HOME/myinstall
make install
source /cvmfs/eic.opensciencegrid.org/x8664_sl7/opt/sphenix/core/bin/setup_local.sh $HOME/myinstall
cd ../../macros
root.exe
```

## root commands to start the `Geant4 QT` Gui

```cpp
.x Fun4All_G4_Example01.C(-1)
.L DisplayOn.C
PHG4Reco *g4 = QTGui();
```
## `Geant4` commands

```
/Fun4All/run 1
```

x-kill the Geant4 window and .q root when you get the prompt back



{% include links.html %}
