1. log in to WHM
2. Create new account
- url: clientname.staging.unitymakes.us
- username: clientname
- ps: random generator (check i have copied in safe place)
- email: admin@unitymakes.us
- package: unity_micro
- mail routing: remote mail exchanger
3. List Accounts
4. Cpanel icon for staging site 
5. SSH Access
6. Manage SSH keys > Import key
7. Name it as user_computer (like alisa_mac)
8. Paste the computer’s id_rsa.pub into public key box. Don’t use a passphrase.
9. Go back to Manage Keys and then Authorize the public key you just added

10. In cPanel, wordpress manager
11. New site 
12. advanced config
- user & pw: usual
13. install 

14. potentially look into cpanel and git instead of terminal 
```
# @ ~
$ mkdir -p git/production.git
$ cd git/production.git
$ git init --bare
$ vi hooks/post-receive
```

In vi editor, type i to insert text, then copy and paste the following:
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

Push the esc key and then type :wq to save your edits and quit vi.

Back in the regular terminal, type the following:
```
# @ ~/git/production.git
$ chmod +x hooks/post-receive
```

15. add remote and push 

16. ssh accountname@ip
