---
title: Example 4
keywords: [tutorial, example]
tags: [tutorial]
summary: "Example Analysis Package"
sidebar: tutorial_sidebar
permalink: tutorials_example4.html
folder: tutorials
---


## shell commands

```
source /cvmfs/eic.opensciencegrid.org/ecce/gcc-8.3/opt/fun4all/core/bin/ecce_setup.sh -n
source /cvmfs/eic.opensciencegrid.org/ecce/gcc-8.3/opt/fun4all/core/bin/setup_local.sh $HOME/myinstall
git clone git@github.com:ECCE-EIC/tutorials
cd tutorials/AnaTutorialECCE/src
mkdir build 
cd build
../autogen.sh --prefix=$HOME/myinstall
make install
```

## Run example pythia event

```
cd ../../macro
root.exe
.x Fun4All_G4_EICDetector_AnaTutorial.C(3)
```

The event run is a dummy 5 pion event and is simply intended as an example. Take a look at the AnaTutorial source code to learn more about different accessible physics objects.


## Run with production data

You can use the AnaTutorial (or any analysis package that you write) to run over the produced DST data. To do this, download an example DST and run the provided macro over it as follows. First, change to the macros directory, e.g. `cd AnaTutorialECCE/macro`. Then, download an example DST and run the provided macro

```
mcs3 cp eicS3/eictest/ECCE/MC/ana.14/5f210c7/SIDIS/pythia6/ep_18x100highq2/DST_SIDIS_pythia6_ep_18x100highq2_039_0099000_01000.root .
root.exe
.x Fun4All_ReadDST.C(1,"DST_SIDIS_pythia6_ep_18x100highq2_039_0099000_01000.root")
```

{% include links.html %}
