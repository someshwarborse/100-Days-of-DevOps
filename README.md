# Day 5: Hands-on Git Project  

## 🔹 Overview  
Today, I worked on a hands-on Git project covering repository creation, branching, merging, and pushing changes to GitHub.  

## 🔹 Steps Performed  
1️⃣ **Initialized a Git repository** using `git init`.  
2️⃣ **Created and modified files** (`README.md` and `script.sh`).  
3️⃣ **Worked with branches** (`feature-branch`, `bugfix-branch`).  
4️⃣ **Merged branches into main** while handling conflicts.  
5️⃣ **Pushed changes to GitHub** and verified updates.  

## 🔹 Commands Used  
```bash
# Initialize Git
git init

# Check repository status
git status

# Create a new branch
git checkout -b feature-branch

# Stage & commit changes
git add .
git commit -m "Added new feature"

# Merge branch into main
git checkout main
git merge feature-branch

# Push changes to GitHub
git push origin main

