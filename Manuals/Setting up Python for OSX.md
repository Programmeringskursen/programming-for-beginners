# Setting up Python for OSX using packages from python.org

* Start Safari, go to python.org. Click on "Downloads", then "Download Python 2.7.xx".

* When the download is finished, click on the Downloads icon bottom right, then click on the python-2.7.xx-macosx10.y.pkg. Follow the instructions.

* In Safari, go to pygame.org. Click on "create", then "download.shtml". Scroll down to the section "Macintosh". Select the first item (with py2.7 in the filename).

* When the download is finished, click on the Downloads icon bottom right, then click on the pygame-...-macos10.x.dmg file.

* A new window opens. Hold the Control key, and right-click?! on the package icon, then click on "Open". Follow the instructions.

* Start a Terminal and run:

	`pip install virtualenv`

# Setting up Python for OSX using Homebrew

* First you set up the Homebrew package manager. A package manager is a software that helps you install other software or "packages".

      `$ ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`

* Then we install a clean version of Python for us to program with, using "brew", that we just installed. This will also include "pip", another package manager, that helps us installing "libraries" for python.
 
      `$ brew install python`

* We finish by installing virtualenv for Python using pip.

      `$ pip install virtualenv`
