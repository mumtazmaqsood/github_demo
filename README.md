# github_demo


#Make sure git is tracking your project.
    1- Using your terminal/command line, get inside the folder where your project files are kept: cd /path/to/my/codebase.
    You cannot do this simply by opening the folder normally, you must do this with the command line/terminal.
    
    Do you need a refresher on using your command line/terminal? I've compiled my favorite resources here.
    
    2 - Check if git is already initialized: git status
    If you get this error message: fatal: Not a git repository (or any of the parent directories): .git, that means the folder you are currently in is not being tracked by git. In that case, initialize git inside your project folder by typing git init, then going through the process of adding and committing your project.
    
    If you get another error message, read carefully what it says. Is it saying git isn't installed on your computer by saying that the word 'git' is not recognized? Is it saying that you're already in a folder or sub-folder where git is initialized? Google your error and/or output to understand it, and to figure out how to fix it.
    
    Do you need a refresher on git? Go through Codecademy's git course.

#Create a remote, empty folder/repository on Github.
    1 - Login to your Github account.
    
    2 - At the top right of any Github page, you should see a '+' icon. Click that, then select 'New Repository'.
    
    3 - Give your repository a name--ideally the same name as your local project. If I'm building a travel application,
     its folder will be called 'travel-app' on my computer, and 'travel-app' will be the Github repository name as well.
    
    4 - Click 'Create Repository'. The next screen you see will be important, so don't close it.

#Connect your local project folder to your empty folder/repository on Github.
    The screen you should be seeing now on Github is titled 'Quick setup — if you’ve done this kind of thing before'.
    Copy the link in the input right beneath the title, it should look something like this: https://github.com/mindplace/test-
    repo.git This is the web address that your local folder will use to push its contents to the remote folder on Github.
    
    1 - Go back to your project in the terminal/command line.
    
    2 - In your terminal/command line, type git remote add origin [copied web address]
    
    Example: git remote add origin https://github.com/mindplace/test-repo.git
    
    3 - Push your branch to Github: git push origin master
    
    4 - Go back to the folder/repository screen on Github that you just left, and refresh it. The title 'Quick setup — 
    if you’ve done this kind of thing before' should disappear, and you should see your files there.


    #ERROR HANDLING
    ! [rejected] master -> master (fetch first)
    error: failed to push some refs to 'https://github.com/manojkumarhcm9/test-repo.git'
    hint: Updates were rejected because the remote contains work that you do
    hint: not have locally. This is usually caused by another repository pushing
    hint: to the same ref. You may want to first integrate the remote changes
    hint: (e.g., 'git pull ...') before pushing again.
    hint: See the 'Note about fast-forwards' in 'git push --help' for details.


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
    
    
#The “fatal: refusing to merge unrelated histories” Git error
    SOLUTION
    The error is resolved by toggling the allow-unrelated-histories switch. 
    After a git pull or git merge command, add the following tag:

        git pull origin master --allow-unrelated-histories

