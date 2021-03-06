# Welcome to Git and GitHub Training!

## Preliminary Steps
Create a GitHub account

[Install Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)

Make sure `git bash` (on MacOS, use `terminal`)is installed as part of this.

[Creating SSH keys](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/)

[Adding SSH keys to GitHub Account](https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/)

[Testing SSH](https://help.github.com/articles/testing-your-ssh-connection/)


## Step 1 -- Fork the repository
![Alt text](images/fork_repo.png?raw=true "Optional Title")

Once forked, go to your fork.  It should have the url

`https://github.com/<your GH name>/core`

## Step 2 -- Clone your fork
Using Git BASH navigate to somewhere useful create a directory called `trafficsensemsd`.  I usually put it at `~/` (home folder)

Replace `<your GH name>` and `<repo name>`

`git clone git@github.com:<your GH name>/<repo name>.git`

For example, my fork of this repository is
`git@github.com:eilifm/core.git`


You should see a structure similar to that of the main repo at the time of forking.

## Step 3 -- Practice Using Git
1. Navigate to the root directory of your cloned repo.  (`~/trafficsensemsd/core` in this example)
2. Navigate to `misc/training_resources/git_training` in both `git BASH` (or terminal on MacOS) and the file explorer (Explorer for Windows/Finder for MacOS)
3. Add a folder called `<your_first_name>_<your_last_name>` (ex. `eilif_mikkelsen`)
4. Using your favorite text editor, add a file to this folder called "README.md"
5. In the newly created README.md, type your name and favorite color.  Save.
6. From `git BASH` (or terminal on MacOS) add the changes you to a commit with `git add -r ./<your_first_name>_<your_last_name>`
7. Now let's commit the added changes to your local branch with `git commit -m "initial README.md commit"`.  
`-m` followed by double quoted message is the commit message.  We will see where this shows up later.
8. Now, push the local commit back to the remote repository in GitHub with `git push origin master`.  Once complete, you should 
see the changes you made reflected in GitHub. 

On GitHub, the commit should look something like [this](https://github.com/eilifm/core/commit/5e7e6512621703fbc6e537418e599d892f174e57)

9. On your fork of `core` in GitHub, create a Pull Request.
A Pull Request is a GitHub tool to initiate the process of merging changes you made on your fork back into a target branch of the main 
`TrafficSenseMDA/core` repository.  Most of the time you will be merging from your fork's `master` branch to the main `master` branch. 

![Alt text](images/make_pr.png?raw=true "Optional Title")

10. On the next screen be sure that the target and source branch are correct.  If opening a PR from your fork's `master` branch,
the default will look like the image below. 

![Alt text](images/open_pr.png?raw=true "Optional Title")

11. In order to help out the rest of the team, give your PR a title and description that describes your changes. 
![Alt text](images/describe_pr.png?raw=true "Optional Title")

Click "Create Pull Request"

12. Once created add eilif as a reviewer.  (I can't add myself so it is blank)
![Alt text](images/reviewers_pr.png?raw=true "Optional Title")

# Other useful things to do
## Adding additional "remotes"
Your repository is not a clone of the "remote" repository in your fork on GH.  This "remote" is called
`origin`.  Let's add another remote repository.  In this case let's add the main fork of the `core` repo.

`git remote add msd git@github.com:TrafficSenseMSD/core.git`


# Some other online tutorials
https://guides.github.com/activities/hello-world/

# Quick Reference
[Amazing Git Cheat Sheet](http://rogerdudler.github.io/git-guide/)