
Project Organization
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
    ├── presentations      <- Contains all powerpoint presentations in .pdf format
    ├── references         <- background information
    |  └── codestyle       <- Some code Code style standards
    |  └── leerdoelen      <- Learning goals per lesson, including pages to read and videos to watch
    │
    ├── reports            <- Generated analysis like PDF, docx, etc.


--------

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

`git clone https://github.com/Clein2312/Advanced_AI_Applications_WS24-25_MADS_HSRW.git`

## add your username and email to git
1. `git config --global user.name "Mona Lisa"`
2. `git config --global user.email "m.lisa@pisa.com"`

## install all dependencies
1. `cd MADS-MachineLearning-course/`
2. `rye sync`

## Watch the video.

Please watch the video to understand rye better.. [introduction video about rye](https://rye.astral.sh/guide/)
