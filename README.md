basic commands of git 

some descriptions

###subheader

git clone ssh key 

git status...to check the status ..like modified,untracked file

git add .
the above to add all the changes..once donne u can check it using 
git status 

then
git commit -m"added fe commands" -m"some description"

here m is message ..here we gave it twice because one is for heading and another for description ..the thing in quote are the message 

now still we have saved everything locally and not on github yet to make it live we should use git push

to push this we have to tell github that we are the owner of the account 

so to this we have to connect our local machine to github anyhow and this is done by using ssh key

so to do this we hav eto generatte the ssh key 

ssh-keygen -t rsa -b 4096 -C"bsanjanamdival@gmail.com"

-t ..type of encryption

in git bash 
HP@sanjana MINGW64 ~/Desktop/Git/gitworkshop (main)
$ ls | grep testkey
testkey
testkey.pub

HP@sanjana MINGW64 ~/Desktop/Git/gitworkshop (main)
$ ssh-add ./testkey
Identity added: ./testkey (bsanjanamdival@gmail.com)

HP@sanjana MINGW64 ~/Desktop/Git/gitworkshop (main)
$ ssh-add -l
4096 SHA256:NQK/KJwZ2IWWV4/Afqp+uUNvRYlE6KxXD3MS8UlDEK4 bsanjanamdival@gmail.com (RSA)

HP@sanjana MINGW64 ~/Desktop/Git/gitworkshop (main)
$ ssh -T git@github.com
Hi sanjanamadival! You've successfully authenticated, but GitHub does not provide shell access.

HP@sanjana MINGW64 ~/Desktop/Git/gitworkshop (main)
$


now in terminal to push 
git push origin main
so here main is the branch name

see now whwne i add few things again i should save it na and push so 
git add .
git commit -m"added changes"
git push origin main


braches
Feature Branches are used for regular development....master or main branch
Once a feature is ready, it is merged into the Master Branch after review and testing.....feature branch
If an urgent problem occurs in the live app, a Hotfix Branch is created, fixed, and merged back into the Master Branch.....hot fix branch



git branch 
git checkout -b feature-readme-instruction
git checkout to switch the branch and -b to create a branch and thengive branch name 


if u want to switch back then just give
git checkout main

now currently i m in main branch 
here i m checking this with feature branch 
git diff 
to check the chagnes made between 2 files 

now push this new branch 

to merge 2 branch 
git merge feature-readme-instruction 
general syntX 
git merge branch_name

to delete the merged branch 
git branch -d branch_name


git conflict ..happpens when multiple peoples try to do changes 

