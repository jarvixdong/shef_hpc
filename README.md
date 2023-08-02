# shef_hpc
This document includes some basic guidance for the use of hpc in the University of Sheffield.
https://docs.hpc.shef.ac.uk/en/latest/hpc/index.html

## 1. install anaconda
a) Using the following command to download miniconda
```
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
```

b) Using the following command to install miniconda. Please remember to answer yes to allow conda init, so that everytime you login the hpc, the conda will start automatic.
```
bash Miniconda3-latest-Linux-x86_64.sh
```

c) create your personalised environment for python

```
conda create -n [name] 
```
d) activate your environment 
```
conda activate [name]
```

## 2. How to use GPU in hpc
a) Using the following command to apply a GPU.
```
srun --partition=gpu --qos=gpu --nodes=1 --gpus-per-node=1 --mem=34G --pty bash
```
b) after be offered one gpu, you need to activate your python environment again to run your python scripts (using the command in section 1 part d).

c) run your python script, using "python + path". You can see the following example. 
```
python test.py
```
d) some basic command of Linux.
```
ls                     \\View the files in the current directory
cd + [directory path]  \\entry the directory
```
