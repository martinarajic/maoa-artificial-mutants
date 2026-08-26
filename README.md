
This repository contains the files necessary to reproduce the computational results reported in the manuscript:

Single-Residue Rational Design Fails to Outperform the Wild-Type MAO-A Enzyme: Artificial Mutants Reveal the Limits of Local Electrostatic Optimization <br>
Martina Rajić, Outi Lampela, Robert Vianello Janez Mavri, Jernej Stare


#### REPOSITORY STRUCTURE

The input files are organized into three main folders:


#### QM

The QM folder contains Gaussian input files used for quantum-mechanical calculations.

For each investigated system, Gaussian inputs are provided for:

R – reactant state
TS – transition state

The provided .com files correspond to the ON state, meaning that the environmental point charges are included in the Gaussian input.

The corresponding OFF calculation does not require a separate structural input. To prepare the OFF state, use the same .com file and simply remove the point-charge section from the Gaussian input.


#### MD

The MD folder contains all input files required to run the molecular dynamics simulations in Amber.

Due to a 48-hour computational time limit on our cluster, the MD production simulation was divided into three consecutive input files. The second MD run starts from the output/restart of the first run, and the third starts from the output/restart of the second run. Therefore, these should not be treated as three independent MD simulations, but as three consecutive parts of the same simulation trajectory.

#### EVB

The EVB folder contains all input files required to run the Empirical Valence Bond (EVB) simulations.


!!For the MD and EVB simulations, the provided input files are based on the WT system and may therefore require modification such as naming or index numbers.Additionally, for the purpose of preparing and organizing this repository, some files were renamed to ensure a clearer and more consistent folder and file structure.
