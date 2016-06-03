# hyperopt-tutorial
A tutorial on the basics of using hyperopt. Includes notebook examples for both [hyperopt](https://github.com/hyperopt/hyperopt) and [hyperopt-sklearn](https://github.com/hyperopt/hyperopt-sklearn).

## Installation

To run the notebooks in this repo you will need up-to-date versions of many Python packages installed from GitHub. I recommended setting up a virtual environment to try them out in case these versions are not the ones you use normally. To do this you will need virtualenv installed, which you can get by running:

`sudo apt-get install virtualenv`

To create the virtual environment, run the command `virtualenv <name>`. This will create a new folder with your chosen name from which you can activate the virtual environment (for the particular terminal you have open). While active, anything you pip install will be installed in this environment.

Instructions for installing everything you need to a virtual environment are shown below. It is also possible to clone packages from git and then install them after instead.

```
cd ~/
virtualenv hptut
cd hptut
. bin/activate
pip install jupyter
pip install matplotlib
pip install numpy
pip install https://github.com/hyperopt/hyperopt/archive/master.zip
pip install networkx
pip install scipy
pip install pyll
pip install seaborn
pip install pandas
pip install https://github.com/scikit-learn/scikit-learn/archive/master.zip
pip install https://github.com/bjkomer/hyperopt-sklearn/archive/revival.zip

```

You will need the latest version of hyperopt from GitHub for compatibility with hyperopt-sklearn. You will also need the latest version of scikit-learn from GitHub in order to use the MLPClassifier in the MNIST example. There have been some API changes to scikit-learn since hyperopt-sklearn came out which can break a few things. A new 'revival' branch has been created where fixes are going to go for keeping the project more up to date. You need to use this branch for the RBF kernel of a SVM to work (and possibly other things as they get noticed and fixed).
