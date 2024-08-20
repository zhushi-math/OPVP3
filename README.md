Feasible Region Self-Limitation: A Novel Approach to Policy Optimization in Offline Reinforcement Learning
==================================
This project provides the open source implementation of the POFRS method introduced in the paper: "Feasible Region Self-Limitation: A Novel Approach to Policy Optimization in Offline Reinforcement Learning" . 

## Installation
#### 1. System requirements
- Tested in Ubuntu 20.04, should be fine with Ubuntu 18.04
- I would recommend to use [Anaconda3](https://docs.anaconda.com/anaconda/install/) for python env management

#### 2. System-wise dependencies installation
Since we will use `mujoco` and `mujocu_py` for the `gym` environment experiments, so some dependencies should be installed with `sudo` permissions. To install the dependencies, run
D4RL can be installed by cloning the repository as follows:
```
git clone https://github.com/Farama-Foundation/d4rl.git
cd d4rl
pip install -e .
```
And enter the sudo password to finish dependencies installation.

#### 3. Anaconda Python env setup
Back to the repo root folder, **activate a python 3.7 virtual anaconda env**, and then run
```
conda create -n POFRS python=3.7
conda activate POFRS
cd ../.. && bash install_all.sh
```
It will install the modified `gym` and this repo's python package dependencies that are listed in `requirement.txt`.  Note that we modify the original environment repos to accelerate the training process, so not using our provided envs may require additional hyper-parameters fine-tuning.

#### 4. Install pytorch
To install the pytroch, run 
```
pip install torch==1.8.0+cu111 torchvision==0.9.0+cu111 torchaudio==0.8.0 -f https://download.pytorch.org/whl/torch_stable.html
```
You can also refer to this tutorial [tutorial here](https://pytorch.org/get-started/locally/) for installation on your platform.

## Training
### How to run a single experiment
Before running, you need to download the dataset. 

Simply run
```
python script/POFRS_main.py -wan
```

### Check the result of the experiment
You can log in to Wandb to view the training results.
