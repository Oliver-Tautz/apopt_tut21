# How to install python and jupyter on Ubuntu

## Install python

python3.8 is installed with ubuntu. Test if it is installed this way:

* open bash (command line)
    * ctrl+alt+t on ubuntu
    * or search for 'bash', 'cmd' or similar
* type `python3`

If it prints somethins similar to `Python 3.8.10 (default [...] >>>` it is already installed. If it shoul be missing type `sudo apt install python3` and test again.

We still need to install a package manager for python. To install pip type `sudo apt install python3-pip` and say `Y` when prompted


## Install jupyter

Type `sudo apt install jupyter-notebook`. Thats it. You can now start with `jupyter-notebook`.

## Installing packages

If you need to install a package such as *scipy* or *matplotlib* you can just type `python3 -m pip install $PACKAGENAME` and pip will install it 

## Use virtual environments

It can be useful to make use of *virtualenvs*. After installing you have a main python3 environment with its installed packages. If you want to install new packages for everything you do in that environment it can become cluttered. To avoid that you can use virtual environments. To generate a virtualenv follow these steps:

* type `python3 -m venv $ENV_FOLDER`. The folder of the environment can get big if you install lots of packages, so choose a sensible location for it
* type `source $ENV_FOLDER/bin/activate` to *activate* the new environment. Now you can install packages just like before, but they will only be available in the new environment

If you want to use the new environment in jupyter do this:

* you need to be in the environment, so if you are not type `source $ENV_FOLDER/bin/activate` like before
* type `ipython kernel install --user --name=$ENVNAME`. This will make the environment available in jupyter under the $ENVNAME

Now you can select it via Kernel -> Change kernel -> $ENVNAME


