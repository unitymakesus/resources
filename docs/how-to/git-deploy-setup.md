# Setup New Git Deploy

## In website's cPanel

Add user’s computer’s public key to SSH Access in cPanel:
* Manage SSH Keys > Import Key
* Name it as user_computer (like alisa_mac)
* Paste the computer’s id_rsa.pub into public key box. Don’t use a passphrase.
* Go back to Manage Keys and then Authorize the public key you just added

## In Terminal

1. SSH into account [account_name]@173.236.13.74. You’ll be asked to enter the passphrase you set when creating the key on your computer. When in doubt, try your computer password.

2. Type the following:

```bash
# @ ~
$ mkdir -p git/production.git
$ cd git/production.git
$ git init --bare
$ vi hooks/post-receive
```

In vi editor, type `i` to insert text, then copy and paste the following:

```
#!/usr/bin/env ruby
# post-receive

# 1. Read STDIN (Format: "from_commit to_commit branch_name")
from, to, branch = ARGF.read.split " "

# 2. Only deploy if master branch was pushed
if (branch =~ /master$/) == nil
  puts "Received branch #{branch}, not deploying."
  exit
end

# 3. Copy files to deploy directory
deploy_to_dir = File.expand_path('~/public_html')
`GIT_WORK_TREE="#{deploy_to_dir}" git checkout -f master`
puts "DEPLOY: master(#{to}) copied to '#{deploy_to_dir}'"
```

Push the `esc` key and then type `:wq` to save your edits and quit vi.

Back in the regular terminal, type the following:

```bash
# @ ~/git/production.git
$ chmod +x hooks/post-receive
```

## In the local repo

Add remote:
`production	ssh://[account name]@173.236.13.74/~/git/production.git`

Now you can git push to production!!! WOOO!!!

---
This was modified from: http://krisjordan.com/essays/setting-up-push-to-deploy-with-git
