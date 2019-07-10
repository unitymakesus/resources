---
layout: default
published: true
weight: 2
---

# Contributing to an existing Project
Use this workflow if someone has already set up the starter theme and there is an existing GitHub repo. Check the [pre-build checklist](https://drive.google.com/open?id=1Yc_hj-tikhQxwk3-YIs9_M9KXlqrz08MdukcZuA5kTM) to get all the information needed.

## Set Up Local Environment
Create a new project in Local by Flywheel:
* Site Name: Use the pre-build Site Name
* Local Dev URL: Use the pre-build Local Site Domain
* Project directory: Store all Unity projects in same folder
* Choose custom environment:
  * PHP Version > Latest available
  * Web server = Apache
  * MySQL > Latest Available
* WordPress Credentials
  * Username: unityadmin
  * Password: Use pre-build password
  * Email: hello@unitymakes.us

## Clone GitHub Repo
1. In terminal, CD to the `app/public/` directory for the new project you created in Local by Flywheel.

2. Run the following command to clone the starter-template repo into your project without a commit history.

```shell
git clone https://github.com/unitymakesus/[PROJECT-NAME].git
```

3. Run the following commands to move the theme files into the correct place in your project.
```shell
cp -r [PROJECT-NAME]/. .
rm -rf [PROJECT-NAME]
```

## Set up Theme Dependencies
Make sure all dependencies have been installed:

1. CD to the `project-core` theme directory and open the entire folder in Atom

* Update the `resources/assets/config.json` settings:
  * `devUrl` should reflect your local dev url
  * `proxyUrl` should be localhost:3000

* Run the following commands:
  * `composer install`
  * `yarn`  

2. Complete Step One with the `project-child` theme.  

3. Login to your Local by Flywheel site and activate the project theme.

## Pull down the Staging Database
- On your **local** site (the .test url, not localhost), activate the "WP Migrate DB Pro" and "WP Migrate DB Pro Media Files" plugins. Enter the license key found in Google Drive
- On the **staging** site, login and go to `Tools > WP Migrate DB Pro`. From the settings tab, copy the connection info to your clipboard
- On your **local** site, go to `Tools > WP Migrate DB Pro` and select **PULL**. Enter the staging connection info and check `media files` to also download images. Click `pull`.

**Be very very careful with this step so you don't accidentally overwrite the staging site. Always pull from staging (to get latest local db) or local (to get latest staging db). Never push.**
