## Make a GitHub account
Bose has a corporate GitHub account called [BoseCorp](https://github.com/BoseCorp). To get added to this, you must create an account (with some special configuration) and contact CIS via Remedy for them to add you in. See [this wiki article](https://wiki.bose.com/display/cloud/GitHub+Notes) for more details on the onboarding process.

If you don't have a BoseCorp account and want to follow along, create a free GitHub account.

At this point, you can decide if you'd like to use GitHub via command line with `git` or use a client like [GitHub Desktop](https://desktop.github.com/) or [Sourcetree](https://www.sourcetreeapp.com/). I recommend setting up both!

### Git setup
- Install [Git](https://git-scm.com/downloads) (but check that it's not already installed with `git --version`!). 
- Now, if you don't setup 2FA, you can use `git` as is. 
  - You will be prompted for a GitHub username and password when using `http` repository URLs.
- If you did setup 2FA, you cannot use `http` repository URLs. You must use SSH.

#### Setup up GitHub with SSH
Create an SSH key, continue through the prompts. I recommend you _not_ setting a passphrase when prompted.
```bash
$ ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```
Add they key to the SSH Agent folling [these instructions](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/#adding-your-ssh-key-to-the-ssh-agent).
Then add the key to your account by following [these instructions](https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/).

### GitHub Desktop setup
- Download [GitHub Desktop](https://desktop.github.com/) and install it
- Sign in with your GitHub credentials. If you enabled 2FA, you'll have an extra verification setup.

### Sourcetree
- I don't use it so I'm not sure, but it likely will require you to setup an SSH key and add it to your GitHub account.
