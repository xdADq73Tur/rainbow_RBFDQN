### Rainbow RBFDQN

Run flags: 

`--seed <seed_num>`

`--experiment_name <exp_name>` 
Usually use something like `results/experiment1`, to create a new folder in the results root directory. 

`--run_title <run_title>`
Creates a sub-folder under the <exp_name> directory and stores all the logs, hyperparameters, and meta logger information here. 

`--hyper_parameter_name <task>`
The code of the task you want to run. All of these can be found in the rbf_hyper_parameters folder. For example, 00 is Pendulum. 

`--distributional <True / False> `
If you want to use quantile distributional RBF-DQN 

`--double <True / False>` 
If you want to use double DQN

`--per <True / False>` 
Use priority experience replay

`--dueling <True / False>` 
If you want to use a dueling architecture.

`--nstep <step_size>`
If you want to use multi step returns, by default 1 is 1-step updates

`--noisy_layers <True / False>`
If you want noisy linear layers to be used in place of linear layers, and use parameter noise for the exploration strategy

### Example Run Commands
`python experiments/experiment.py --hyper_parameter_name 00 --seed 0 --experiment_name "./results/<TASK_NAME>" --run_title "<VARIATION>" --double True --per True --distributional True`