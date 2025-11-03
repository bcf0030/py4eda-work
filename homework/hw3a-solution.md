# HW3A Solution - Git and Version Control
## Part 1: Repository Cloning
I successfully cloned the class repository from `https://github.com/olearydj/INSY6500` to
`~/insy6500/class_repo`.
### Key Commands Used
- `git clone <url>` - Create local copy of remote repository
- `git log` - View commit history
- `git remote -v` - Check remote repository connections
## Part 2: Portfolio Repository Creation
I created my personal course repository with:
- Professional README.md describing the project
- Proper .gitignore to exclude unnecessary files
- Organized directory structure for homework, projects, and notes
### Understanding Git Workflow
The three-stage workflow:
1. Working Directory: Where I edit files
2. Staging Area: Where I prepare commits with `git add`
3. Repository: Where commits are permanently stored with `git commit`
## Part 3: GitHub Publishing
Successfully published repository to GitHub:
- Used `git remote add origin` to connect local repo to GitHub
- Used `git push -u origin main` to upload commits
- Verified all files and commits are visible on GitHub
### The Remote Connection
My local repository is now connected to GitHub:
- `git remote -v` shows the remote URL
- `git push` will send my commits to GitHub
- `git pull` will get updates from GitHub (if changes are made on GitHub)
### Details
Details from my setup:
- Repository URL: https://github.com/bcf0030/py4eda-work.git
- Output of `git remote -v`: NOTE: I removed my personal access token from the URLs below.
origin	https://bcf0030:<personal_access_token>@github.com/bcf0030/py4eda-work.git (fetch)
origin	https://bcf0030:<personal_access_token>@github.com/bcf0030/py4eda-work.git (push)
- The output of `git log --oneline`:
e685b5d (HEAD -> main, origin/main) Add hw3a solution document
6e4fc68 Initial commit: Add README and .gitignore
### Reflections:
Git Workflow Benefits:
a) Typically, I would keep multiple versions of my work. For example, as I made progress on a document,
I would save the updated versions with the date or a version number added to the end of the filename.
That approach is much less useful and makes it harder to tell what the differences between the versions are.
With Git, you can always tell exactly the differences between the versions (commits). Another perk of Git
is not having to keep multiple versions of a file saved somewhere. Git takes care of that history and allows
you to revert to a previous version if needed. Keeping multiple versions of files in a code project is
extremely difficult to manage. Git makes this simple, once you get the hang of it.
b) At a previous job, I was creating a VBA script to automate some monotonous work, and I got to the point
where it was mostly working. I came back later and made some changes, and it broke. I could not figure out
what I had changed that had broke it. I spent a lot of time debugging to solve it. If I had been using Git,
I could have easily checked what I had changed, or reverted a commit or two until I got back to a working
version.
Repository Organization:
a) It is important to have a your reference only repo and your working repo separate to keep your work
isolated from read-only reference files. You cannot push to the read-only repo, so you should not have the files
within your working repo. You should only be pulling from the read-only repo. If you mixed them together,
you would run into issues while trying to push. You would two separate remotes, one you can only pull from
and one you can pull and push to. You would receive errors if you tried to push changes to the read-only repo.
b) For a group project, I would create a main branch that is controlled and baselined. When working on
updates to this repo, each team member would create a branch to work off of. They would push their updates
to this branch, and they would create a pull request before merging into the main branch. The pull request
would be reviewed by the team before merging. For individual assignments, I would create a single working 
branch off of the main repo to make updates. I don't have to worry about conflicting updates, so I can
merge this branch to the main without issue. For reference materials, I would keep them in a standalone repo
, so I can pull when needed and not worry about mixing working material into it.
Commit Messages and History:
a) The second message is more useful. It details what the commit includes, so that you can easily know
what you did in the commit without having to look at the work the changed. It makes it easy when you're
looking for a specific commit in the future. In the example provided, I might want to review the information
added for Git workflow and repository structure, I could easily find the commit and see exactly what portion
of hw3a was added those two topics. I would not have to review the entire document, it would show exactly
what was added for that commit.
b) There are a few different situations where I'd want to commit to the repository. If the first task
of the project was to parse a file, I would commit after successfully completing parsing portion of the code. 
I would repeat commits for every task of the project. I would essentially commit each time a task of the 
project was complete. I also don't want to commit multiple functionalities with one commit. It's best to break those up.
I'd be sure to commit before redoing some work that was already completed and working. Another possible scenario
that I could see needing to commit is to allow a group member to pick up where I left off a task, but this would 
need to be on a isolated branch, because it would leave the code in a non-working state.
### Graduate Questions
The Three-Stage Model:
a) It is valuable to commit the setup of the repo, before starting the solution. If you commit them all together,
you lose the initial state of the repo. Since they were committed separately, we can always revert to the initial state. 
b) I would commit the finished tasks, so I would commit the code to load data, the typo fix, and the README update.
I would wait to commit the half-finished code. This is because all of the finished items are indpendent and complete
updates. The half-finished code could likely leave the project in a broken state, so I would not commit it. Staging
allows you to commit these all individually even if working on them all at the same time. You can stage and commit
one at a time.
c) Git status shows you which files have been modified, so you can stage only the files you want to commit at that time.
You can identify the files that have been modified for the completed task, stage those related files, and commit them.
You should really use this all the time while working, but especially in the working directory staging area stages.
Local vs. Remote Repositories:
a) It means you have a copy of the full repositories on your local machine along with all the associated data from
the repo. Unlike Google Drive, you have everything locally that is on the server. In Google Drive, you just sync your
work to the server, but if you lose internet, you lose the ability to see the file history or to sync. Git allows you
to see the file history locally without internet. You can also commit without internet, you just cannot push until you
connect.
b) It allows for a offline workflow. If you are working on the go and have no internet access, you can continue to commit
and all the history is saved locally. Once you are back online, you can push everything and all that history will be synced
to the server. It also allows you to make various updates and commits locally to try to fix a bug. Instead of it automatically
syncing all these small commits, once you reach a solution you can "squash" the commits together before pushing. This enables 
you to have one clean commit to the repo.
c) Git clone copies the entire remote repository onto your local machine. Git pull grabs the latest changes to the remote repo
and updates your local repo with the updates. Git push takes your local changes to the repo and uploads them to the remote repo.
You can pull from the class_repo, because you have read permissions to it but not write permissions. You have read and write
permissions to my_repo.
Professional Portfolio:
a) You should consider whether what you are commiting a complete unit of work. It may not be perfect, but it is a complete
idea and doesn't break the project. Individual updates that fix and clean up this unit can also be committed. For example,
you can commit a "completed intial parsing functionality of sample.csv" and separate commits for "added additional comments
to parsing code" and "fixed bug in parsing code".
b) The README.md for a portfolio repo would be more geared towards showing what you're capable of and showing off your work.
The README.md for a open-source project would explain what the code in the repo is and describe how the user can utilize it.
The key difference is the portfolio is aimed to show off the developer and the open-source is meant to be an instruction
manual.
C) It is more valuable to create during coursework, because it can be used to show years of proof of your work and skill development. It
can be used in addition to your resume to grab recruiters attention and get job interviews. It provides more value than just a resume
alone. Good habits would be creating useful READMEs, comments, and practice good commit habits with useful descriptions, so when you 
revisit your work in the future, it makes sense to you. You can look back at past work to understand how you solved a problem and see 
individual commits for each step of the way.

