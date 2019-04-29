# Stephanie Kitchen
Blog of my learning surrounding Git and GitHub, and CLI basics

## :one: CLI Commands
I learnt the following commands to navigate using only the Command Line

* $ cd  
  * *To navigate to the home directory*
* $ ls
  * *To list all the files within that directory*
* $ cd source/foo
  * *To go into an already created project folder*
  * *That by pressing the Tab, one can shortcut tp the names of the files*

* $ cd ..
  * *Moves up one directory*
* $ cd -
  * *Goes back to the previous location*

* $ ls
  * *List current contents of the directory*
  
* $ mkdir "folder name"
* $ mkdir FolderName
* $ mkdir /c/Users/StephanieK/source/FolderName
  * *make-directory first, can make within the directory or give the full name of desired directory*

* $ pwd
  * *Prints the name of the working directory*
  

## :two: Git
To begin, I downloaded __Git Bash__ and learnt the following commands to add files and directories from the command line:

* $ git add dummydocument.txt
  * *Added a .txt file that was created in the folder*
* $ git status
  * *Would show everything that was modified and not yet into the __Staging Area__*
* $ git add .
* $ git add dummydocument.txt
  * *That one can either add the specific file or all files, depending on need, from the working directory to the __Staging Area__*
  
* $ git mv
  * *Moves or renames a file or directory*
* $ git rm
  * *Removes the file from the working directory and the index*
  
* $ git commit -am "Commit message here"
* $ git commit -i dummydocument.txt -m "Commit message here for specific file"
  * *Commits all files or includes a specific file, with the commit message which should contain a relevant concise message of what that commit entailed, and commits this to the __Local Repository__*
* $ git log
  * *Prints out all the commits previously done before now with the author, date and message from each commit*

Other commands that were useful to learn were that if I typed:
* $ git --help
* $ git add -h
* $ git commit -h

These were particularly useful in order to list some of the common Git commands and options, as well as decriptions for how these worked

## :three: Dotnet CLI
To begin, I downloaded **.NET** as the platform to build my apps

The initial commands I learnt were to create a new Console App for my katas:

* $ dotnet -h
  * *Gave a list of all the commands and options for .Net Core SDK*

Once a directory was made, to go within that new directory before the next step
  
* $ dotnet new -h
  * *Gives a list of the templates, their short names, langauges and tags*
* $ dotnet new console
  * *Creates a new console app*
* $ code .
  * *Opens the console app in VS Code*

I learnt that after this is created that I should create:
* a .gitignore .txt file to specify the untracked files to ignore
* a README.md file, typically used for giving instructions and additional information about the app

Aside from the Console Application, I also used dotnet to create:
* $ dotnet new sln
  * *Creates a Solution*
* $ dotnet sln SolutionName add PROJECT
  * *Adds a project within the Solution*
  
Add a separate folder for the test files and then within that folder:
* $ dotnet new xunit
  * *Adds a new Xunit Test Project*
* $ dotnet add reference ../MainSolution.csproj
  * *Adds the reference from the current test project to the relevant main solution*

# :four: Git Hub
Initially, I needed to create a GitHub account for the projects and repositories for my apprenticeship katas in order for them to be reviewed by my mentor and other developers.
After creating a GitHub account, I was then able to create a new remote repository.

Using git bash I could then add this to the created Console App on my local directory
* $ git remote ass origin https://github.com/StephanieK94/Kata-4.git
  * *Adds the url of the repository on my GitHub account*
* $ git push -u origin master

Or one could create a new repository on the command line:
* $ echo "# Kata-4" >> README.md
  * *Appends the header "Kata-4" to the file README.md and creates that file if not already there*
* $ git init
  * *Initialises the repository
* $ git add README.md
* $ git commit -m "First commit"
* $ git remote add origin https://github.com/StephanieK94/Kata-4.git
  * *Adds the established github repository*
* $ git push -u origin master
  * *Pushes this upstream to the remote server where it can be pushed to and pulled from*

###### Useage
Once these four things were established and relatively understood it became habit when writing a piece of code to regularly
* $ git status
* $ git add .
* $ git commit -am "Commitment Message"

and then once the that piece of the code was finished to push
* $ git push
