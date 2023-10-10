# FNS_AuditorOpinion
Accompanying code for FNS2023 submission, please do not redistribute.


## Installation
The requirements for this project can be installed by running:

conda env create -f environment.yml

Python version used: Python 3.9.16


## Details
The contents of the repo are the following:

- *frozen_splits*: Folder with the train/val/test opinions data.
- *logs*: Folder to save log files.
- *results*: Folder to save resuts.
- *settings*: Folder with settings configurations.
- *enviroment.yml*: Conda enviroment to create.
- *fine_tune_lm.py*: Script used for fine-tuning the LM. The script cannot be run as is, because the labels are missing from the data here. The whole process is the same though.
- *fine_tune_rf.py*: Script used for hyper-parameter tuning on the *tf-idf + RF* model. The script cannot be run as is, because the labels are missing from the data here. The whole process is the same though.
- *early_stopper.py*: Module for the early stopping functionality.
- *focal_loss.py*: Module implementing the weighted focal loss as used in the results Section 4.3.
- *load_data.py*: Module implementing the loading/splitting and preprocessing of the data.
- *model.py*: Module containing the Langugage Model + Classifier layer, along with routines for training and evaluation.
- *utils.py*: Helper functions.

## Run
One would run either:

```cmd
python fine_tune_lm.py ./settings/wanted_settings_file.json
```

to train and evaluate a LM with the parameters as defined in the setting file or

```cmd
python fine_tune_rf.py 
```

to do a hyper-parameter tuning on the *tf-idf + RF* pipeline used as a baseline.


## Data
Currently, the above would result in an error, as **the data shared here are not annotated with the AuditAnalytic labels used in our analysis due to property rights**. For a subset of the labeled dataset please contact the authors after publication. Nonetheless, the **unlabeled frozen splits containing the auditor reports**, with other metadata as well, **are currently available and provided in the data folder**.


## Notes
The repository will be updated regulary and the weights of the pre-trained models will be uploaded soon as well.




