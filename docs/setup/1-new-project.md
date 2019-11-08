---
layout: default
published: true
weight: 1
---

# Creating a New Project
Use this workflow if you are starting a project from scratch and there is no repository or local site set up. If you need to work on a project that already has a Git repo, use the "existing project" step.

## Set Up Local Environment
Create a new project in Local by Flywheel:
* Site Name: something descriptive based on Project
* Local Dev URL: sitename.test (all lowercase, single word)
* Project directory: Store all Unity projects in same folder
* Choose custom environment:
  * PHP Version > Latest available
  * Web server = Apache
  * MySQL > Latest Available
* WordPress Credentials
  * Username: unityadmin
  * Email: admin@unitymakes.us
  * Password: Create new secure password and enter the info in the [Pre-Build Checklist form] (https://forms.gle/vreZiAdHggATknt7A)

## Create Git Repo
Create a new repository in Unity's [GitHub](https://github.com/organizations/unitymakesus/repositories/new)

**Repo name should be the url sitename without .test**

**Do not initialize it with a README, license, or .gitignore files.**

## Set Up Unity Starter Template
1.In terminal, CD to the `app/public/` directory for the new project you created in Local by Flywheel.

2.Run the following command to clone the starter-template repo into your project without a commit history.

```shell
git clone --depth 1 https://github.com/unitymakesus/starter-template.git
```

3.Run the following commands to move the starter-template files into the correct place in your project and remove the starter-template folder.

```shell
rm -rf starter-template/.git
cp -r starter-template/. .
rm -rf starter-template
```

4.Create a local repo with an initial commit and push your local changes to the GitHub repo.

````shell
git init
git add .
git commit -m "Initial commit"
git remote add origin [replace with remote repository URL]
git remote -v
git push -u origin master
````

5.CD to the `wp-content/themes` directory and use command `rm -rf [replace with theme name]` to remove any themes that are not the two Unity specific themes.


## Set Up Unity Starter Theme

1.CD to the `unity-core` theme directory and open the entire folder in Atom

* Update the `resources/assets/config.json` settings:
  * `devUrl` should reflect your local dev url
  * `proxyUrl` should be localhost:3000

* Run the following commands:
  * `composer install`
  * `yarn`  

2.Complete Step One with the `unity-child` theme.  

3.Login to your Local by Flywheel site (url.test/wp-admin) and active the `Unity Child` theme. Once you do this, the starter theme should be working.

## Final steps
- Commit and push all theme changes up to GitHub
- Make sure to submit the [pre-build checklist](https://docs.google.com/forms/d/e/1FAIpQLSePcuWoTGgeKrsRLtlOCYJD8UbOFwBthBkXPlRJNRttsrlxfQ/viewform)
