# Version management

Make a directory have history (make it a *repository*):

    git init

Save some changes

    git add basket.py
    git commit -m "A descriptive comment"

List previous changes (press *q* to get out)

    git log
    
Connect your repository with one on github.com:

    git remote add origin git@github.com:Programmeringskursen/MyProject.git

By default the name origin is used, but you can register more remote repositories with other names, and then use them by specifying the name explicitly.

Send all your changes to github:

    git push origin master

Get all new changes from github:

    git pull origin master
