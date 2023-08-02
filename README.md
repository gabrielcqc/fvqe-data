# Data for F-VQE Paper
This repository contains the data generated for the project, divided in three sections with the two problems considered: MaxCut and ATSP. The directory is structured in the following way:
```
project
│   README.md
|
└───plots
│   |   noiseless_simulations.ipynb
│   |   hyperparams.ipynb
│   |   grads.ipynb
│   |   ibmq.ipynb
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
|   |   |   exact_grads.pkl
|   |   |   exact_grads_vqe_.pkl
│   └───atsp
|       |   exact_grads.pkl
|       |   exact_grads_vqe.pkl
└───ibmq
|    └───maxcut
|    |   └───problems
|    |   |   |   *.txt
|    |   |   |   *.npy
|    |   └───results{1,2,3}
|    |   |   └───exp_folder
|    |   |       |   input_clean.{txt,pkl}
|    |   |       |   output_clean.{txt,pkl}
|    |   |       |   summary_runs_clean.{txt,pkl}
|    |   |       |   best_samples.npy
|    |   └───sequential
|    |       |   *.npy
|    └───atsp
|        └───problems
|        |   |   *.pkl
|        |   |   *.npy
|        └───results{1,2,3}
|        └───sequential
|            |   *.npy
└───hyperparams
    └───maxcut
    |   |   cumul_probs_{fvqe,cl}_{1,2,3,4}.pkl
    └───atsp
        |   cumul_probs_{fvqe,cl}_{1,2,3,4}.pkl
```
Let us now describe the information contained in each file:
* ```data_{maxcut,atsp}_{fvqe,classical,sequ7ential,annealing}.pkl```: A dictionary with a dictionary for each size. Contains a list of the evolution of the best sample, energy, app. rat. and number of shots per each problem, as well as an indicator if the ground state has been sampled.

* ```exact_grads{_vqe}.pkl```: Dictionary of arrays of exact gradients for all experiments of a given size.

* ```input_clean.{txt,pkl}```: Contains the main input info of the experiment, such as the problem file, backend, number of shots, etc.

* ```output_files_clean.{txt,pkl}```: Contains info of every step such as the evolution of best parameters, the times for both the quantum and classical part, gradient info, etc.

* ```summary_runs_clean.{txt,pkl}```: Summary of each job sent to Qiskit Runtime.

* ```best_samples.npy```: Array with the evolution of the best sample, energy, approximation $ratio and number of shots.

* ```cumul_probs_{fvqe,cl}_{1,2,3,4}.pkl```: Array with the cumulative probabilities for each problem instance for different sizes using exact simulations and 4 sets of hyperparameters for both the F-VQE and the Classical Ansatz.

In ```plots``` we have notebooks showing how to read the data and generate the plots displayed on the manuscript.
