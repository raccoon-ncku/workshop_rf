# Workshop: Robotic Fundamentals

## Computer Setup
### System Requirement
- Windows 10 Pro or above / Mac OS Sierra 10.12 or above

### Applications
Please download and install the following applications:
* [miniconda 3](https://docs.conda.io/en/latest/miniconda.html)
* [Docker Desktop](https://www.docker.com/products/docker-desktop) 
* [Rhino 6 or 7](https://www.rhino3d.com/download)
* [Visual Studio Code](https://code.visualstudio.com/)

for Visual Studio Code, please install the following extensions:
* ms-python.python
* ms-azuretools.vscode-docker

### Large Files
Please download the following files before the workshop:
- [Workshop Files](https://drive.google.com/drive/folders/1159IfPik13sScniSJwjBX9LQlO-e-gGp?usp=sharing)


## Installing Python and COMPAS
We use `conda` to make sure we have clean, isolated environment for Python and dependencies.
Open `Anaconda Powershell Prompt (miniconda3)` (Windows), or `Powershell` (Windows),  or `Terminal` (macOS).

First, we have to add `conda-forge` as a channel for `conda` to fetch packages. This only needs to be done once on every computer.
```
conda config --add channels conda-forge
```
If the command return nothing, it means the channel has been added successfully.

Next, create a new environment for this course:
```
conda create -n robot python=3.11
```
When prompted, type `y` to proceed.
![conda_create_env](/Assets/imgs/conda_create_prompt.png)

When finished, activate the environment, so that we could install packages into it.
```
conda activate robot
```

When an environment is activated, the name of the environment will be shown in front of the command prompt. In this case, it is `(robot)`. Continue to install compas and other modules:
```
conda install compas compas_fab compas_cgal compas_view2
```

> [!IMPORTANT]  
> The commands above might take up to 20-30 minutes to finish.

These step might take a while. You might experience a warning like this. It is because the some module we use is not yet a stable version. When prompted, type `y` to proceed.

### Initialize Developing Environment in Rhino
The developing environment in Rhino need to be initialized before installing Python modules. This only needs to be done once on every computer. To do that, open Rhino and navigate to `Tools > PythonScript > Edit...`. Once the script editor shows up, the environment is successfully initialized, and Rhino could be closed.

Finally, depending on your installed Rhino version, execute one of the flollowing:

#### Rhino 6
```sh
python -m compas_rhino.install -v 6.0 -c
```

#### Rhino 7
```sh
python -m compas_rhino.install -v 7.0 -c
```

## Slides
- [Module 1](https://app.rccn.dev/slidev/KUKA)
- [Module 2](https://link.rccn.dev/wsrf)