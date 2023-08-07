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
