Graded Assignment on Git and GitHub Steps performed
Q1
a)Clicked New button on dashboard, provided repo named git_assignment_HeroVired, changed access to private, added a Readme.md file and created repo.

b)Cloned the repository in local machine and created a dev branch by 
git clone https://github.com/MissIshwari/git_assignment_HeroVired.git
git checkout -b dev

c)Added the files to the staging area, committed code for CalculatorPlus.py by below commands
git add .
git commit -m "Adding Calculator code."
Pushed it by below
git push --set-upstream origin dev
Created pull request from dev to main branch from the github ui and created  v1.0.0 tag with release title as Version 1 of the ‘calculator plus app’ on main branch.

d)Added Garima as collaborator

e,f)Created a new branch as feature/sqrt and switched to it by below command and added square root code
git checkout -b feature/sqrt
Added code to staging area, committed and pushed code to remote repo
git add .
git commit -m "Adding Square root code."
git push --set-upstream origin feature/sqrt

g)Switched to dev branch and fixed the bug and committed code to dev branch by below commands
git checkout dev
git add .
git commit -m "Fixed divide issue."
git push
Created a pull request from dev to feature/sqrt branch in the github ui as it also has division functionality. As there were no conflicts the merge was successful from dev to feature/sqrt as feature/sqrt was up to date.

h) Created a pull request to merge square root feature from feature/sqrt to dev branch. 
i)Created a pull request from feature/sqrt branch to dev and selected Garima as the reviewer. After her approval merged the feature square root into dev branch.
j)Tested code into dev branch and merged into main branch with no merge conflicts. Created v2.0.0 release.


Q2
Downloaded git lfs and installed the exe file, and downloaded a 512 mb file from Vodafone site
Created a new branch named lfs
git checkout -b lfs

Placed the zip file into the repo, followed below commands
git lfs install
git lfs track “*.zip”

Added the .gitattributes file and 512MB.zip, committed and pushed them with below commands
git add .gitattributes
git add 512MB.zip
git commit -m "Adding 512MB zip file."
git push --set-upstream origin lfs

Q3
Created a branch named geometry-calculator and created GeometryCalculator.py file with a skeleteon of class and class object, added to staging area, committed and pushed it to remote repo.
git add .
git commit -m "Adding skeleton for geometry calculator."
git push --set-upstream origin geometry-calculator

Created branch feature/circle-area from geometry-calculator in local by
git checkout -b feature/circle-area
Pasted code for calculating area of circle and printing it provided in the question.
Added code to staging area and stashed the code
git add .
git stash save "Added function to find area of circle."
Checked working tree and the added code for calculating area of circle in GeometryCalculator.py is stashed to the staging area.

For Rectangle feature, created feature/rectangle-area branch from geometry-calculator branch 
git checkout geometry-calculator
git checkout -b feature/rectangle-area
Pasted code for calculating area of rectangle and printing it provided in the question.
Added code to staging area and stashed the code
git add .
git stash save "Added function to find area of rectangle."
Checked working tree and the added code for calculating area of rectangle and printing in terminal in GeometryCalculator.py is stashed to the staging area.

Switched back to the feature/circle-area branch, unstashed the code and added the code to invoke the function that calculates the area of circle and prints it, tested it, committed, pushed it.
git checkout feature/circle-area
git stash apply 'stash@{1}'
git add .
git commit -m "Completed area of circle functionality."
git push --set-upstream origin feature/circle-area

Switched back to the feature/rectangle-area branch, unstashed the code and added the code to invoke the function that calculates and prints the area of rectangle and prints it,tested it , committed and pushed it to remote.
git checkout feature/rectangle-area
git stash apply 'stash@{0}'
git add .
git commit -m "Completed area of rectangle feature."
git push --set-upstream origin feature/rectangle-area

Created pull request from feature/circle-area into geometry-calculator and merged without conflicts on GitHub ui.
Created pull request from feature/rectangle-area into geometry-calculator and resolved conflicts manually through the github file editor and merged the branches.

Created a pull request from geometry-calculator branch to dev and added Garima for review, merged code automatically as there were no conflicts.
Created a pull request from dev to main branch and merged the code.

Edited README.md on main branch and pulled it to all branches, so that there is no dissimilarity of the file when working on other branches and overwriting it. 
