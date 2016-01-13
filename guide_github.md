# Github Guide
---
* Github Configuration in Linux
* Common Commands

## Github Configuration in Linux
1. Generate SSH key

`ssh-keygen -t rsa -C"mail@mail.com"`
use default configuration, and file */.ssh/id_rsa.pub* will be created. 

2. Copy SSH key to github

Copy text in *id_rsa.pub*.
`cat  ~/.ssh/id_rsa.pub`
Paste it to github.
Verify the configuration
`ssh -T git@github.com`

3. Configure the account

`git config --global user.name "Your Name Here"
git config --global user.email "your_email@example.com"`　

4. Clone repository from github

Initialize the folder in which you want to place the repository
`git init`
Clone a repository
`git clone git://github.com/your_account/aimed_repo.git`
