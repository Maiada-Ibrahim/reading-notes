#### **Development**
# Git Tutorial: A Comprehensive Guide
![git](https://www.javacodegeeks.com/wp-content/uploads/2016/08/Git-Tutorial_book.png)
## INTRODUCTION
### efore beginning this tutorial, it is highly recommended that you have a solid understanding of the Terminal (for Mac) or Command Line (for Windows and Linux).In order to explain Git, we have to first explain various aspects of Version Control.
## Version Control
- ### Local Version Control
#### Many years ago, programmers created Local Version Control systems. A Local VCS entails one database on your hard disk that stores changes to files.
- ### Centralized Version Control
#### The need for collaboration within a developer team on a single file or set of files led to the advent of the Centralized Version Control System (CVCS). This system entails a single server storing all changes and file versions, which can be accessed by various clients. This streamlined the collaboration process (by eliminating the need to involve all local databases), allowed programmers to have more knowledge of team members’ activities with certain files, and gave administrators much more control over divvying up revision privileges.
- ### Distributed Version Control
#### A Distributed Version Control systems (DVCS) addresses the major vulnerability of the CVS: the server as a single point of failure. If a CVS goes down, collaborators cannot work with each other on a file or save changes and new versions. Also, in the event of corruption of a central database’s hard disk — with the absence of backups — all work will be lost, except for any portions on local machines.

#### To prevent this type of catastrophic loss, a DVCS allows clients to create mirrored repositories. These data backups can be easily be placed on the server to replace any lost information.
#### Because the DVCS allows for multiple mirrored repositories, programmers working in teams can collaborate with each other in various ways to complete a joint project, which enables the use of various simultaneous workflows.

##  what is Git?
- ### Snapshots
#### Git is a DVCS that stores data in a file system made up of snapshots. Each time you save a changed version of your project — called commit — Git creates a snapshot of the file and stores a reference to it. If the file has not changed, Git only stores a reference to the already-stored identical version of it.
- ### Local Operations
#### Git mostly relies on local operations because most necessary information can be found in local resources. This allows for process expediency because a project’s history resides on the local disk, eliminating the need to fetch history information from the server, and allowing one to continue work on a project even when not online or on a VPN.
- ### Tracking Changes
#### Every single change applied to any file or directory is tracked by Git. And, as the gatekeeper, Git will always detect file corruption or loss of information in transit.
- ### Loss of Data
#### Git is set up to greatly minimize the possibility of irreversible damage to files, such as accidentally lost data. Git makes it extremely difficult for a snapshot of your file that is committed to be lost.
- ### States
#### Files in Git can reside in three main states: committed, modified and staged.
- ### Committed
#### Data is securely stored in a local database
- ### Modified
#### File has been changed but not committed to the database
## Staged
### Flagged a file’s changed version to be committed in the next snapshot
![](https://blog.udemy.com/wp-content/uploads/2015/08/image066.png)
## Setting up a Git Repository
### Importing


1. *Switch to the target project’s directory*

             example :$ cd test (cd = change directory)
2. *Do the change and to prepar it to commit* 

              example : git add .
3. *commit it* 
             
              example: git commit -m 'what you chang'
4. *git push*

              example: git push origin main


## For more information [check here](https://blog.udemy.com/git-tutorial-a-comprehensive-guide/)