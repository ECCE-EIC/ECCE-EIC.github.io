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
source /cvmfs/eic.opensciencegrid.org/ecce/gcc-8.3/opt/fun4all/core/bin/ecce_setup.sh -n
git clone git@github.com:eic/fun4all_g4exampledetector
cd fun4all_g4exampledetector/simple/source
mkdir build
cd build
../autogen.sh --prefix=$HOME/myinstall
make install
source /cvmfs/eic.opensciencegrid.org/ecce/gcc-8.3/opt/fun4all/core/bin/setup_local.sh $HOME/myinstall
cd ../../macros
root.exe
```
Note: you can use HTTPS to get the example if you don't have an ssh key set up for github but this method will soon be deprecated.
```
git clone https://github.com/eic/fun4all_g4exampledetector.git
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
