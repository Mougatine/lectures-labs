Either use Anaconda or Pip.

Do only one, then go to the final section "Installation".


# Anaconda

Download the Anaconda distribution for your Operating System
(Windows, macOS or Linux):

   - https://www.anaconda.com/products/individual (~500 MB)
   - Choose **Python 3.7**
   - Choose "64-bit installer"

Follow the instructions of the Anaconda page to install anaconda
on your laptop.

Create a conda env in the repo directory and activate it:

    conda create --name dlclass
    conda activate dlclass


In a console check the installation location of the conda command in
your PATH:

    conda info

Read the output of that command to verify that your conda command is
associated with Python 3.7.

Check that the pip command in your PATH is the one installed by conda:

    pip show pip

and check that it matches:

    python3 -m pip show pip

In particular, look at the "Location:" line of pip is a subfolder
of the "environment root:" line from "conda info".

# Pip

Install python>=3.7 and pip on your machine.

Create a virtual env:

    python3 -m venv dlclass


# Installation

Install requirements:

    pip install -r requirements.txt

Check that you can import tensorflow with the python from anaconda:

    python3 -c "import tensorflow as tf; print(tf.__version__)"
    2.2.0

Note that tensorflow 2.0.0 should also work.

If you have several installations of Python on your system (virtualenv, conda
environments...), it can be confusing to select the correct Python environment
from the jupyter interface. You can name this environment for instance
"dlclass" and reference it as a Jupyter kernel:

    python3 -m ipykernel install --user --name dlclass --display-name dlclass
