# Setting up Python for OSX using Homebrew

* First you set up the Homebrew package manager. A package manager is a software that helps you install other software or "packages".

      `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`

* Then we install a clean version of Python for us to program with, using "brew", that we just installed. This will also include "pip", another package manager, that helps us install "libraries" for python.
 
      `$ brew install python`

* We finish by installing ipython, a nicer python prompt:

      `$ pip install ipython`
