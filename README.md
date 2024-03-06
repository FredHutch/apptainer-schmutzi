# Container Build for schmutzi

This repository contains a .def file for building a container for use with Apptainer.  The container created by this will contain the scripts, binaries, and supporting files for [schmutzi](https://github.com/grenaud/schmutzi/):

> schmutzi is a set of programs aimed at ancient DNA data that can :
>  - estimate contamination based on deamination patterns alone
>  - call a mitonchondrial consensus for the endogenous genome. This consensus calls takes into account contamination and deamination.
>  - estimate mitonchondrial contamination and identify the most likely contaminant from a set.

# Use

Schmutzi tools are not run by default- it is necessary to use `apptainer exec schmutzi.sif <command>` to run the desired Schmutzi tool.  These tools are installed to `/usr/bin`.

# Building

`apptainer build schmutzi.sif schmutzi.def`

## Notes

 - This will not build with later GCC versions.  Versions 8 and 9 are known to work.  Version 11 and later are known to fail.
