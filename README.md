## 415Project
ECSE415 final project

---
# Project Description:

This is projects attempts to solve the MIO-TCD challenge. The challenge consists of two parts: 
- Classification: A set of ~ 650k images of 11 different objects is provided. The task is to claissify those objects into their respective classes.

- Localization: A set of ~ 140k images of large images that contain several objects is provided. The task is to localize and identify those objects.

- Approach: 

1. Classification: Use HOG descriptiors to train a suppor vector machine (SVM) classifier and a nearest neighbour KNN classifier. 

2. Localization: Train an SVM to distinguish between "Background" and "Non-background or Object". Then use sliding windows of different sizes to classify patches in the image as background or non-background. Run the non-background images through other filters as well until you're left with patches that are only objects. Then classify the objects on those patches using the classifier trained in part 1.

3. Also, deep-learning classifier using Tensorflow was implemented for part 1 (Bonus).

[MIO-TCD Challenge](http://podoce.dinf.usherbrooke.ca/challenge/dataset/)

---

# Git instructions for team members:

**cloning** 

In the terminal/command line, navigate to the folder where you want to store the project files:

`git clone https://github.com/Aljulanda9/415Project.git`

**workflow**

`git pull` to update your local repository with the most recent changes

DO WORK

`git status` to see which files YOU changed

`git add CHANGED_FILES` or `git add .` to add all files (stage files to be committed)

`git commit -m'Descripe the changes/work you want to commit'`

`git push`

In case you edit a piece of code that someone else originally pushed, you might get a conflict which you would have to resolve. Git will ask which version of the code you want to keep (yours or the older one)

**force pull**

Use the following command to overwrite your local files with the files that are in the remote repository. You will lose whatever changes/code that you haven't pushed yet to the remote repository. So be careful.

`git fetch origin master`

`git reset —hard FETCH_HEAD`

`git clean -df`
