# Setting up Python for OSX

* First you set up the Homebrew package manager. A package manager is a software that helps you install other software or "packages".

      `$ ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`

* Then we install a clean version of Python for us to program with, using "brew", that we just installed. This will also include "pip", another package manager, that helps us installing "libraries" for python.
 
      `$ brew install python`

* We finish by installing virtualenv for Python using pip.

      `$ pip install virtualenv`
