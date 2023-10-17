# cuda_conda
conda environment to interact with GPU in pytorch

## Code to install everyone on your own

```
conda create --name cuda_test python=3.8
conda activate cuda_test
conda install -c anaconda cudatoolkit -y
conda install pytorch-cuda=12.1 -c pytorch -c nvidia -y
conda install pytorch torchvision torchaudio -c pytorch -c nvidia -y
```

## install `environment.yml`

```
conda env create -f environment.yml
```

## To see if `pytorch` can access cuda

```{python}
import torch

torch.cuda.is_available()
#returns `True` if cuda is present and `False` if only CPU
```
