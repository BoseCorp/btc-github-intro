## Adding a fix
Let's add a new feature to our project. Use one of the following methods to make a change to your repository via branching.

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

### Pull requests/code reviews
- Pull requests are a GitHub feature, and its not a _git_ term.
- Pull requests tell the administrator of a repo that you would like them _pull_ your change into their branch.
- The act of reviewing a Pull Request facilitates a "code review"

Let's conduct a code review on our previously-made fix branch. To do so, we need to create a pull request to merge our new branch into the old one.

1. Navigate to your repository on github.com
1. Click the "New pull request" button
1. Select `master` as your base branch.
1. Select `fix-123` as your compare branch.
1. Click the _Create pull request_ button.
1. It's a good idea to put a summary of the changes you made, in addition to any related Jira ticket links.
1. Add another user as a reviewer. This will send them and email asking them to review the pull request.

### Private forks
- Since you do not have access to modify my repository (https://github.com/Dominick-Peluso-Bose/btc-github-intro) you cannot make a branch. To contribute to the code, you must create a **private fork**.
- Private forks allow users to make tracked changes to a copy of someone else's repisitory.
- You can send a pull request against a origin of a fork. This is how much of the open source community operates.
- You can't make changes to them directly, but you can copy the repo elsewhere, make a change, and request someone to pull in the change.
- https://github.com/illacceptanything/illacceptanything

1. Make a private fork of https://github.com/Dominick-Peluso-Bose/btc-github-intro
1. Change **THIS** to your first name
1. Create a pull request in your private fork with the base branch as `Dominick-Peluso-Bose/btc-github-intro`
