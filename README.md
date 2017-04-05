#alp_analysis

## FUNDAMENTAL IDEA
... ciaooooo

## CODE STRUCTURE
...alp_analysis inherits classes from ALPHA framework.
The latter has to be installed before.
Everything inside a CMSSW environment. ...

## TO DEBUG:
Look at issue on GitHub and use this chat for discuss about the code:
[![Join the chat at https://gitter.im/cms-hh-pd/alp_analysis](https://badges.gitter.im/cms-hh-pd/alp_analysis.svg)](https://gitter.im/cms-hh-pd/alp_analysis?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

## TO INSTALL:
- Prerequisites
git account and git environment set

- Git instructions
    0. In your working area, first set up the CMSSW release:
        ```
        cmsrel CMSSW_8_0_12

        cd CMSSW_8_0_12/src/

        cmsenv

        git cms-init
        ```
    1. Install packages needed by ALPHA:
        see README from ALPHA repo [https://github.com/cms-hh-pd/ALPHA#alpha]

    2. Clone ALPHA and setup it:
        see README from ALPHA repo [https://github.com/cms-hh-pd/ALPHA#alpha]
        NOTE: clone it from cms-hh-pd repo:
            ```bash
            git clone git@github.com:cms-hh-pd/ALPHA.git
            ```
    3. Clone the alp_analysis git repository:
        ```bash

        cd $CMSSW_BASE/src/Analysis

        git clone git@github.com:cms-hh-pd/alp_analysis.git
        ```

## TO RUN:
Compile the code:
```bash
cd $CMSSW_BASE/src/
scram b -j 8
```
and run it:
```bash
cd $CMSSW_BASE/src/Analysis/alp_analysis
python scripts/Selector.py
```

If you do not have ALPHA compiled do: 

cd Analysis/alp_analysis/src/
root -l
> .L ../src/alp_objects.h++
