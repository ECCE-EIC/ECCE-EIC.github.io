---
title: Example 3
keywords: [tutorial, example]
tags: [tutorial]
summary: "Adding Detectors to Existing Setups"
sidebar: tutorial_sidebar
permalink: tutorials_example3.html
folder: tutorials
---

Go to your tutorial root directory

## shell commands

```
source /cvmfs/eic.opensciencegrid.org/ecce/gcc-8.3/opt/fun4all/core/bin/ecce_setup.sh -n
source /cvmfs/eic.opensciencegrid.org/ecce/gcc-8.3/opt/fun4all/core/bin/setup_local.sh $HOME/myinstall
git clone https://github.com/ECCE-EIC/macros
cd macros/detectors/EICDetector
root.exe
```

## `root` commands to start the Display

```cpp
.x Fun4All_G4_EICDetector.C(-1)
.L DisplayOn.C
PHG4Reco *g4 = DisplayOn();
g4->ApplyCommand("/vis/viewer/panTo 0 100 cm")
```

{% include links.html %}
