# Multiple SSH Keys settings for different github account:

## GEN key:
ssh-keygen -t ed25519 -C "your_email@example.com"

## Start the ssh-agent in the background:
eval `ssh-agent -s`

## Add key to identity:
ssh-add ~/.ssh/id_YOUR_ID

## Open id key public:
cat ~/.ssh/id_YOUR_ID.pub

## Check list id:
ssh-add -l

## Delete id from identity:
ssh-add -d ~/.ssh/id_YOUR_ID

## Config ssh key:
use: nano ~/.ssh/config

```
#study account
Host github-txm-minh21
HostName github.com
User git
IdentityFile ~/.ssh/id_txm_study

#project account
Host github-txm-minh
HostName github.com
User git
IdentityFile ~/.ssh/id_txm_project
```

## Git clone:
git clone git@github-txm-minh21:txm-minh21/study-git.git
git clone git@github-txm-minh:txm-minh/study-git.git

## Config account:
git config user.name "your_usename"
git config user.email "your-email@example.com"

