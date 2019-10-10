# Collaboration

## Git Set-Up Tutorial
This is a guide on how to set up Git so it can be used to work collaboratively with a group of people. It is assumed that the user will have already installed [GitHub Desktop](https://desktop.github.com/) and created an account on [github.com](github.com).
- The first step to making sure that you will be able to collaborate with others is to set up your SSH key and link it to your [github account](https://github.com/settings/keys). Having an SSH key set up means that you will be able to clone other people's repositories and then push any changes that you make back into the master.
  - Before this, you must check for an existing SSH key in your system, and if one does not exist, then you will create one. To check, you must open your terminal or Git Bash and type in *ls -al ~/.ssh*. This will list the files in your .ssh directory, if it exists. If it does not exist, you must create a new one.
  - To create a new SSH key, type *ssh-keygen -t rsa -b 4096* and enter through all the prompts. Do not set up a password as it can get tedious having to enter it at every push.
  - Now, to add your SSH key to your account, you must copy the key and paste it into the field. The easiest and cleanest way to get the key is to go to the terminal and enter *clip <~/.ssh/id_rsa.pub*. This copies the exact text that needs to be pasted into the **Key** field in order to connect it. Now that your SSH key is set up, you can clone and make changes to your group members' projects.
- Understanding the concept of branching is a big part of bring able to collaborate effectively in a group. A branch is essentially an addition to the main repository that can be merged when it needs to be used or removed when no longer needed or obsolete. It is a way for many collaborators to contribute to a project without causing major disruptions to others who may also be working simultaneously.
- A common issue that comes up when working collaboratively in Git is a merge conflict. A merge conflict occurs when you merge branches that have competing commits, or commits that work against one another.
  - Common ways to create a merge conflict is when two or more people make changes to the same line of the same file, or when one person edits a file while another person deletes that same file.
- Resolving a merge conflict can generally be done in two different ways. It is possible that sometimes Git itself can automatically resolve differences between branches, but there are manual ways.
  -  The first way is for a specific type of merge conflict, like when people make changes to the same line of the same file. Git has its own [conflict editor](https://help.github.com/en/articles/resolving-a-merge-conflict-on-github) which isolates the affected line or lines and lets the user make their choice on what to keep.
  - For all other types of merge conflicts, the issue must be resolved on a local clone of the repository and then pushing the change to your branch on GitHub.

## 1. Forking vs. Cloning
### Forking
Forking a repository is essentially creating a linked copy of a repo where you can make whatever changes you wish without having any effect on the original project. Once you make changes to your *forked* version of the repository, you can then submit a pull request which will allow you to contribute your proposed changes to the original project. A forked copy has a real connection to its original repo as opposed to a cloned copy.

### Cloning
Cloning a repository is like downloading an offline copy of the project that is not connected to the original in any way. You are downloading a specific iteration of the repository at a specific point in time and that is your local copy. When you make changes to this clone, you can then push the changes back to the original project, but only if you are added as an official contributor by the creator of the repository.

## 2. Pull Request
A pull request is how a contributor can share his changes to a repository with the rest of the group and to discuss what parts should be kept and added to the main repository and what should be discarded. This is a good way for the whole team to review the propose changes of a contributor and discuss how to proceed.

## 3. Adding a Collaborator to a GitHub Repository
Adding a collaborator to a GitHub repository is the way to work with cloning. Since cloning creates a disconnected copy of the repository on the contributor's local computer, they will need a way to upload any changed they make to the original repository. By adding an authorized person as a contributor, the creator of the project gives permission to another person to push commits to the repository.
