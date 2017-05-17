# iTesla 7-Bus Model: PSS/E Models for the initialization of OpenIPSL Modelica Model

This repository includes a PSS/E implementation of the iTesla 7-Bus model in PSS/E, and other auxiliary files to be able to use this model together with it's implementation in ([OpenIPSL](https://github.com/SmarTS-Lab/OpenIPSL)).

The iTesla 7-Bus model is a synthetic network used for testing the iTesla Power System Tool (iPST), and its original implementation was done within the iPST, where the dynamic models are defined in both iPSL/Modelica and Eurostag model definitions.

In order to test some of the workflows within the iPST, specially those related to static and dynamic stability classification indexes from time-domain simulations; we defeloped both a PSS/E implementation (available in this repository), which can be used to provide different power flow solutions to our OpenIPSL Modelica model implementation (see [here](https://github.com/SmarTS-Lab/OpenIPSL/tree/master/ApplicationExamples/SevenBus)).

The model is substantially different from the one defined within iPST/Eurostag, making many significant improvements in terms of power system modeling principles.

This repository provides:
 - The PSS/E implementation (aka the ['base case'](https://github.com/SmarTS-Lab/7Bus/tree/master/PSSE))
 - A set of snapshots (solved power flow archives), to be used with [RawtoRecord](https://github.com/SmarTS-Lab/Raw2Record) to provide multiple operating points to simulate the [OpenIPSL 7-Bus Model Implementation](https://github.com/SmarTS-Lab/OpenIPSL/tree/master/ApplicationExamples/SevenBus).
 - A Python script that helps to create new snapshots by running PSS/E (Note: requires a PSS/E license), for 24 hrs by providing the loading/generation profile (see [here](https://github.com/SmarTS-Lab/7Bus/tree/master/PSSE/Sevenbus-snapshots)).
