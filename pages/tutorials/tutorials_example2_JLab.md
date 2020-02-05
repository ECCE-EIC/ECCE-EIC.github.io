---
title: Example 2a
keywords: [tutorial, example]
summary: "Out of box on JLab iFarm: Fast Momentum Resolution Estimate during Design Stage"
sidebar: tutorial_sidebar
permalink: tutorials_example2_JLab.html
folder: tutorials
---

This example is the same as [Example 2a](/tutorials_example2a.html), 
but given specifically for running on [JLab ifarm computer clusters](https://scicomp.jlab.org/). 

## Login into JLab ifarm and start Fun4All-EIC container

```
# on your computer
ssh login.jlab.org

# on login.jlab.org
ssh ifarm1802

# ifarm1802.jlab.org> 
module load /apps/modulefiles/singularity/3.4.0
singularity shell -B /cvmfs:/cvmfs /cvmfs/eic.opensciencegrid.org/singularity/rhic_sl7_ext
export LANG=C
source /cvmfs/eic.opensciencegrid.org/x8664_sl7/opt/sphenix/core/bin/eic_setup.sh -n
```

## Run the simulation in batch mode in [Example 2a](/tutorials_example2a.html)

```
root.exe -q -b Fun4All_G4_Momentum.C\(1000\)
```

## shell commands

```
root.exe FastTrackingEval.root
```

## `root` command

```cpp
tracks->Draw("sqrt(px*px+py*py)/sqrt(gpx*gpx+gpy*gpy)");
tracks->Draw("sqrt(px*px+py*py)/sqrt(gpx*gpx+gpy*gpy)","sqrt(px*px+py*py)/sqrt(gpx*gpx+gpy*gpy)>0.8");
tracks->Draw("dca2d");
tracks->Draw("dca2d","dca2d<0.1");
```

{% include links.html %}
