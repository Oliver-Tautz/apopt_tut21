# Install python and jupyter on windows

## Install python

To use python on windows install miniconda, not simple python!
Find it [here](https://docs.conda.io/en/latest/miniconda.html)

* Download Miniconda and run the .exe
* always click next/I agree/Install
* search for `Anaconda Prompt (miniconda3)` and run it
* type `python` in the cmd window
If it prints something similar to  

```
Python 3.9.5 (default, May 18 2021, 14:42:02) [MSC v.1916 64 bit (AMD64)] :: Anaconda, Inc. on win32
Type "help", "copyright", "credits" or "license" for more information.
```

this step is finished :)

## Install jupyter

We use the installed conda environment to install jupyter:
* type `conda install -c conda-forge jupyterlab notebook` into the conda prompt
* say `y` when asked to Proceed

Thats it :) Now type either `jupyter notebook` or `jupyter-lab` into the conda prompt. It should open a browser window and you can start using jupyter!

## install packages

You will need some packages such as sklearn, matplotlib, scipy etc. To install a package use `conda install $PACKAGE_NAME`, so e.g. `conda install scipy` in the conda environment
