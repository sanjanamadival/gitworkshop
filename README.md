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