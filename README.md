# SDMD
This repository contains jupyter notebook associated with the manuscript "Harnessing regulatory sequences to combine homing and sex distortion for population control of the human malaria vector *Anopheles gambiae*". The notebooks and associated files contain code needed to reproduce the analysis and figures associated with the modelling aspect of the manuscript.

Silvia Grilli[^1], Oksana Vertsimakha[^1], Louise Marston[^1], Irati Aramburu Gonzalez[^1], Austin Burt[^1], Andrea Crisanti[^1], Federica Bernardini[^1]

[^1]: Department of Life Sciences, Imperial College London, London, UK.

For correspondence regarding the code: oksana.vertsimakha22@imperial.ac.uk



## Requirements 
Julia 1.10.1 or above

Jupyter notebook

This analysis was performed on Windows 11 Enterprise, any system which can run Julia 1.10.1 should be suitable.

All necessary packages and dependencies can be installed by running the following code in Julia from the folder containing downloaded files (SDMDModel.ipynb, SDMDSimulations.ipynb and folder Environement). The code only needs to be run once.
```
using Pkg
Pkg.add("NBInclude")  

using NBInclude
@nbinclude("./Environment/Setup0.ipynb");
```
The dependencies can also be installed manually:
```
CairoMakie v0.14.0
DataFrames v1.7.0
Distributions v0.25.120
JLD2 v0.5.13
NBInclude v2.4.0
PrettyTables v2.4.0
ProgressMeter v1.10.4
SplitApplyCombine v1.2.3
StatsBase v0.34.5
Random
Statistics v1.10.0
```
Once the packages are installed, the following code should be run o initiate the environment (should be run at the start of each session):
```
using Pkg
Pkg.activate("./Environment/")
Pkg.instantiate()
```
To use the modelling functions, run
```
include("SDMDModel.jl")
```
The code and instructions are also provided in the SDMDSimulations.ipynb file.
## User notes
The SDMDModel.ipynb is a jupyter notebook that contains the code for the model as described in the paper as well as supplementary functions.

The SDMDSimulations.ipynb is a jupyter notebook that contains the code used to generate the figures and sumaltions data used in the modelling results.

## Timing
Installation is not expected to take more than 5 minutes

For both ideaised and empirical parameters, the simulations take less than 2 minultes in total (100 repetitions for each strategy). Depending on the number of repetitions, the simulations can take few minuted longer.


