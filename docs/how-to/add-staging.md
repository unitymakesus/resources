# Create New Staging Site

## Set up new hosting account
1. Log in to WHM
2. Create new account
- url: clientname.staging.unitymakes.us
- username: clientname
- ps: random generator (check "I have copied in safe place" -- but don't actually save it.)
- email: admin@unitymakes.us
- package: unity_micro
- mail routing: remote mail exchanger
3. List Accounts
4. cPanel icon for staging site 

## Add SSH Keys
1. SSH Access
2. Manage SSH keys > Import key
3. Name it as user_computer (like alisa_mac)
4. Paste the computer’s id_rsa.pub into public key box. Don’t use a passphrase.
5. Go back to Manage Keys and then Authorize the public key you just added

## Install WordPress
1. In cPanel, WordPress manager
2. New site
3. Advanced config
- Delete 'wordpress' from subdirectory
- user & pw: usual
4. Install 

## Set Up Git Deploy
1. In cPanel, Git Version Control
2. Create repo
- Toggle off clone
- Repo path: `home/clientname/repository/projectname`
- Repo name: `projectname`
3. In local repo, edit line 3 of `.cpanel.yml` file: replace `user` with `clientname`
4. Add remote, `git remote add staging [ssh url]`
5. Push `develop` branch.
