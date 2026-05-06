 Git is a version control system that allows you to track changes to your files and collaborate with others
 It is used to manage the history of your code and to merge changes from different branches.

 
 *Git and Github are different*
 Git is a version control system that is used to track changes to your files. It is a free and open-source software that is available for Windows, macOS, and Linux. Remember, GIT is a software and can be installed on your computer.

 Github is a web-based hosting service for Git repositories.
 Github is an online platform that allows you to store and share your code with others. It is a popular platform for developers to collaborate on projects and to share code. 

 *version control systems*
 Version control systems are used to manage the history of your code. 
 They allow you to track changes to your files and to collaborate with others.
Version control systems are essential for software development. Consider version control as a checkpoint in game. You can move to any time in the game and you can always go back to the previous checkpoint. 

Before Git became mainstream, version control systems were used by developers to manage their code. They were called SCCS (Source Code Control System). SCCS was a proprietary software that was used to manage the history of code. It was expensive and not very user-friendly. Git was created to replace SCCS and to make version control more accessible and user-friendly. 

Check your git version
To check your git version, you can run the following command:

Terminal window
git --version (display the version of git installed on your system. Git is a very stable software and don’t get any breaking changes)

you can run the following command to see the current state of your repository:

Terminal window
git status

![alt text](image.png)

Your config settings

You can change your username, email, and other settings. Whenever you checkpoint your changes, git will add some information about your such as your username and email to the commit. There is a git config file that stores all the settings that you have changed.

git config --global user.email "your-email@example.com"
git config --global user.name "Your Name"

 check your config settings:

Terminal window
git config --list

This will show you all the settings that you have changed.



git status
git init

git status command will show you the current state of your repository. git init command will create a new folder on your system and initialize it as a git repository. This adds a hidden .git folder to your project.

Commit
commit is a way to save your changes to your repository. It is a way to record your changes and make them permanent. You can think of a commit as a snapshot of your code at a particular point in time. When you commit your changes, you are telling git to save them in a permanent way. This way, you can always go back to that point in time and see what you changed.
![alt text](image-1.png)

![alt text](image-2.png)

When you want to track a new folder, you first use init command to create a new repository. Then you can use add command to add the folder to the repository. After that you can use commit command to save the changes. Finally you can use push command to push the changes to github. 

Stage
Stage is a way to tell git to track a particular file or folder. You can use the following command to stage a file:

Terminal window
git init
git add <file> <file2>
git status

Here we are initializing the repository and adding a file to the repository. Then we can see that the file is now being tracked by git. Currently our files are in staging area, this means that we have not yet committed the changes but are ready to be committed.

Commit
Terminal window
git commit -m "commit message"
git status

Here we are committing the changes to the repository. We can see that the changes are now committed to the repository. The -m flag is used to add a message to the commit. This message is a short description of the changes that were made. You can use this message to remember what the changes were. Missing the -m flag will result in an action that opens your default settings editor, which is usually VIM.

Logs
Terminal window
git log

This command will show you the history of your repository. It will show you all the commits that were made to the repository. You can use the --oneline flag to show only the commit message. This will make the output more compact and easier to read.

☕️ - Check git log docs

Atomic commits are a way to make sure that each commit is a self-contained unit of work. This means that if one commit fails, you can always go back to a previous commit and fix the issue. This is important for maintaining a clean and organized history in your repository.

change default code editor
You can change the default code editor in your system to vscode. To do this, you can use the following command:

Terminal window
git config --global core.editor "code --wait"

gitignore
Gitignore is a file that tells git which files and folders to ignore. It is a way to prevent git from tracking certain files or folders. You can create a gitignore file and add list of files and folders to ignore by using the following command:

Example:

.gitignore
node_modules
.env
.vscode

Now, when you run the git status command, it will not show the node_modules and .vscode folders as being tracked by git.














