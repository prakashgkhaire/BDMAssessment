# Branching Development Model

### DESCRIPTION

Create a branching model to help your team understand the Git Feature Branch Workflow for faster and efficient integration of work

# Background of the problem statement:

<p align="justify">M-theta Technology Solutions hired you as a DevOps Architect. It is undergoing an infrastructural change to implement DevOps to develop and deliver the products. Since M-theta is an Agile organization, they follow the Scrum methodology to develop the projects incrementally. Hence, the company wants to adopt Git as a Source Code Management (SCM) tool for faster integration of work and smooth transition into DevOps.</p>

<p align="justify">So, as a DevOps Architect, you have been asked to build a branching model to demonstrate the Git Feature Branch Workflow for the company’s engineering team. In the branching model, you are required to create a Production branch which will act as the main (master) branch, an Integration branch which will again have two branches inside it namely Feature 1 and Feature 2, and a Hotfix branch which will be used for fixing any issues that could come up from Integration or Production branches.</p>

![CreateGitDirectory](https://github.com/prakashgkhaire/BDMAssessment/blob/Integration/Images/BranchModel.png) 

# SOLUTION

## Steps to perform:

First of all create a repository on your local machine and initialize it with git as shown in below image.

![CreateGitDirectory](https://github.com/prakashgkhaire/BDMAssessment/blob/Integration/Images/1.png)

`$ mkdir BDMAssessment`<br>

`$ cd BDMAssesment` <br>

`$ git init` <br>

After creating the `BDMAssessment` git repository, its time to create a `README.md` to add the text contents.

![CreateGitDirectory](https://github.com/prakashgkhaire/BDMAssessment/blob/Integration/Images/2.png)

`$ touch README.md` <br>

`$ git add README.md`

Now it is time to commit the work

![CreateGitDirectory](https://github.com/prakashgkhaire/BDMAssessment/blob/Integration/Images/3.png)

`$ git commit -m "first commit"`

### A. Start with the Production branch (master branch), and then create a HotFix  and Integration branch

![CreateGitBranch1](https://github.com/prakashgkhaire/BDMAssessment/blob/Integration/Images/4.png)

`$ git branch -M production`

`$ git branch -a`

![CreateGitBranch2](https://github.com/prakashgkhaire/BDMAssessment/blob/Integration/Images/5_1.png)

`$ git checkout -b HotFix`

`$ git checkout -b Integration`

### B. Subsequently, create Feature 1 and 2 branches that integrate to the Integration branch as shown in the above figure

![CreateGitBranch3](https://github.com/prakashgkhaire/BDMAssessment/blob/Integration/Images/5_2.png)

`$ git checkout -b Feature1`

`$ git checkout -b Feature2`

![CreateGitBranch3](https://github.com/prakashgkhaire/BDMAssessment/blob/Integration/Images/7.png)

`$ git checkout Feature2`

`$ touch main.py`

`$ vi main.py`

`$ cat main.py`

`git add main.py`

`git commit -m 'Added main.py'`

`git push --set-upstream origin Feature2`

### C. Commit some changes in the Feature 2 branch and merge it into the Integration branch. Delete this branch once merging is complete

![CreateGitBranch3](https://github.com/prakashgkhaire/BDMAssessment/blob/Integration/Images/8.png)

`$ git checkout Integration`

`$ git merge Feature2`

![CreateGitBranch3](https://github.com/prakashgkhaire/BDMAssessment/blob/Integration/Images/9.png)

`$ git checkout Feature1`

`$ vi logging.py`

`$ cat logging.py`

`$ git add logging.py`

`$ git commit -m 'Added file for basic logging`

`$ git push --set-upstream origin Feature1`

![CreateGitBranch3](https://github.com/prakashgkhaire/BDMAssessment/blob/Integration/Images/10.png)

`$ git checkout Integration`

`$ git checkout Feature1`

`$ vi auth.py`

`$ cat auth.py`

`$ git add auth.py`

`$ git commit -m 'Added JWT auth File'`

### D. Commit some changes in the Feature 1 branch and rebase it to the Integration branch

![CreateGitBranch3](https://github.com/prakashgkhaire/BDMAssessment/blob/Integration/Images/11.png)

`$ git checkout Integration`

`$ git merge Feature1`

### E. Merge the Integration branch into Hotfix and Production branch to update these branches

![CreateGitBranch3](https://github.com/prakashgkhaire/BDMAssessment/blob/Integration/Images/12.png)

`$ ls -l`

`$ git status`

`$ git add Images`

`$ git commit - 'Add Command Screenshots'`

`$ git branch`

`$ git push origin Integration`

### F. Commit some changes in Feature 1 branch, and then merge it into Integration, Hotfix, and Production branch. Delete this branch once merging is complete

![CreateGitBranch3](https://github.com/prakashgkhaire/BDMAssessment/blob/Integration/Images/12.png)

`$ ls -l`

`$ git status`

`$ git add Images`

`$ git commit - 'Add Command Screenshots'`

`$ git branch`

`$ git push origin Integration`

![CreateGitBranch3](https://github.com/prakashgkhaire/BDMAssessment/blob/Integration/Images/13.png)

`$ git branch -D Feature1`

`$ git checkout HotFix`

`$ vi logging.py`

### G. Commit some changes in the Hotfix branch and merge it into the Production as well as the Integration branch

![CreateGitBranch3](https://github.com/prakashgkhaire/BDMAssessment/blob/Integration/Images/14.png)

`$ git add logging.py`

`$ git push --set-upstream origin Hotfix`

![CreateGitBranch3](https://github.com/prakashgkhaire/BDMAssessment/blob/Integration/Images/15.png)

`$ git branch`

`$ git checkout production`

`$ git branch`

![CreateGitBranch3](https://github.com/prakashgkhaire/BDMAssessment/blob/Integration/Images/16.png)

`$ git stash`

`$ git checkout Production`

`$ git branch`

`$ git checkout production`

`$ git merge HotFix`

![CreateGitBranch3](https://github.com/prakashgkhaire/BDMAssessment/blob/Integration/Images/17.png)

`$  git branch`

`$ git checkout Integration`

`$ git merge HotFix`


