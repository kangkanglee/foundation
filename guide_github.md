# Github Guide
---
* Github Configuration in Linux
* Common Commands

## Github Configuration in Linux
---
**1\. Generate SSH key**

`ssh-keygen -t rsa -C"mail@mail.com"`

use default configuration, and file */.ssh/id_rsa.pub* will be created. 

---
**2\. Copy SSH key to github**

Copy text in *id_rsa.pub*.

> `cat  ~/.ssh/id_rsa.pub`

Paste it to github, and verify the configuration.

> `ssh -T git@github.com`


---
**3\. Configure the account**

> `git config --global user.name "Your Name Here"`

> `git config --global user.email "your_email@example.com"`　

---
**4\. Clone repository from github**

Initialize the folder in which you want to place the repository

> `git init`

Clone a repository

> `git clone git@github.com:your_account/aimed_repo`

---
## Question & Answer
***
**The way to avoid enterring the password repeatly.**

在linux的～目录下，touch创建文件 .git-credentials

    touch .git-credentials
 
用vim编辑此文件

    vim .git-credentials
 
输入内容格式

    https://username:password@github.com

在终端下执行

    git config --global credential.helper store

可以看到~/.gitconfig文件，会多了一项：

        [credential]
            helper = store
---

