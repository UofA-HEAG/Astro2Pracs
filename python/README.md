# Python

Python is a programming language that is very intuitive and easy to learn. It also offers a variety of packages for basically everything - plotting, image processing, statistics, machine learning and much more. This means that you do not have to implement these methods yourself, but can use them directly.

It is strongly recommended to use python via anaconda. Anaconda is both a package and an environment manager. 
As a *package manager*, it allows an easy installation of packages. For a specific package, it installs all further necessary packages with the correct version.
As an *environment manager*, it allows you to have multiple environments at the same time. An environment is a combination of specific packages of specific versions. Depending on a project, a specific combination of packages and versions might be necessary. Often, different combinations are necessary for different projects. An environment manager helps to setup these environments and to organise them.

For the installation of python via anaconda, see `installation.md`.


## Jupyter Notebooks

The examples in this folder are so-called *ipython notebooks* (.ipynb). They can be viewed here, but you can also download them and use them intereactively.


### Start a Notebook

* Activate your conda environment (`conda activate pracs`).
* Start an existing notebook via `jupyter notebook SomeNotebook.ipynb`
* Or create a new notebook: `juypter notebook` and then *File->New->Notebook* and select *python 3* or *New->Python 3*.

### Execute Code

Just type `Shift+Enter` to execute a cell.

### Help

To get information on an object, method, ... (within a notebook): Type the name followed by a question mark and then Enter. For example: `numpy.percentile?`