---
title: Example 0
keywords: tutorial, example
summary: "Jaroslav's Luminosity Monitor"
sidebar: tutorial_sidebar
permalink: tutorials_example0.html
folder: tutorials
---

## shell commands

```console
source /cvmfs/eic.opensciencegrid.org/x8664_sl7/opt/sphenix/core/bin/eic_setup.sh -n
git clone https://github.com/EIC-Detector/Fun4All-lmon
cd Fun4All-lmon/source
mkdir build
cd build
../autogen.sh -prefix=$HOME/myinstall
make install
source $OPT_SPHENIX/bin/setup_local.sh $HOME/myinstall
cd ../../macros
root.exe
```

## root commands to start the `Geant4 QT` Gui

```cpp
.x Fun4All_G4_Lmon.C(-1)
.L DisplayOn.C
PHG4Reco *g4 = QTGui();
```
## `Geant4` commands

```
/Fun4All/run 1
```

## root commands to start the `root` display

```cpp
.x Fun4All_G4_Lmon.C(-1)
.L DisplayOn.C
PHG4Reco *g4 = DisplayOn();
Fun4AllServer *se = Fun4AllServer::instance();
se->run(1);
displaycmd();
```
