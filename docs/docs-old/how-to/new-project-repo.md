# Create New Project with Git

## Setup Local Environment

Create new project in Local by Flywheel:
* Set site name, local dev URL, and project directory
* Choose custom environment:
  * PHP Version >= 7.0.0
  * Web server = Apache
  * MySQL >= 5.5

## Create Git Repo

Create a new repository in Unity's GitHub organization: https://github.com/organizations/unitymakesus/repositories/new (**Do not initialize it with a README, license, or .gitignore files.**)

## Setup Starter Template

In this step, you'll be cloning the starter-template repo without commit history. Then you'll move the starter-template files into the new project directory and initialize a new local repo for the new project.

So in Terminal, go to the `app/public/` directory for the new project you created in Local by Flywheel and then do the following:

````shell
# @ app/public/
$ git clone --depth 1 https://github.com/unitymakesus/starter-template.git
$ rm -rf starter-template/.git
$ cp -r starter-template/. .
$ rm -rf starter-template
$ git init
$ git add .
$ git commit -m "Initial commit"
$ git remote add origin [replace with remote repository URL]
$ git remote -v
$ git push -u origin master
````
