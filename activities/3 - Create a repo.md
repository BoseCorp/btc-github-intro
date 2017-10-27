## Creating a repo

1. Look for the [New repository] button on the GitHub homepage: https://github.com/new
1. Select the "Owner". For Bose projects, this should **always** be BoseCorp
   - If you have a free account, just select yourself as the owner
1. Give your repository a name (you can change this later easily)
1. Select whether the repo is public or private. Public is public to the entire Internet. **You most likely should always choose private when its a Bose project**. Be careful!

## Making changes to files
Use the steps below as a reference for adding files to your repos.

### Via github.com
1. Navigate to your repository
1. Either click on the file you want to edit > pen icon, or click "Create new file"
1. Enter the content you want
1. Click "Commit changes"

### Via git
1. Make the changes/additions to the files you want within the local repo
```sh
$ git add your_file_name
$ git commit -m "Your commit message"
$ git push origin master
```
## Let's make some files
### Via GitHub Desktop
1. Make the changes/additions to the files you want within the local repo
1. You'll see the change appear on the left side.
1. Enter a description of your changes in the "Summary box"
1. Click "Commit to master"
1. Click "Push origin"

### Create a README
- The _README.md_ file renders when you visit any repository on github.com.
- Readmes are really important if you want other teams to collaborate or consume your project.
- Readmes should contain:
  - An overview of what the repo contains
  - Instructions for getting it running
  - Links to necessary API/usage documentation
- Sometimes badges <img src="https://img.shields.io/badge/kinda-like this-green.svg"> are displayed on the readme. These give details to the project's build/test status.
- Markdown (and some HTML) is rendered in the readme. It's useful to reference a [markdown cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).

### Add a .gitignore
- Sometimes you may not want to add certain files to your repository. 
- Use a `.gitignore` file to ensure that those files cannot be added.
- https://www.gitignore.io/

### Review commit history
- Look at the commit history of your repository
- Review your open branches

### Permissions
Private repositories are, by default, only visible to you. You must share them with your colleagues if you want them to collaborate.

1. Go to _Settings > Collaborators and teams_ and add a user or a "team" to your repo.

#### Protected branches
Special protection rules can be enforced by GitHub for your branches. For example, let's say you wanted to make sure nobody could change code in a protected branch without being an administrator. This can be configured in _Settings > Branches_. 

Additionally, if you're working with a Galapagos microservice. Jenkins is integrated with GitHub so you can also enforce that no pull requests can be merged until all tests have passed on Jenkins.
