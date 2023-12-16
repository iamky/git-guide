# git-guide
A basic git guide for install and use


//INSTALL
git on mac $ brew install git

//LOGIN
git config --global user.name "github username goes here"
git config --global user.email "github email goes here"

//SSH KEY SETUP

 //Check for SSH key
 ls ~/.ssh

 //Create an SSH key
 ssh-keygen -t rsa -b 4096 -C "github email goes here"    //Go for default values on prompts

 //Copy the SSH key   // if you have a key make sure to use the file name of .pub file instead of id_rsa
 
 MacOS    pbcopy < ~/.ssh/id_rsa.pub
 Windows  clip < ~/.ssh/id_rsa.pub
 Linux    sudo apt-get install xclip , xclip -sel clip < ~/.ssh/id_rsa.pub

 //GitHub settings setup
   Open GitHub settings 
   Find SSH and GPG settings
   Add a TITLE and new key by pasting it from clipboard SELECT it as "Authentication Key"

//Test the setup using 
ssh -T git@github.com

//GIT and GitHub are now SETUP


FOR USING GIT BY COMMAND LINE AFTER SETUP

//Initialize 
git init (Adds .git folder to the project)

//Clone 
git clone ssh-url (Use SSH url not the HTTP Adds.git folder and Adds Remote)

// Start 
 //Go to GitHub start a new repo add readme (README helps for guide and notes)
 
 //USE CLONE with SSH 
 
 //Open terminal in the folder you want to start and use git clone command

 //Open the folder in vs code {vs code integrates with github}
  //Make a new file
  
  //The file will turn green with a U (Untracked) next to it
  
  //Use git add filename.txt in terminal {the U will change to A which means the file is added to index}

  // Use git commit -m "MESSAGE GOES HERE" {the green color will be removed because the file is now tracked by git}

  //After adding some content in the file the filename will turn into orange color with M(Modified) which means its a different version than git right now 

  //To see the difference use git diff command 


  //Use git add . command to add every file 
  //Use git commit -m "Message"

  //In order to get the changes in repo on github 
  
  //Use git push command this will push it to our remote repo on github

  
  
  
  //BRANCHES

  
  // USE git checkout -b BRANCH_NAME
  //git push --set-upstream origin BRANCH_NAME {To setup branch on github}

  // To show these changes on master branch
  
   // git checkout master {switches us to main branch}
   // git status {To check current branch}

   //MERGE
     //git merge {merges side branch in main branch}

   //MERGE CONFLICT {Purple C(conflict) on side with name}
   <<<<<<HEAD IS CURRENT CHANGE
   ======
   UPCOMING CHANGE>>>>>>>

   //RECLONE TO SIMULATE A TEAM
   //use clone command 

   // git pull command for updating local repo from remote repo






//SUMMARY

git init
git clone ssh-url
git add filename.txt
git add .
git commit -m "MESSAGE GOES HERE"
git push
git checkout -b BRANCH_NAME
git push --set-upstream origin BRANCH_NAME
git checkout master
git status
git merge
git pull
