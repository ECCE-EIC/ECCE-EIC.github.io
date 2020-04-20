---
title: Example 1a
keywords: [tutorial, example]
tags: [tutorial]
summary: "Geometry Verification with a Geantino Scan"
sidebar: tutorial_sidebar
permalink: tutorials_example1a.html
folder: tutorials
---

Continue with [Example 1](/tutorials_example1.html), and stay in `g4exampledetector/simple/macros` directory

## shell commands

```
source /cvmfs/eic.opensciencegrid.org/x8664_sl7/opt/fun4all/core/bin/eic_setup.sh -n
source /cvmfs/eic.opensciencegrid.org/x8664_sl7/opt/fun4all/core/bin/setup_local.sh $HOME/myinstall
root.exe
```

## `root` command to run 10000 geantinos

```cpp
.x Fun4All_G4_Geantino.C(10000)
```

## shell commands

```
root.exe HitNtuple.root
```

## `root` commands

```cpp
hitntup->Draw("x1:y1:z1");
hitntup->SetMarkerColor(2);
hitntup->Draw("x0:y0:z0","","same");
```

{% include links.html %}
