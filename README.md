# revature

What is VCS?

VCS stands for Version Control Systems; it's synonomous with Revision Control and SCM (Source Code Management); it's main functionality is to manage a collection of source code along with a history of the changes that is made on that code. This allows the developer to see all iterations of the code and if necessary, revert the source code to a previous version. Another benefit to VCS is that it allows multiple users, through branching, to work on the code simultaneously. With VCS, both large and small scale projects can be shared and worked on by multiple people throughout the code--granted that they have access to the source code at all.

What is git?

Git is an implementation of a VCS (SCM). Git is a software that runs on the local machine and is used to track and commit all changes done to the source code of any particular repository that the user could be working in.

When do we use git/Why is git important?

git should be used as you are working on any project and editing your source code. Commit often and commit early; the earlier and more often you commit, the easier it will be for you and others--if there are other collaborators on your project--to see and view your changes. This prevents situations where your both working on features and end up drastically changing key parts of the source code only later down the line not know what changes were made and how it affects the project as a whole. Another reason why git is important is that it allows users to work on and track changes done on right their on their local environment with or without access to the internet. All edits are tracked locally and will be available to "cloned"/pushed to a remote repository hosting environment. 

Three main states of Git/Version Control:

Modified: The user has made changes to a file, but have not commit the changes to a database
Staged: The user has marked changes to the file--in the current version--to be included in the next commit snapshot
Committed: The data--changes that have been made to the code--is stored in the local database.

Git Workflow: 

git init--initializes/creates the initial repository (locally--if done through the terminal)

git add .--moves all changes that have been made to the repository (i.e. changes to source code, insertion of files, etc.) and preps them for the staging process

git commit -m"message"--adds a commit message that encapsulates all the changes done to the repository in this iteration and sends those changes, along with the message to be stored in a local database

git push--this pushes a copy of the changes made on the repository to a remote repository hosting service (mainly github); acts as another way to keep track of the code's history and allows collaborators the ability to see and pull those changes to their local repository.


Gitbash:

Application for Windows Operating System environment; this package installs Bash utilities and Git on your native windows operating systems and acts as an extra emulation layer for command line interfaces.


Initializing a git repository:

git init--will create a .git file in the directory that you are currently working in. This allows git to start tracking changes that are being made within the repository.

git clone [url] [directory(optional)]--clones an existing remote repository to your local environment; [url] will be the github url of the repository you are cloning and [directory] is the directory that you want to clone your repo into--if no arguement is added, git will default clone the repository into the current directory you are working in.

.gitignore?:

literally "git" + "ignore"; the purpose of this file is to tell git which files and changes need to be tracked which does not. Convetionally any file name that you put in the gitignore file will not be tracked by git, and will not be sent to a remote repository that you are pushing to.

conventions within the gitignore file:

* is used as a wildcard match.
/ is used to ignore pathnames relative to the .gitignore file.
# is used to add comments to a .gitignore file.
** can be used to match any number of directories.
! to negate a file that would be ignored.

ex.
*.log--will not let git track any files that end with the "log" file type
!example.log--this line dictates that example.log will be tracked by git despite it being a .log file.

How is git different from github?

Github is a website that allows for and hosts remote versions of repositories that the user might have on their local environment; github is one of many websites that can host remote repositories and changes tracked by git which in turn allow other users to access that repository for a variety of reasons. Basically, github and these other web apps just saves a copy of whatever the user was doing on their local machine--allowing for easier and worldwide access. Git however, operates at the local environment and is in charge of version control. Git will track changes done within the repository irregardless if you have a github account or not. One can think of it this way: github cannot exist without git or any other form of version control; but git can exist and function without github.

What is repository?

a repository is a place--either local or remote where all files that are relevant to the source code is stored and accessed


How do we tell when a folder is git repository or not?

on the terminal, at the end of the line where it shows you what directory you are in, there will be the branch name in parenthesis to denote that the folder you are in is initiated as a git repository

What's the difference between remote and local repository?

Remote repositories are hosted on a different environment and not on the local hardware--github is a remote repository hosting web application, aws has their own way of hosting repositories remotely. Local repositories are held and tracked on the local hardware--it is nearly impossible for another person to clone your repository if its only being tracked on the local environment--there are some ways but its not easy to do.

What is cloning?

Cloning is the process of copying all contents from a repository to your local machine; this is done at the start and you'll usually only use git clone once during the initial setup of the repository; once you have the repository on your local machine, you'll use git pull to get any changes made to the remote repository.

What is staging?

staging is the act of marking files or any changes in the git repository so that they will be included in the next commit snapshot

What is committing?

the act of storing your changes and the code's history in the local/remote database

how do I look at my commit history?

git log -- shows a list of all commits in reverse chronological order
git history -- similary but shows changes in a specific commit; often times you'll have to know the commit hash to be able to use this command line prompt

What is pulling?

Pulling is "bringing down" any changes to the source code in the remote repository onto your local machine. For example, if one of youre team members added a file into the repository that the source code needs to run the program correctly, you would have to pull that change along with the file down to your local repository.

What is pushing?

Merges any changes you made on your local machine to the remote repository


Describe the basic git workflow
What are branches, and why are they important?
What is merging?
What is a Pull Request?
What are some recommended practices when working with others?
(T/F) It is recommended to push directly to main especially when working in a team project
