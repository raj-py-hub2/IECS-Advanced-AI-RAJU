
## Project Organization
------------

    ├── README.md          <- This file
    ├── .gitignore         <- Stuff not to add to git
    ├── pyproject.toml     <- Human readable file. This specifies the libraries I installed to
    |                         let the code run, and their versions.
    ├── data
    │   ├── external       <- Data from third party sources.
    │   ├── processed      <- The processed datasets
    │   └── raw            <- The original, raw data
    │
    ├── models             <- Trained models
    │
    ├── notebooks          <- Jupyter notebooks. Naming convention is xx_name_of_module.ipynb where
    │                         xx is the number of the lesson
    ├── presentations      <- Contains all powerpoint presentations
    ├── references         <- background information
    |  └── codestyle       <- Some code Code style standards
    |  └── leerdoelen      <- Learning goals per lesson, including pages to read and videos to watch
    │
    ├── reports            <- Generated analysis like PDF, docx, etc.


--------

## Introduction to Jupyter Notebooks

The `notebooks` folder contains lessons divided into Jupyter notebooks. Each notebook follows the naming convention `xx_name_of_module.ipynb` where `xx` represents the lesson number. Below is an overview of each lesson and its contents.

#### 0. Baseline (`0-baseline/`)
This folder contains notebooks introducing basic Python operations, including:
- Fundamental Python concepts
- Array manipulation and vectorization
- Classes and functions

#### 1. PyTorch Introduction (`1_pytorch_intro/`)
This module introduces PyTorch tensors, data handling, and training basic neural networks.

- `01_tensors.ipynb`: Introduction to Torch tensors, including manipulation and broadcasting.
- `02_datagenerators.ipynb` & `03_dataloaders.ipynb`: Implementation of custom dataloaders and loading datasets using `mads_dataset` for machine learning tasks.
- `04_neuralnets.ipynb`: Introduction to building a simple linear neural network.
- `05_image_classification.ipynb`: Training a neural network for image classification using the Fashion MNIST dataset.
- `06_exercise.ipynb`: Exercise solution that explores changes in different parameters and their effects.

#### 2. Convolutions (`2_convolutions/`)
This module focuses on handling image datasets and training convolutional neural networks (CNNs).

- Introduction to CNN model training on image datasets.
- `03_mlflow.ipynb`: Introduction to MLFlow for tracking the machine learning lifecycle.
- `04_exercises.ipynb`: Exercise solutions, including a configurable CNN model for Fashion MNIST dataset.

#### 3. Recurrent Networks (`3_recurrent_networks/`)
This module covers time-series data and different types of recurrent neural networks (RNNs).

- Understanding the windowing technique for time-series data.
- Introduction to Simple RNNs, GRUs, and LSTMs, along with their respective use cases.

#### 4. Tuning Networks (`4_tuning_networks/`)
This module explores different hyperparameter tuning strategies and transfer learning techniques.

- `02_hypertuner.ipynb`: Implementation of hyperparameter tuning methods such as Grid Search, Bayesian Optimization, and Hyperopt.
- `04_transfer_learning_with_resnet.ipynb` and `05_minimal_transfer_learning.ipynb`: Introduction to transfer learning techniques for leveraging pre-trained models.
- `Hypertuning_Exercise.ipynb`: Exercise solution involving two models to perform parameter search for maximizing accuracy.

#### 5. Attention Mechanism (`5_attention/`)
This module introduces the attention mechanism and its role in model training.

- Understanding how attention mechanisms help in faster model convergence.
- `06_metric.ipynb`: Importance of selecting the right evaluation metric, especially in cases of class imbalance.


## Dependencies 
For this project you will need some dependencies.
The project uses python 3.10, and dependencies are defined within the `pyproject.toml` file. You will also find `requirements.lock` files, but they are generated for a Mac so they will miss CUDA specific dependencies.

The management of datasets and the training-loop code are separated. You will find them as dependencies in the project:
- https://github.com/raoulg/mads_datasets
- https://github.com/raoulg/mltrainer

Both of these will be used a lot in the notebooks; by separating them it is easier for students to use the code in your own repositories.
In addition to that, you can consider the packages as "extra material"; the way the packages are set up is something you can study if you are already more experienced in programming.

## Installing python with Rye

### Installation for Linux [Recommended]
1. Watch the [introduction video about rye](https://rye.astral.sh/guide/)
2. You skipped the video, right? Now go back to 1. and actually watch it. I'll wait.
3. Open your Terminal
4. Install [rye](https://rye.astral.sh/) with `curl -sSf https://rye.astral.sh/get | bash`

run through the installer like this:
- Platform linux: yes
- Preferred package installer: uv
- Run a Python installed and managed by Rye
- Which version of python should be used as default: 3.10
- Should the installer add Rye to PATH via .profile? : y
- Run in the cli: `source "$HOME/.rye/env"`

### Installation for Mac
1. Watch the [introduction video about rye](https://rye.astral.sh/guide/)
2. You skipped the video, right? Now go back to 1. and actually watch it. I'll wait.
3. Open your Terminal
4. Install [rye](https://rye.astral.sh/) with `curl -sSf https://rye.astral.sh/get | bash`

Run through the installer like this:
- Platform macos: yes
- Run the old default Python (provided by your OS, pyenv, etc.)
- Should the installer add Rye to PATH via .profile? : y

5. Run in the terminal: `source "$HOME/.rye/env"`
6. Install python 3.10 as follow: `rye fetch 3.10`


### Installation for Windows

1. Watch the [introduction video about rye](https://rye.astral.sh/guide/)
2. You skipped the video, right? Now go back to 1. and actually watch it. I'll wait.
3. Activate "Developer Mode" on Windows. Follow the instruction of **Windows Developer Mode** [See this page](https://rye.astral.sh/guide/faq/#windows-developer-mode)
4. Download and install the latest release of [rye](https://rye.astral.sh/) 


## add the git repo
run in the cli:

```bash
git clone https://github.com/raj-py-hub2/IECS-Advanced-AI-RAJU
```

## add your username and email to git
```bash
git config --global user.name "Mona Lisa"
git config --global user.email "m.lisa@pisa.com"
```

## install all dependencies (rye will install all dependencies)
```bash
cd IECS-Advanced-AI-RAJU
rye sync
```

## Watch the video.

Please watch the video to understand rye better.. [introduction video about rye](https://rye.astral.sh/guide/)
