# how to learn git from scratch
Reference: https://www.liaoxuefeng.com/wiki/896043488029600  
This is a tutorial to learn the basic commands of git. Three functions of git and github:  
1. remote repository  
2. version control  
3. branch management  

## *Function 1: remote repository* 
###### 1. create reposition without README.md
###### 2. contruct README.md in your file
`echo "# StableAA" >> README.md`
###### (2. set the user information)
`git config --global user.name 'datake'`  
`git config --global user.email 'ajksunke@foxmail.com'`
###### 3. tell git you want to manage current folder 
`git init` 
###### 4. add files to Repository(.git) into "staged" status
`git add . / git add ***`
###### 5. commit files to the working repository (after multiply adding files), from "staged" to "unmodified" status
`git commit -m "log information, e.g., first commit"`
###### 6. connect with your repository, where origin is the default repository name
`git remote add origin 'repository address'`
###### 7. set the branch main
git branch -M main
###### (7. add README.md in your folder, if there already exists a README.md in your repository)
`git pull --rebase origin main`
###### 8. push codes to github, master is our default first branch
`git push -u origin main (first time)`  
`git push origin main (later)` 

## *Function 2: version control* 
###### 1. check the status of current folder (unmodified -> modified -> stages -> unmodified)
`git status`
###### 2. check the difference between unmodified and modified
`git diff ###(file name)`
###### 3. check previous commit versions to find one you'd go back
`git log (--pretty=oneline)`
###### 4. go back to previous version, note that HEAD is the current version, ^ means the last version, ^^ indicates the second last version. HEAD is a pointer, pointing to a specific version
`git reset --hard HEAD^`
`(git reset --hard "commit id(several first numbers is OK)")`
###### 5. check your past command and result to find your past commit id
`git reflog`
###### 6. delete the modification to be commited (to staged or unmodified versions)
`git checkout -- filename`
###### 7. tell git you delete some files, then commit
`git rm ***(file name)`

## *Function 3: branch management* 
###### 1. check all branches
`git branch` 
###### 2. establish and convert to a new branch dev
`git branch dev`  
`git checkout dev`
###### 3. merge branch dev to master
`git checkout master
git merge dev`
###### 4. delete past branch
`git branch -d dev`




Here are two important figures about git.

![Alt text](https://github.com/datake/learn-git/blob/master/git.png)

![Alt text](https://github.com/datake/learn-git/blob/master/branch.png)
