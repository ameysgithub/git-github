# Understanding git and GitHub
Use cases of git and GitHub:
- For including more collaborators to your project
- For saving the history of your project
- Contribution to Open-Source - for sharing your code/adding your changes to the existing code

GitHub is a platform which allows us to host/store our git repositories

- Repository is a folder which stores all the history of the changes made in the project or application

Email service and email platforms synoym to git and GitHub/GitLab/BitBucket

Steps to start with:
1. Download git from [here](https://git-scm.com/downloads)

1. Using terminal commands - ls,mkdir, cd, touch

1. git init to initialize a git repository

1. to know which files are changed in the project which are not saved in the history of the project i.e. untracked files, use git status

1. add files to the staging area, git add . or git add "individual filename"

1. to store the files in git history of the repo, git commit -m "commit message added"

1. Using terminal commands - vi, cat

1. to remove from staging area, git restore --staged "filename"

1. to list the entire history of commits, use git log command

1. terminal commands : rm -rf "filename"

1. deleted any file by mistake so for going back to previous commit i.e. unstage a particular commit, copy the hashValue in git log command run git reset hashValue, the remaining commits are in before staging area

1. putting commits in stash area for later use - not adding to project but keeping it to be added later, use git stash command

1. git stash pop for getting the commits that are in the stash area

1. to remove the changes in the stash area, use git stash clear command

1. remote means working with URLs, add- means adding new URL, origin - URL name (by convention it is given as origin if it is in personal account), git remote add origin "URL"
1. git remote -v

1. to share the chnages to the URL, use the command - git push origin master

1. what do we mean by branches
    - when working on a new feature or resolving abug always create a separate branch
    - never commit directly to the main branch, since if the commit you make may have some errors thus causing a high-level failure
    - a lot of contributors working on a project
    - creating branch, git branch "branchname"
    - using that branch, git checkout "branchname"
    - to add your code to the main branch, use git merge "branchname"
1. working with existing projects on GitHub
    - create a copy of the project in your own account, i.e. fork the project to your GitHub account - hence you can perform changes to it
    - use git clone "URL" for fetching the project from your account to perform changes locally
    - from where you fork the project it is the upstream URL, git remote add upstream "URL"
    - git remote -v

1. What is a pull request?
    - When you want to add your changes to the main project code, you request to the main project managers, they run some tests, give some suggestions and then your request is rejected or accepted(very rare).
    - you cannot push to upstream URL if you are not the project maintainer
    - you can perform "git push origin branchname"
    - then you get a "Compare and pull request" option in GitHub account
    - create new pull request for new feature, one branch can associate to one pull request, hence it is advised to create a new branch for every new pull request i.e. new features

1. going back to the previous commit, git reset hashValue

1. to force push a commit, git push origin "branchname" -f

1. merging pull requests, thus adding the changes made in the personal forked repo will reflect in the main project

1. get the updated main project code:
    - fetch upstream button on GitHub
    - using git commands in terminal
        1. git checkout "mainbranch"
        1. git fetch --all --prune(prune means the ones that were deleted will also be fetched)
        1. git reset --hard upstream/main
        1. git push origin main

1. for fetching content directly from main project code:  
    1. git pull upstream "main-project-main-branch-URL" commmand
    1. git push origin main

1. update your main branch before making a new branch

1. merge conflicts
    - changes made in the same file or same line number
    - GitHub wants you to resolve the conflicts caused

1. squashing your commits
    1. git rebase -i "base commit hashValue"
    1. change the pick string to s, in the interactive environment

1. adding a git repo inside another repo, nested repos - git submodule add "inside-repo-URL" nested-filename

Git CheatSheet by GitHub Education [here](https://education.github.com/git-cheat-sheet-education.pdf "Git CheatSheet")