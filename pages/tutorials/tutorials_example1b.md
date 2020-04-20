---
title: Example 1b
keywords: [tutorial, example]
tags: [tutorial]
summary: "Saving and Reading a Chain Snapshot"
sidebar: tutorial_sidebar
permalink: tutorials_example1b.html
folder: tutorials
---

Continue with [Example 1](/tutorials_example1.html), and stay in `g4exampledetector/simple/macros` directory

## shell commands

```
source /cvmfs/eic.opensciencegrid.org/x8664_sl7/opt/fun4all/core/bin/eic_setup.sh -n
source /cvmfs/eic.opensciencegrid.org/x8664_sl7/opt/fun4all/core/bin/setup_local.sh $HOME/myinstall
root.exe
```

## `root` command to run 10000 geantinos and write Dst

```cpp
.x Fun4All_G4_Write_Dst.C(10000)
```

## shell commands

```console
root.exe
```

## `root` command to read Dst and write ntuple

```cpp
.x Fun4All_Read_Dst.C(0)
```

## shell commands

```
root.exe HitsFromDst.root
```
## `root` command 

```cpp
hitntup->Draw("x1:y1:z1");
hitntup->SetMarkerColor(2);
hitntup->Draw("x0:y0:z0","","same");
```


{% include links.html %}
