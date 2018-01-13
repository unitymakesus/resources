# Contribute to Unity WP Project

## Setup Local Environment

Create new project in Local by Flywheel:
* Set site name, local dev URL, and project directory
* Choose custom environment:
  * PHP Version >= 7.0.0
  * Web server = Apache
  * MySQL >= 5.5

## Clone Git Repo

1. In this step you will find and clone the repository URL in Unity's GitHub organization: https://github.com/organizations/unitymakesus/.

So in Terminal, go to the app/public/ directory for the new project you created in Local by Flywheel and then do the following:

```shell
# @ app/public/
$ git clone https://github.com/unitymakesus/[PROJECT-NAME].git
$ cp -r [PROJECT-NAME]/. .
$ rm -rf [PROJECT-NAME]
```

## Set up Theme Dependencies

Make sure all dependencies have been installed:

* [Composer](https://getcomposer.org/download/)
* [Node.js](http://nodejs.org/) >= 6.9.x
* [Yarn](https://yarnpkg.com/en/docs/install)

Install theme dependencies using Composer and Yarn from the theme's directory (replace `your-theme-name` below with the name of the theme):

```shell
# @ app/public/wp-content/themes/your-theme-name/
$ composer install
$ yarn
```

