1) An .md file is a plain-text document created using the Markdown 
    language. Unlike a standard .txt file, it uses simple text symbols to indicate formatting like headers, bold text, and lists 

2) To show the hidden folders:
    ls -la 
    eg- will show the '.git' hidden folder

3) Flow of Git: 
   Write -> add -> commit

4) Git flow
   ![alt text](<Git Flow.png>) 
   refer the git_flow.png image

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

19) git merge --abort : will abort the merging of the braches.

20) git stash: 
    it is a Git feature used to temporarily save your uncommitted changes without committing them.
    It is useful when:
         You are working on something
         Suddenly need to switch branches or pull latest code
         But your current work is incomplete and you don’t want to commit it yet
    Flow: So after doing the git stash 
         Do other work, switch branches, pull code, fix bugs, etc. 

    Bring your changes back
                  | Command           | What it does                                  |
         | ----------------- | --------------------------------------------- |
         | `git stash apply` | Restores stash but keeps copy in stash list   |
         | `git stash pop`   | Restores stash and deletes it from stash list |
     
21) git rebase master(branch you want to rebase) : 
      It re-writes the history of commit messgaes/flow. 
      It helps to re-allign the base.

      suppsose you created a feature_branch from the master. You continue to do the changes in the feature
      branch, but someone made some changes in the master branch itself. So, in that case, you would want to
      have those as well. Here, realligning the base would help.

22) git reflog : 
      This will show you the history of the commits.

23) git reset --hard <commit-id/commit-hash> :
      This will reset and take up to the point of commit for which commit-id is shared.
      After doing this, the already further commits happended after the shared <commit-id> will not exit. 

24) git push origin main : 
    use to push the repo changes to Github Repo