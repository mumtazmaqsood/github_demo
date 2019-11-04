# github_demo

#This file contain git commands 

    1- make dir --
            mkdir dirname
    
    2- make file --
                Touch filename 
     
    3- git status --- check a status of git 
     
    4- git init
    
    5- git add filename
    
    6- git commit -m "wirte comments about git"
    
    7- git add -p , --> use to add modified file ,
     same like git add , git add use for first time to 
     add file while git add -p use after modification.
     
     
     ---git log --> use to view logs 
     
     
     8- git checkout commit-no --> it is handy command becareful while using
     , it reverse the code to back state

#GITHUB 
    
    git clone use to attach with dir on github and download or upload code on that dir
        git clone path of github dir
        
        Example:
         git clone https://github.com/mumtazmaqsood/misknursery1.git
         
         above command will clone the dir , we can add or remove code , 
         do the same if you need to modified the cloned file
         after changin do the below steps
            
            1- git status
            2- git add -p
            3- git commit -m "add msg"
            4- git push origin master (this command push code into cloned dir)
    
#Git Pull
    If multiple developer working with same dir and push their codes as well. then
    git pull command help to get the updated code on our local machine
    
        git pull origin master 
     
#Branches

        To check how many branches it has 
            $ git branch
            
        To change from one branch to another 
            $ git checkout  branch-name 
         
        To make new branch and switch to new branch
            $ git checkout -b my_branch
        
        To merge branches (move to mastar branch and then merge it) 
            $ git merge 2nd_branch
         
#Resoloving Conflicts
        
        Let suppose two deveolopers are working with same code file , when they commit
        their code , it will create conflict
        and message come like that
        
        $ git merge 2nd_branch
        Auto-merging 2ndfile.txt
        CONFLICT (content): Merge conflict in 2ndfile.txt
        Automatic merge failed; fix conflicts and then commit the result.  
        
        resolove
            open file and remove comments from master and 2nd branches
            git add filename
            git commit  (without writing -m)
                it will open in editor , review it and save it , it will open in 
                vim editor , command to save and quit :wq
        
        # Blame command: will show to who work with the file last time
        $ git blame 2ndfile.txt
        
#Ignore Files
    
    make a file with name ".gitignore" and write file name inside this file which 
    need to be ignore 
    
       $ touch .gitignore 

#git Stash 

    If there is piece of code is not ready to commit and developer need to change
    branch , and don't want to commit code , there is stash command can be use, 
    and stash pop command can retrive code again and commit it 
 
        
     $ git stash
        Saved working directory and index state WIP on master: cf69f1e ignore file
     $ git stash pop

        
    this code is written in 2nd_branch

