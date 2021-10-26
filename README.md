# CS1200 Beginners Git Workshop

Git instructions taken from [NUWIT Website Hack Day 2021](https://github.com/britneyart80/hack_day_2021)

## Table of Contents
- [Installing Git](#installing-git)
- [Setting up Github](#setup)
- [Commit Changes to Git and Github](#commit-changes)
- [Branching](#branching)
- [Merging](#merging)

<a name="installing-git"></a>
### Installing Git 
To check if you have git installed on your machine, type `$ git` into your terminal. If the response is a list of git commands, you already have git installed!

- **[For Mac](http://git-scm.com/download/mac)**
- **[For Windows](https://www.computerhope.com/issues/ch001927.htm)**
- **[For Linux](https://git-scm.com/download/linux)**

<a name="setup"></a>
### Setting up Github
[Create a github account.](https://github.com/join)

Type the following into terminal to add a username to your Git. It can be your Github username, or just your name:

`git config --global user.name "[GITHUB USERNAME]"`

And also type the following into terminal to match your Git email to your Github email. **This email must match the one you associated with your Github account**:

`git config --global user.email "email@example.com"`

Return to the Github repository for this workshop. Fork this repository using the link below the topbar:
  ![How to fork a repository](https://help.github.com/assets/images/help/repository/fork_button.jpg)
  
**Copy** your new repo's clone url:

![Clone button](https://help.github.com/assets/images/help/repository/clone-repo-clone-url-button.png)

![Url to clone](https://help.github.com/assets/images/help/repository/https-url-clone.png)

In your terminal, navigate to the folder/directory you want to put your project in. 

To navigate into a folder, type `cd [folder name]`

To go back a folder, type `cd ..`

To see where you are in your file system, type:

Linux/Mac: `pwd`

Windows: `cd`

To see what files/folders you have in your current directory, type:

Linux/Mac: `ls`

Windows: `dir`

For more information on using the terminal, go [here](https://enexdi.sciencesconf.org/data/pages/windows_vs_mac_commands_1.pdf)

**Type** the following command into your terminal, **pasting** the git clone url you just copied:

```git clone [COPIED GIT CLONE URL]```

and press enter...

You should now have this repo on your machine!

<a name="commit-changes"></a>
### Commit Changes to Git and Github

Navigate into your github repo folder in your terminal.

To see all the files you've changed, type:

`git status`

To stage your changes to be committed, type:

`git add .` OR
`git add [file name]` if you only want to commit certain files

Then type the following command to commit the changes to your **local repository**. Your local repository is the git repository that is tracking the changes on your laptop only. Your **remote repository** is your Github repository, the one that saves all your changes online.

`git commit -m "Add my name"` OR
`git commit` and type out your commit message in the text editor. If you do this one, make sure you set your default text editor to one you know how to use (vim can be tricky). [Here are instructions on how to do this](https://docs.github.com/en/get-started/getting-started-with-git/associating-text-editors-with-git)

Once the changes are committed, let's push them to your Github repo.

`git push`

You should now see the changes on your Github repo.

You can use those three commands to save your work throughout your coding process.

<a name="branching"></a>
### Branching

Branching lets you "branch" out from the original code base and make changes to just that branch. Branches are useful when you're collaborating with multiple people on the same repository because it allows each collaborator to make changes independently of each other.

To see all branches, type:

`git branch`

To make a new branch, type:

`git branch [branch name]`

To work on a specific branch, type:

`git checkout [branch name]`

To make sure you have all your collaborators' changes and branches, type:

`git pull`

<a name="merging"></a>
### Merging

When you've finished working on your branch, commit all your changes to the branch. 

**If you get an errors at this point, don't freak out!**

If git says "the current branch has no upstream branch" when you type `git push`, type:

`git push --set-upstream origin [branch name]`

If you then get an error saying that you need to use a personal access token, follow [these instructions](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token)

Now, let's merge this branch back into the main code base.

To see what branch you're on, type:

`git status` OR `git branch`

Say you want to merge a branch into your main branch. If you aren't on the branch you want to merge, type:

`git checkout [merging branch name]`

Next, type:

`git merge main` OR `git merge [merging into branch name]`

If you have any merge conflicts, make sure your resolve them, commit your changes to your branch, and then resume merging.
