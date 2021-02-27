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

![CreateGitBranch3](https://github.com/prakashgkhaire/BDMAssessment/blob/Integration/Images/5_2.png)

`$ git checkout -b Feature1`

`$ git checkout -b Feature2`
