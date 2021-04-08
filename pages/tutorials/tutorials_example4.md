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
cd AnaTutorial/src
mkdir build 
cd build
../autogen.sh --prefix=$HOME/myinstall
make install
```

## Run example pythia event

```
cd ../../macro
root.exe
.x Fun4All_AnaTutorial_Jets.C\(3\)
```

The pythia event is a p+p event and is just meant as an example. Take a look at the AnaTutorial source code to learn more about different accessible physics objects.


{% include links.html %}
