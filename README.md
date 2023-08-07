# Data for F-VQE Paper
This repository contains the data generated for the project, divided in three sections with the two problems considered: Max cut and ATSP. The directory is structured in the following way:
```
project
│   README.md
└───simulations
│   └───maxcut
│   |   │   data_maxcut_fvqe.pkl
│   |   │   data_maxcut_classical.pkl
│   |   │   data_maxcut_sequential.pkl
│   |   │   data_maxcut_annealing.pkl
│   |   └───problems
|   |   |   |   *.txt
│   └───atsp
│       │   data_atsp_fvqe.pkl
│       │   data_atsp_classical.pkl
│       │   data_atsp_sequential.pkl
│       │   data_atsp_annealing.pkl
│       └───problems
|       |   |   *.pkl
└───gradients
│   └───maxcut
|   |   |   exact_grads_*.npy
|   |   |   exact_grads_vqe_*.npy
│   └───atsp
|       |   exact_grads_*.npy
|       |   exact_grads_vqe_*.npy
└───ibmq
    └───maxcut
    |   └───problems
    |   |   |   *.txt
    |   └───results1
    |   |   └───exp_folder
    |   |   |   |   input.{txt,pkl}
    |   |   |   |   output.{txt,pkl}
    |   |   |   |   summary_runs.{txt,pkl}
    |   |   |   |   best_samples.npy
    |   └───results2
    |   └───results3
    |   └───sequential
    |   |   |   *.npy
    └───atsp
        └───problems
        |   |   *.pkl
        └───results1
        └───results2
        └───results3
        └───sequential
            |   *.npy
```
Let us now describe the information contained in each file:
* ```data_{maxcut,atsp}_{fvqe,classical,sequ7ential,annealing}.pkl```: A dictionary with a dictionary for each size. Contains a list of the evolution of the best sample, energy, app. rat. and number of shots per each problem, as well as an indicator if the ground state has been sampled.

* ```exact_grads_*.npy```: Array of exact gradients for all experiments of a given size.

* ```input.{txt,pkl}```: Contains the main input info of the experiment, such as the problem file, backend, number of shots, etc.

* ```output_files.{txt,pkl}```: Contains info of every step such as the evolution of best parameters, the times for both the quantum and classical part, gradient info, etc.

* ```summary_runs.{txt,pkl}```: Summary of each job sent to Qiskit Runtime..

* ```best_samples.npy```: Array with the evolution of the best sample, energy, approximation $ratio and number of shots.
