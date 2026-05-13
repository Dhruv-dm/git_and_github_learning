1) An .md file is a plain-text document created using the Markdown 
    language. Unlike a standard .txt file, it uses simple text symbols to indicate formatting like headers, bold text, and lists 

2) To show the hidden folders:
    ls -la 
    eg- will show the '.git' hidden folder

3) Flow of Git: 
   Write -> add -> commit

4) Git flow
   ![alt text](<Git Flow.png>)

5) Taking the file to the staging area after doing the changes:
   git add <file name> 
    or
   git add .   (# To select all the changed file in one go)

6) To commit the file
   git commit -m "type the message"

7) Flags: 
   --version, --oneline  
   these are called flags in git

8) git log:
   this command will give the complete log of the commits happened and who did these commits
   
   git log --oneline
   will provide mail commit message detials

9) git commit sentence, usually method:
   give instruction to the code(the code change that is being performed), what it needs to perform
   {Present Tense, imperative}
   eg- fix: update the datatype for sales_amt

10) To Set VS Code as Git Default Editor
    git config --global core.editor "code --wait"
    The --wait flag is important because it tells Git to wait until you close the file before continuing the Git operation (like commit message editing).

11) .gitignore file:
    Place the files are the required not to track by git.
    eg- I put the ignore_file in the .gitignore file, so it will not be tracked by git

12) .gitkeep file:
    Usually git does not keep the track of an empty folder, this file can be placed under that empty folder, so that git could keep a track. 

13) git branch : will provide the current branch name
14) git branch <new_branch_name> : will create a new branch
15) git switch <branch_name> : will switch to other branch
16) git switch -c <new_branch_name> : will create a new branch and automtically switch to this new branch.
17) git checkout <other_branch_name> : will switch to the other branch

18) merging the changes from feature_branch to master/any other branch:
    make the feaute_branch updated
    switch to master branch: git checkout master
    merging the changes: git merge <feature_branch>