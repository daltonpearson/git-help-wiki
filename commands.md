
# Git Commands

<b>Command 1:</b>
```
git status
```

<b>Definition:</b> 
- This command allows you to view which files have been modified, shows you which branch you are currently on, and if you have added any files to the queue on your local machine. 
- If the file names are <b>RED</b>, this means that there have been changes made to the files in <b>RED</b> but <b>HAVE NOT</b> been added to the queue. 
- If the file names are <b>GREEN</b>, this means that there have been changes made to the files in <b>GREEN</b> but <b>HAVE</b> been added to the queue.

<b>Command 2:</b>
```
git checkout -b branchName
```

<b>Definition:</b>
- This command will create a new branch off of the branch you are currently on. It is best practice to only create a new branch when you are currently on the "master" branch. This is to avoid pushing old code to the repository.
- If you simply want to move from branch to branch you can issue the command "git checkout branchName" without the "-b" parameter to move from branch to branch. 

<b>Command 3:</b>
```
git add . 
```

<b>Definition:</b>
- This command will add all of the files to the queue on your local machine to indicate to Git that these are the files that you want to commit changes to.
- If you want to add a single file you can simply replace the dot with the file name. Example: git add index.php

<b>Note:</b> If you want to see which files have been added to the queue you can simply use "git status" to see which files have or have not been added to the queue.

<b>Command 4:</b>
```
git commit -m "Your Message"
```

<b>Definition:</b>
- This command will commit any changes you have made to any files that have been added to the queue on your local machine. 
- The -m parameter indicates that you want to attach a message to this specific commit and in quotes you can attach your message.

<b>Command 5:</b>
```
git push -u origin branchName
```

<b>Definition:</b>
- This command will push any files you have committed on your local machine to the remote repository on Git.
- The "-u" parameter is only needed when you have created a new branch with Git on your local machine. This is because the remote repository doesn't know which branch you are referring to when it has just been created on your local machine.
- The "origin" parameter tells Git that you want to send your local changes to the remote repository named origin. This is the default name for any repository created and Git and most likely will not be changed.
- The "branchName" parameter is to tell Git which branch you want to push to the server.

<b>Note:</b> The only time you need to include the parameters "-u", "origin" and "branchName" are when you first push your newly created local branch to the remote repository. Once you have done this once you simply just need to checkout to the branch you want to push and enter "git push".

<b>Command 6:</b>
```
git pull
```

<b>Definition:</b>
- This command will pull all of the code for the specific branch that you are on from the remote repository and onto your local machine and merge the two together.
- It is good practice that once you are done working on one branch and would like to get the code from the "master" branch on the remote repository you first checkout to the "master" branch and issue "git pull" to update your local repository.


## A Typical Scenario On How You Will Use All Of These Commands:

<b>Scenario:</b> Your current machine has the Git repository cloned in and are you are all set up locally. Now you want to edit some code files.

<b>Step 1:</b> Make sure you are on master branch by either checking the status to see which branch you are on or just simply checkout to the master branch by issuing:
```
git checkout master
```

<b>Step 2:</b> Make sure you are up to date with the most recent code from the remote repository before you make any changes by issuing:
```
git pull
```

<b>Step 3:</b> Check out a new branch by issuing:
```
git checkout -b branchName
```

<b>Step 4:</b> Make changes to your code file. Once you are happy with the changes you made you can add the file(s) to the queue by issuing:
```
git add .
OR
git add fileName.php
```

<b>Step 5:</b> Commit your changes to your local machine by issuing:
```
git commit -m "Descriptive and awesomely informative commit message here."
```

<b>Step 6:</b> Push your changes to the remote repository:
```
git push -u origin branchName
```

<b>Step 7:</b> If you are not done with the current branch you are on, you can continue working on that same branch. If you want to push more changes simply repeat steps 4 - 5 and instead of the command in Step 6 you can issue this instead:
```
git push
```

<b>Step 8:</b> If you are done with the branch you are currently working on and would like to work on a new feature and a new branch simply start this process over from Step 1.