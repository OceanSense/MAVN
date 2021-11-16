#  Collaborative Visual Navigation
![CollaVN](CollaVN.png)


## Installation

The code is tested under the following environment:

- Ubuntu 16.04 LTS
- Python 3.6
- Pytorch 1.8.0
- CUDA 11.1
- GCC 7.3

### Install required package
```shell
conda install pytorch==1.8.0 torchvision==0.9.0 torchaudio==0.8.0 cudatoolkit=11.1 -c pytorch -c conda-forge

pip install scikit-image
```
### Install MAVN

```shell
git clone https://github.com/OceanSense/MAVN.git

cd MAVN

# if you didn't create the conda environment before:
conda create -y -n MAVN python=3.6
conda activate MAVN

pip install -e . 
```
### Note
If you have problem in openGL, please see [[Trouble Shooting]](http://svl.stanford.edu/igibson/docs/issues.html)

### Presample Datapoint
To make the comparison fair, we pre-generated some data points, which we used in our paper, please see dataset dir.
[Google Drive](https://drive.google.com/drive/folders/1fBDSfS9Mk0sBuPJyLNO-arc12aLqR6pT?usp=sharing)

```shell
cd MAVN
wget https://drive.google.com/drive/folders/1fBDSfS9Mk0sBuPJyLNO-arc12aLqR6pT?usp=sharing
```

## Run Demo
```shell
python demo.py -n1 --auto_gpu_config 1 --total_num_scenes 1 --task_config ./config/CommonGoal_two_locobot.yaml
```

## TODO:
Release CollaVN V2 and method code

## Acknowledgments

Our code is heavily based on [iGibson](https://github.com/StanfordVL/iGibson). Thanks iGibson Development Team for their awesome codebase.
