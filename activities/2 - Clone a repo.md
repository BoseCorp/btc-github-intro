## Clone a repo
**Objective:** Get the source code from this repository on your computer locally.

### With git
1. Access the repo on GitHub, look for the green button that says "Clone or download"
1. If 
   - you setup git for SSH, then select use SSH (if HTTPS is selected), and copy the SSH URL
   - you didn't setup git for SSH, then select use HTTPS (if SSH is selected), and copy the HTTPS URL
1. Use _git clone_:
```sh
$ git clone git@github.com:Dominick-Peluso-Bose/btc-github-intro.git
# or
$ git clone https://github.com/Dominick-Peluso-Bose/btc-github-intro.git
```
Now you can examine the files which have been downloaded in the `btc-github-intro` folder.
```sh
$ cd ./btc-github-intro
$ ls
```
Try checking the status with `git status`
```sh
$ git status
```

### With GitHub Desktop
1. Access the repo on GitHub, look for the green button that says "Clone or download"
1. Click "Open in Desktop"
1. Choose where to clone the repository within the GitHub desktop app

### Download the repo as a zip/tar
1. Access the repo on GitHub, look for the green button that says "Clone or download"
1. Click "Download ZIP"
