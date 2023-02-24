# HInvisible

Higgs to invisble selection for FCCee


## Initial Setup

Clone the repository, including the FCCAnalyses submodule.

Via ssh:
```shell
git clone --recurse-submodules git@github.com:BNL-FCCee/HInvisible.git HInvisible
cd HInvisible
```

or via https:
```shell
git clone --recurse-submodules https://github.com/BNL-FCCee/HInvisible.git HInvisible
cd HInvisible
```



## Initial Setup
For the initial setup of the FCCAnalyses do:

```shell
cd FCCAnalyses

source ./setup.sh
mkdir build install
cd build
cmake .. -DCMAKE_INSTALL_PREFIX=../install
time make install
cd ../..
```

# Regular Setup

Then on every return do 
```shell
source FCCAnalyses/setup.sh
```

## Run the selection
The analysis proceeds in multiple steps. Execute these steps in squence


```shell
fccanalysis run analysis_HInv_stage1.py
fccanalysis final analysis_HInv_final.py
```