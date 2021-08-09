# Installation Instructions


## Installation of Python via Anaconda

#### MacOS
-	The Anaconda Installers can be found at the bottom of this page: https://www.anaconda.com/products/individual
-	Download the Graphical Installer for Python 3.8 under MacOS
-	Follow the instructions

#### Windows
-	The Anaconda Installers can be found at the bottom of this page: https://www.anaconda.com/products/individual
-	Download the Graphical Installer for Python 3.8 under Windows
-	Follow the instructions

Note: Here, 'Terminal' refers to the 'Anaconda Prompt'. 

#### Linux
-	The Anaconda Installers can be found at the bottom of this page: https://www.anaconda.com/products/individual
-	Download the Installer for Python 3.8 under Linux for your system (probably x86)
-	In terminal:

```
bash Anaconda3-*-Linux-*.sh
<Enter>
yes
~/.local/anaconda3
yes
```
-	Restart terminal


## Test Your Installation

In the terminal, try the following commands:

* `python` (Interactive python  session should start up and the prompt is specifying your python version. Exit with `exit()`)
* `ipython` (Interactive ipython  session should start up and the prompt is specifying your python version. Exit with `exit()`)
* jupyter notebook


## Create an Environment for these Pracs

-	Copy the file `environment.yml` to your computer. This file specifies all packages to be installed and the name of the environment.
-	Go to that folder and in terminal:
```
conda env create -f environment.yml 
```
-	This will create an environment called 'pracs'

Every time you want to use it:
```
conda activate pracs 
```
