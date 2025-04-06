# DevOps Lab 03
This is lab 4 below.

1- Create a local git repo. create two files in it. 
   write some lines in the both files and commit changes
   now write some lines again in both files and add changes to staging area for only one file
   now use diff command to check difference for both files

2- Use VS code and check differences between both files


3- Perform Lab on Git Lecture 2 Slide 15

4- Perform Lab on Git Lecture 2 Slide 16 

5- Create a new local git repo. Create file1 and add some lines in it. Commit it to the local repo
   Now add a new line in file1 and commit changes. 
   Now create file2 with few lines and commit it
   Now create file3 with lines. Also add another lines in both file1 and file2 and commit changes. 
   Now revert file1 to the commit 2 
   after reverting file1 delete the latest commit. clear the working directing, untracked area but stash unstage area

6- Connect local repo to the remote repo

7- Implement Branch Policy to any branch and run the whole git cycle. 

8- Fork any repo with only main branch and clone it to your machine
   create a new branch form the main branch
   create a new file with some lines and commit it. 
   create a PR to merge copy repos temp-main branch to original repo main branch. 
   after merging the PR sync the copy repo main branch both locally and remotely 

9- Create a new remote repo. 
   create a file and commit it to main branch. 
   create temp1 and temp2 branches from main branch. 
   write line1 in file and commit it to temp1 branch. create PR for main branch and merge it
   replace line1 with line2 in file and commit it to temp2 branch. create PR for main branch and merge it. 
   if you merge conflict on merging the PR you need to abandon your PR. 
   delete temp2 branch. Pull changes form main branch and create temp2 again. now replace line1 with line2 and try to merge in main

10- Create a empty local repo. 
    now create 4 files and add them to local git repo in a separate commit
    use rebase command to merge the last three commits. 

11- Create remote repo on github or azure repos. 
    add a file in the repo and commit it to main branch
    now create new-main branch from main. 
    clone the repo locally and create a temp-main branch from main. 
    make changes to the file and add them to temp-main branch. Create a PR and merge changes to to main branch
    Also cherry pick changes to new-main branch

### Point 1: Create a local git repo. create two files in it.
* Create a folder, move to it and initialize local repo.
  ```
  mkdir DevOps_Lab_04
  cd DevOps_Lab_04
  git init
  
  # Initialized empty Git repository in D:/Labs/DevOps_Lab_04/.git/
* Create 2 files
  ```
  touch file1.txt file2.txt
* Write some lines in the both files and commit changes.  
  file1.txt (This is file1.txt content.)
  file2.txt (This is file2.txt content.)
    ```
    git add file1.txt file2.txt
    git commit -m 'Initial commit'
* Now write some lines again in both files and add changes to staging area for only one file:  
  * file1.txt:  
    > This is file1.txt content.  
    > This is line2 of file1.txt.
  * file2.txt:
    > This is file2.txt content.  
    > This is line2 of file2.txt.
  ```
  git add file1.txt
* Now use diff commands to check difference for both files
    ```
    git diff                      # for unstaged file (file2.txt)
    
    diff --git a/file2.txt b/file2.txt
    index 9daa472..6e71a4c 100644
    --- a/file2.txt
    +++ b/file2.txt
    @@ -1 +1,2 @@
    -This is file2.txt content.
    \ No newline at end of file
    +This is file2.txt content.
    +This is line2 of file2.txt.
    \ No newline at end of file
   

    git diff --staged            # for staged file (file1.txt)

    diff --git a/file1.txt b/file1.txt
    index 9a440cf..c526d0d 100644
    --- a/file1.txt
    +++ b/file1.txt
    @@ -1 +1,2 @@
    -This is file1.txt content.
    \ No newline at end of file
    +This is file1.txt content.
    +This is line2 of file1.txt.
    \ No newline at end of file
### Point 2: Use VS code and check differences between both files
* Open folder in VS code.
* Right click on fil1.txt and click 'Select for Compare'.
* Right click on file2.xtx and click 'Compare with Selected.'  
 
    This open file comparison (file1.txt ⟷ file2.txt).  
    Output of comparison shows the line change -/+, and actual change with highlighted content.
  > -This is file`1`.txt content.  
  > -This is line2 of file`1`.txt.  
  > +This is file`2`.txt content.  
  > +This is line2 of file`2`.txt.
### Point 3: Perform Lab on Git Lecture 2 Slide 15
[See Lab 2](https://github.com/abdul-rehman-236/DevOps_Lab_02)
### Point 4: Perform Lab on Git Lecture 2 Slide 16
[See Lab 2](https://github.com/abdul-rehman-236/DevOps_Lab_02)