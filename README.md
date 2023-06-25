# CSE-3000-replication-package
Replication package of my Bachelor Thesis paper titled "Augmenting Pareto Corner Search Evolutionary Algorithm for Automatic Test Case Generation" available at TU Delft Research Repository.

The aforementioned paper introduces adapts Pareto Corner Search Evolutionary Algorithm (PCSEA) for test case generation, and builds on top of it with heuristics from state-of-the-art algorithm DynaMOSA. This repository contains all the necessary tools needed to replicate the experiment, including a python script to visualize the results.


## Configuration
To select the configuration of the experiment and select the related parameters, the [.syntest.json](syntest-javascript-benchmark/.syntest.json) file should be accessed:
- `target-root-directory` specifies the benchmark directory of the files, the available directories can be found [here](syntest-javascript-benchmark/.syntest-projects.json)
- `include` specifies the files for which the algorithm should try to generate tests, the available files can be found [here](syntest-javascript-benchmark/.syntest-projects.json) 
- `preset` specifies the algorithm, valid options are `NSGAII`, `MOSA`, `DynaMOSA`, `MOSAPCSEA`, and `DynaMOSAPCSEA`.
- `total-time`: represents the maximum search time of the algorithm.

## Running the experiment

In order to run the experiment, please follow the instructions provided in javascript-benchmark directory.


## Plotting results

The provided `extract.py` file contains utility functions for plotting the results obtained from running the experiments. This script requires csv files for results and statistics, and could be used for:

- Generating a graph of average coverages of different algorithms over time for a given benchmark file.

- Generating a branch coverage table containing the median branch coverages of all the algorithms for the benchmark files.

- Generating a statistics table from comparing two algorithms.

- Generating an overall results table contatining the average branch coverages and comparison statistics. This was used to generate the results table in the paper.