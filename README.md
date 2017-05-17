# iTesla 7-Bus PSS/E Models
## Power flow and dynamic models of the iTesla 7-Bus for the initialization of the OpenIPSL Modelica Dynamic Model

## What's in here?
This repository provides:
 - The PSS/E implementation (aka the ['base case'](https://github.com/SmarTS-Lab/7Bus/tree/master/PSSE))
 - A set of snapshots (solved power flow archives), to be used with [RawtoRecord](https://github.com/SmarTS-Lab/Raw2Record) to provide multiple operating points to simulate the [OpenIPSL 7-Bus Model Implementation](https://github.com/SmarTS-Lab/OpenIPSL/tree/master/ApplicationExamples/SevenBus).
 - A Python script that helps to create new snapshots by running PSS/E (Note: requires a PSS/E license), for 24 hrs by providing the loading/generation profile (see [here](https://github.com/SmarTS-Lab/7Bus/tree/master/PSSE/Sevenbus-snapshots)).

## Why is this useful?
This repository includes a PSS/E implementation of the iTesla 7-Bus model in [PSS/E](https://en.wikipedia.org/wiki/Power_system_simulator_for_engineering), and other auxiliary files to be able to use this model together with it's implementation in ([OpenIPSL](https://github.com/SmarTS-Lab/OpenIPSL)).

The iTesla 7-Bus model is a synthetic network used for testing the [iTesla Power System Tool (iPST)](https://github.com/itesla/ipst), and its original implementation was done within the iPST, where the dynamic models are defined in both iPSL/Modelica and Eurostag model definitions.

In order to test some of the workflows within the iPST, specially those related to static and dynamic stability classification indexes from time-domain simulations (see [here](https://github.com/itesla/ipst/tree/e46b47547098915367f4fcfe96301d068b45b2ab/dynamic-indexes)); we developed both a PSS/E implementation (available in this repository), which can be used to obtain different power flow solutions to our OpenIPSL Modelica model implementation (see [here](https://github.com/SmarTS-Lab/OpenIPSL/tree/master/ApplicationExamples/SevenBus)).

This can allow to test the afromentioned [indexes](https://github.com/itesla/ipst/tree/e46b47547098915367f4fcfe96301d068b45b2ab/dynamic-indexes) using different simulation engines that comply with the Modelica language. The long term goal is to study how either simulation excecution should be defined or how indexes have to be adapted in order to use outputs from any simulation tool. 
A repository with the indexes in iPST is available in the iPST Github [link](https://github.com/itesla/ipst/tree/e46b47547098915367f4fcfe96301d068b45b2ab/dynamic-indexes), while a new version will be uploaded soon (link when new repo is available).

The model is not identical to the one defined within iPST/Eurostag and differences exist for dynamic simulations, but they are irrelevant if the user is not interested in Eurostag matching but in PSS/E matching (see simulation results [here](https://github.com/SmarTS-Lab/iTesla7BusModel_PSSE2Modelica/tree/master/PSSE/Dynamics/Measurements).

[[https://github.com/SmarTS-Lab/iTesla7BusModel_PSSE2Modelica/blob/master/PSSE/Dynamics/Measurements/gen/V_FSSV_Eurostag_Modelica_PSSE.png]]

# Developers
Venkata Satya Narasimham Arava ([Narasimhamarava](https://github.com/Narasimhamarava)), Tin Rabuzin ([tinrabuzin](https://github.com/tinrabuzin)), Luigi Vanfretti ([lvanfretti](https://github.com/lvanfretti))

# License
This Modelica package is free software and the use is completely at your own risk; it can be redistributed and/or modified under the terms of the GNU Public License version 3.

Copyright (C) 2017, Venkata Satya Narasimhan Arava, Tin Rabuzin, Luigi Vanfretti. 
