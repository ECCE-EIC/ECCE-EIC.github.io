---
title: Day-1 Checklist
keywords: [tutorial]
tags: [tutorial]
summary: "What to check out on Day-1 with ECCE software"
sidebar: tutorial_sidebar
permalink: tutorials_day1.html
folder: tutorials
---
 

Welcome to [ECCE](https://www.ecce-eic.org/)! Here is a check list to get you started on using the ECCE software.

## Sign up

* Software help and discussion chat via BNL [MatterMost](https://mattermost.com/download/) chat
  - The mattermost Fun4All-ECCE channel: [https://chat.sdcc.bnl.gov/eic/channels/fun4all-ecce](https://chat.sdcc.bnl.gov/eic/channels/fun4all-ecce)
  - There are many other Fun4All topical channels under the EIC team too. 
  - If you do not have a BNL account, please email Jin Huang jhuang@bnl.gov to get a direct invitation

* [ECCE email lists](https://www.ecce-eic.org/contact), for example
  - [ECCE public email list](https://lists.bnl.gov/mailman/listinfo/ecce-eic-public-l)
  - [Detector Team discussions and announcements](https://lists.bnl.gov/mailman/listinfo/ecce-eic-det-l)
  - [Physics Benchmark Team discussions and announcements](https://lists.bnl.gov/mailman/listinfo/ecce-eic-phys-l)

## Using ECCE software builds

ECCE software are build daily and distributed over OpenScienceGrid via [ECCE container](https://github.com/ECCE-EIC/Singularity). Using the containerized software builds ensure reproducibility and a binary consistency for studies. 

### Load software container

Get started wtih using the software builds. That includes three options: 
 - If you use BNL RCF (for any experiment account), please jump this step as you can directly use the ECCE software
 - If you have access to a scientific computing center that supports OpenScienceGrid CVMFS, such as at Jlab or CERN, please directly load the ECCE container distributed over  OpenScienceGrid CVMFS: example at [JLab](/tutorials_example2_JLab.html) 
 - If you plan to use on local computers, please check out options of [using ECCE container](https://github.com/ECCE-EIC/Singularity). 
   - For linux workstations and clusters, we suggest [Optiopn-1](https://github.com/ECCE-EIC/Singularity#option-1-mount-eic-cvmfs)
   - For MAC or PC, we suggest using [a linux VM](https://github.com/ECCE-EIC/Singularity/blob/master/VirtualBox.md)
   - For mobile device that may experience internet interuptions, we suggest [Option-2](https://github.com/ECCE-EIC/Singularity#option-2-download-the-eic-fun4all-build-via-https-archive)
 
### Source the environment

This source command setup the environmental variables that enable the use of the lastest build of the ECCE software
```
source /cvmfs/eic.opensciencegrid.org/ecce/gcc-8.3/opt/fun4all/core/bin/ecce_setup.sh -n   # setup environment of newest build
```
*Note, for csh users, please use `/cvmfs/eic.opensciencegrid.org/ecce/gcc-8.3/opt/fun4all/core/bin/ecce_setup.csh` instead*

The ECCE software are pulled from GitHub daily, built and distributed over CVMFS. They are located at `$OFFLINE_MAIN`, which becomes available after the above source. 

There are also weekly archival build of the ECCE software, which are for reproducing past studies, e.g. ana.<number> . To use them we can source with 
```
source /cvmfs/eic.opensciencegrid.org/ecce/gcc-8.3/opt/fun4all/core/bin/ecce_setup.sh -n ana.2  # setup environment of ana.2 build on Apr 4 2021
```

## Get started with ECCE software

Follow a recent tutorial on simulation.
* 10-min tutorials for [![Default macros](https://img.shields.io/badge/reference-macros-green.svg)](https://github.com/ECCE-EIC/macros) 
* Check out the [tutorials](/tutorials_landing_page.html).
* [Mar-2021 ECCE software workshop](https://indico.bnl.gov/event/11112/) - the most recent software workshop with video recording.


## I still have questions, what shall I do?

You are all set to start using ECCE software! If you have question, please feel free to send your question or suggestions here:
* Search for any software pieces on ECCE software via the [doxygen reference site](https://ecce-eic.github.io/doxygen/)
* Ask question on [ECCE software MatterMost chat](https://chat.sdcc.bnl.gov/eic/channels/fun4all-ecce)
* Directly emailing the simulation ([Jin Huang](mailto:jhuang@bnl.gov) and [Cameron Dean](mailto:cdean@bnl.gov)) and [computing](https://www.ecce-eic.org/members) teams


{% include links.html %}
