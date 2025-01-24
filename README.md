<!-- Markdown Tutorial -->

# **Git**
Git is a Distributed Version Control System (DVCS) created by Linus Torvalds in 2005, and has been maintained by Junio Harmano since then.

#### **Used for :**
1. Tracking codes
2. Tracking who made the changes
3. Coding collaboration

#### **What does git do?**
1. Manage projects with repositories
2. Clone a project to work on a localcopy
3. Control and track changes with Staging and Commiting
4. Branch and Merge to allow for working on different parts and versions of project
5. Push local updates to the main project
6. Pull latest version of the project to a local copy

#### **Working with git :**   
1. Initialize git on a folder, making it a repository
2. Git now creates a hidden folder to keep track of changes in that folder
3. When a file is changed, added or deleted, it is considered modified
4. You select the modified files you want to stage
5. The staged files are committed, which prompts git to store a parmanent snapshot of the files
6. Git allows you to see the full history of every commit.
7. You can revert back to any previous commit
8. Git does not store a separate copy of every file in every commit but keeps track of changes made in each commit

#### **Creating Git folder :**
```
mkdir my project
cd myproject
```
>Here, 
>- mkdir -> makes a new directory
>- cd -> changes the current working directory

#### **Initialize Git :**
```
git init
```
Now Git knows that it should watch the folder you initiated on i.e. it is now a Git Repository. Git creates a hidden folder to keep track of changes.

```
ls
```
>ls -> will list all the files in the present working directory

```
git status
```
>git status -> to see if the file is part of our repo or overall repo information

#### Files in your Git repo folder can be in one of 2 states:
1. **Tracked** - Files that Git knows about and are added to the repo
2. **Untracked** - Files that are in your working directory, but not added to the repo

When you first add files to an empty repo, they are all untracked. To get Git to track them, you need to stage them or add them to the staging environment.

<br>

## **Git Staging Environment :**
Staged files are the files that are ready to be committed to the repo you're working on.

**Add only one file to the staging environment:**
```
git add index.html
```
**Add all files in the repo:**
```
git add --all
```
or
```
git add -A
```
or
```
git add .
```

<br>

## **Git Commit :**
Adding commits keep track of our progress and changes as we work. Git considers each commit as "change point" or "save point". It is a point in the project you can go back to if you find a bug or want to make a change.

```
git commit -m "first release on Hello world"
```

#### **Git commit without stage:**
Sometimes small changes in files are made. Staging feels like a waste of time. We can directly commit then. But it is not recommended.
```
git commit -a -m "Updated index.html with a new line"
```

#### **Git commit log :**
To view the history of commits for a repository
```
git log
```

#### **Git status short :**
```
git status --short
```
>- ?? - Untracked files
>- A - Files added to stage
>- M - Modifies files
>- D - Deleted files

### **Git help :**
If you're having a trouble remembering commands or options for commands, git help is used.
```
git command -help
```
Example: 
```
git commit -help
```

- see all the available options for the specific command

```
git help --all
```
- see all the possible commands that git holds
- will display a very long list of commands

<br>

### **Git Branch**
- In Git, a branch is a new or separate version of the main repository.
- Branches will allow you to work on different parts of a project without impacting the main branch.
- When the work is complete, a branch can be merged with the main project.
- You can even switch between branches and work on different projects without them interfering with each other.
- Branching in Git is very lighweight & fast.

#### **New Git branch :**
```
git branch hello-world
```
>It creates a new branch.

```
git branch
```
>To see the list of branches

```
git branch -r
```
>shows remote branches only

```
git branch -a
```
>To see all local and remote branches

```
git checkout hello-world
```
>moves our current workspace from maste branch to the new branch

```
git checkout master
```
>switched back to masterb branch

#### **Emergency Branch :**
```
git checkout -b emergency-fix
```
>Creates a new branch repo named emergency-fix and directly moves to that branch

#### **Delete Branch :**
```
git branch -d emergency-fix
```

#### **Merge Branches :**
```
git merge hello-world
```
<hr>

<br><br>

# **GitHub**
GitHub is the largest host of source code in the world. Owned by Microsoft since 2018. GitHub makes tools that use Git.

#### **Configure Git :**
It lets Git know who you are. It is important for version control system as each Git commit uses this information.

```
git config --global user.name "Cosmic Nomad"
git config --global user.email "cosmicnomad@gmail.com"
```
Here, global is used to set username & email for every repository on computer.
To set for only current repo remove the global.