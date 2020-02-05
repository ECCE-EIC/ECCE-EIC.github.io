---
title: Example 2a
keywords: [tutorial, example]
tags: tutorial
summary: "Fast Momentum Resolution Estimate during Design Stage - Analysis"
sidebar: tutorial_sidebar
permalink: tutorials_example2a.html
folder: tutorials
---

Continue with [Example 2](/tutorials_example2.html), and stay in its working directory

## shell commands

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
