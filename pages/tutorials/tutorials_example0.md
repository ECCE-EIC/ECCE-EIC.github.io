---
title: Example Luminosity Monitor
keywords: [tutorial, example]
tags: [tutorial]
summary: "Jaroslav's Luminosity Monitor"
sidebar: tutorial_sidebar
permalink: tutorials_example0.html
folder: tutorials
---

## shell commands

If you are using <span style="color: blue;">**bash**</span> as your shell, you need to source the <span style="color: blue;">**.sh**</span> scripts, if you have <span style="color: red;">**tcsh**</span> or <span style="color: red;">**csh**</span> as shell you need to source the <span style="color: red;">**.csh**</span> scripts. If you are not sure, use

echo $SHELL

which will tell you which is your shell (<span style="color: blue;">**/bin/bash**</span>, <span style="color: red;">**/bin/csh**</span>, <span style="color: red;">**/bin/tcsh**</span>)



    for bash use: source /cvmfs/eic.opensciencegrid.org/x8664_sl7/opt/fun4all/core/bin/eic_setup.sh -n
    for tcsh use: source /cvmfs/eic.opensciencegrid.org/x8664_sl7/opt/fun4all/core/bin/eic_setup.csh -n
    git clone https://github.com/EIC-Detector/Fun4All-lmon
    cd Fun4All-lmon/source
    mkdir build
    cd build
    ../autogen.sh --prefix=$HOME/myinstall
    make install
    for bash use: source /cvmfs/eic.opensciencegrid.org/x8664_sl7/opt/fun4all/core/bin/setup_local.sh $HOME/myinstall
    for tcsh use: source /cvmfs/eic.opensciencegrid.org/x8664_sl7/opt/fun4all/core/bin/setup_local.csh $HOME/myinstall
    cd ../../macros
    root.exe


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

{% include links.html %}

