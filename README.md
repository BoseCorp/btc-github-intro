# btc-github-intro
GitHub is a wonderful collaborative tool with much more than just version control. In this workshop we'll go through the process of creating a repository, setting permissions, protecting branches, branching code, conducting code reviews, issue tracking, and general best practices.

# About GitHub

## Git
- A distrubuted version control system, been around since 2005
- Learn it here: https://try.github.io
- You don't need to know much git if you use a Git client
  - GitHub Desktop: https://desktop.github.com/
  - SourceTree: https://www.sourcetreeapp.com/
  - You probably know more git than me!
- SVN users: https://www.git-tower.com/blog/git-for-subversion-users-cheat-sheet/

## GitHub
- Web based git hosting service, been around since 2008
- Free for open source projects
- octocat - https://octodex.github.com/

### Why GitHub?
- Open source development is very successful on platforms like GitHub
  - Large software projects with thousands of contributors are able to thrive
  - How do you manage thousands of contributors? GitHub has the tooling
- Bose wants to adopt some Open Source practices, as [Inner Source](https://en.wikipedia.org/wiki/Inner_source)
- Social features, like following people, watching/starring repos
- Let's jump on the [bandwagon](https://github.com/blog/1724-10-million-repositories)

# Activities

## Make a GitHub account
Bose has a corporate GitHub account called [BoseCorp](https://github.com/BoseCorp). To get added to this, you must create an account (with some special configuration) and contact CIS via Remedy for them to add you in. See [this wiki article](https://wiki.bose.com/display/cloud/GitHub+Notes) for more details on the onboarding process.

If you don't have a BoseCorp account and want to follow along, create a free GitHub account.

## Clone a repo
Get the source code from this repository on your computer locally.

### With git
1. Access the repo on GitHub, look for the green button that says "Clone or download"
1. Select use SSH (if HTTPS is selected), get the SSH URL
1. Use _git clone_:
```sh
$ git clone git@github.com:BoseCorp/btc-github-intro.git
```
### With GitHub Desktop
1. Access the repo on GitHub, look for the green button that says "Clone or download"
1. Click "Open in Desktop"
1. Choose where to clone the repository within the GitHub desktop app

### Download the repo as a zip/tar
1. Access the repo on GitHub, look for the green button that says "Clone or download"
1. Click "Download ZIP"

## Creating a repo

1. Look for the [New repository] button on the GitHub homepage: https://github.com/new
1. Select the "Owner". For Bose projects, this should **always** be BoseCorp
1. Give your repository a name (you can change this later easily)
1. Select whether the repo is public or private. Public is public to the entire Internet. **You most likely should always choose private**. Be careful!

### Create a README
- The _README.md_ file renders when you visit any repository on github.com.
- Readmes are really important if you want other teams to collaborate or consume your project.
- Readmes should contain:
  - An overview of what the repo contains
  - Instructions for getting it running
  - Links to necessary API/usage documentation
- Sometimes badges <img src="https://img.shields.io/badge/kinda-like this-green.svg"> are displayed on the readme. These give details to the project's build/test status.
- Markdown (and some HTML) is rendered in the readme. It's useful to reference a [markdown cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).

### Permissions
Private repositories are, by default, only visible to you. You must share them with your colleagues if you want them to collaborate.

1. Go to _Settings > Collaborators and teams_ and add a user or a "team" to your repo.

#### Protected branches
Special protection rules can be enforced by GitHub for your branches. For example, let's say you wanted to make sure nobody could change code in a protected branch without being an administrator. This can be configured in _Settings > Branches_. 

Additionally, if you're working with a Galapagos microservice. Jenkins is integrated with GitHub so you can also enforce that no pull requests can be merged until all tests have passed on Jenkins.

## Adding a fix
Let's add a new feature to our project. Use one of the following methods to make a change to your repository.

### With GitHub Desktop
1. Open GitHub Desktop and select _Branch > New Branch_.
1. Enter a branch name like `fix-abc`.
1. Make a code change.
1. You should see the changed files show up in GitHub Desktop.
1. Add a _commit_ message and click _Commit to fix-abc_.
1. You should now be able to browse to your repo on github.com, select your branch, and see the change.

### With git
1. Navigate to your repository via a terminal window
1. Create a new branch based on _master_ `git checkout -b fix-abc`
1. Make a code change
1. `git status` should show there are changes
1. `git add your-changed-file.txt` to add the changes to the staging area
1. `git commit -m "added a few blank lines"` to commit the changes
1. Finally, you need to push the changes to your remote branch on GitHub (which is your origin): `git push origin fix-abc`
1. You should now be able to browse to your repo on github.com, select your branch, and see the change.

### With github.com
1. Navigate to your repository on github.com
1. Click the _Branch_ button.
1. It will open a pulldown, enter the name of your branch in the text box: `fix-123`.
1. It will now load the branch on github.com. Make a code change.

### Private forks

### Pull requests/code reviews
- Pull requests are a GitHub feature, and its not a _git_ term.
- Pull requests tell the administrator of a repo that you would like them _pull_ your change into their branch.
- This is how large open source projects operate. You can't make changes to them directly, but you can copy the repo elsewhere, make a change, and request someone to pull in the change.
- https://github.com/illacceptanything/illacceptanything
- The act of reviewing a Pull Request facilitates a "code review"

Let's conduct a code review on our previously-made fix branch. To do so, we need to create a pull request to merge our new branch into the old one.

1. Navigate to your repository on github.com
1. Click the "New pull request" button
1. Select `master` as your base branch.
1. Select `fix-123` as your compare branch.
1. Click the _Create pull request_ button.
1. It's a good idea to put a summary of the changes you made, in addition to any related Jira ticket links.
1. Add another user as a reviewer. This will send them and email asking them to review the pull request.

## Issue tracking

## Website hosting

## Tags

### Comparing tags
- https://github.com/BoseCorp/bmx-adapter-tunein/compare/0.2.8...0.3.5
