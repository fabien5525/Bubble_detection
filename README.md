---
title: Bubble detection
author: fabien5525
date: 11/03/2023
os: Windows 10
---

# How to install

## use venv

### install venv
```sh
pip install venv
```

### create it and activate it
```sh
virtualenv -p 'path\to\your\python\python.exe' venv
.\venv\Scripts\activate
```

### install dependencies
```sh
pip install -r requirements.txt
```

### GPU ?

If you want to use your GPU to speed-up your training,
you will need a cuda compatible GPU.

In my case i'm using a RTX 2070 SUPER with CUDA 11.6

To check your CUDA version
```sh
nvcc -V
```

See nividia doc : https://developer.nvidia.com/cuda-11-6-0-download-archive

# Verify if you have GPU avalaible:

In a python shell:
```py
import torch
print(torch.cuda.is_available())
```

If you have problems you can check this : https://stackoverflow.com/a/74618171/17388412
("nvidia-smi -mig 0" worked for me)