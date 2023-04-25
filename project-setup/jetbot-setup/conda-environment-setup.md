# Conda Environment Setup

The team used conda environment for running python files. To set up the conda environment on jetson nano, we need to use miniconda for AArch64 architecture. By the time the team was setting up the environment, conda did not officially support the architecture, and the substitute was to use  [archiconda](https://github.com/yqlbu/archiconda3). Now conda has official support, follow the instruction [here](https://docs.conda.io/en/latest/miniconda.html) to install it.

In the jupyter notebook, open a new terminal and type following

```
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-aarch64.sh

bash Miniconda3-latest-Linux-aarch64.sh
```

Follow the prompts to complete the installation. Then type in&#x20;

```
source ~/.bashrc
```

to update your PATH.

Check "conda --version" for successful installation.
