[![OpenFOAM version](https://img.shields.io/badge/OpenFOAM-4-brightgreen)](https://github.com/OpenFOAM/OpenFOAM-4)

Use coded function in controlDict to reconstruct the mesh and fields in the run time.

# autoReconstructPar
> In old version OpenFOAM. The Parallel IO file handler, e.g., fileHandeler collated, was not available, and thus leads to large number of files in each processors. However, many supercomputer has a file number limit, may leads to the runing case termination. This repository provide a function which can reconstrut fields in processors (and also delete the files in processors if you want) and thus avoiding termination of the runing cases due to large number of files.

## How to use it
Add the file in autoReconstructParDict `system` folder and then add the following function into `system/controlDict`,
```C++
functions
{
    #include "autoReconstructParDict"
}
```
