---
layout: default
published: true
weight: 4
---

# Setting up a Staging Site
login to server https://server.unitymakes.com:2087/

unitycom user

list accounts > create new accounts

* domain: sitename.beta.unitymakes.us
* username: sitename
* pw: autogenerate
* email: admin@unitymakes
* package: default
* mail routing: remote

click create

go into account with cpanel icon


## Install WordPress
1. In cPanel, WordPress manager
2. New site
3. Advanced config
- Delete 'wordpress' from subdirectory
- user & pw: usual
4. Install

## Set Up Git Deploy
1. In local repo, edit line 3 of `.cpanel.yml` file: replace `user` with `clientname`
2. In cPanel, Git Version Control
3. Create repo. Past in the Github clone URL. The following should be automatically populated:
- Repo path: `home/clientname/repository/projectname`
- Repo name: `projectname`
4. Add new remote for staging, `git remote add staging [ssh url]`
5. Push `develop` branch.
