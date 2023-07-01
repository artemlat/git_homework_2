# #2 GIT Homework  
*Here I continued to work with git repositories, created some branches in the local repository, pushed these branches to external repository:*  
*Before i started to do the tasks i had created an external repository named "work_with_branches" and cloned it to the local computer.*  

### 1. In the local repository create branches for:
*- Postman*  
*- Jmeter*  
*- CheckLists*   
*- Bug_reports*  
*- SQL*  
*- Charles*   
*- Mobile_testing*

```
artem@DESKTOP-4FHC137 MINGW64 /d/github/work_with_branches (main)
$ git branch Postman | git branch Jmeter | git branch CheckLists | git branch Bug_reports | git branch SQL | git branch Charles | git branch Mobile_testing
```

### 2. Push all branches to the external repository:

```
artem@DESKTOP-4FHC137 MINGW64 /d/github/work_with_branches (main)
$ git push -u origin SQL
Enter passphrase for key '/c/Users/artem/.ssh/id_rsa':
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'SQL' on GitHub by visiting:
remote:      https://github.com/artemlat/work_with_branches/pull/new/SQL
remote:
To github.com:artemlat/work_with_branches.git
 * [new branch]      SQL -> SQL
branch 'SQL' set up to track 'origin/SQL'.

artem@DESKTOP-4FHC137 MINGW64 /d/github/work_with_branches (main)
$ git push -u origin Bug_reports Charles
Enter passphrase for key '/c/Users/artem/.ssh/id_rsa':
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
To github.com:artemlat/work_with_branches.git
 * [new branch]      Bug_reports -> Bug_reports
 * [new branch]      Charles -> Charles
branch 'Bug_reports' set up to track 'origin/Bug_reports'.
branch 'Charles' set up to track 'origin/Charles'.

artem@DESKTOP-4FHC137 MINGW64 /d/github/work_with_branches (main)
$ git push -u origin CheckLists Jmeter Mobile_testing Postman
Enter passphrase for key '/c/Users/artem/.ssh/id_rsa':
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
To github.com:artemlat/work_with_branches.git
 * [new branch]      CheckLists -> CheckLists
 * [new branch]      Jmeter -> Jmeter
 * [new branch]      Mobile_testing -> Mobile_testing
 * [new branch]      Postman -> Postman
branch 'CheckLists' set up to track 'origin/CheckLists'.
branch 'Jmeter' set up to track 'origin/Jmeter'.
branch 'Mobile_testing' set up to track 'origin/Mobile_testing'.
branch 'Postman' set up to track 'origin/Postman'.
```

### 3. Create txt file with bug report structure in the "Bug_reports" branch:  

```
artem@DESKTOP-4FHC137 MINGW64 /d/github/work_with_branches (main)
$ git checkout Bug_reports
Switched to branch 'Bug_reports'
Your branch is up to date with 'origin/Bug_reports'.

artem@DESKTOP-4FHC137 MINGW64 /d/github/work_with_branches (Bug_reports)
$ cat >> bug_structure.txt


bug_report
  id: 1
  environment: Windows 10, Chrome 112
  summary: No icon of the quote in the widget on the main screen
  steps:
    step1: open the app
    step2: tap on the widget banner
    step3: tap on [Confirm]
    step4: collapse the app
    step5: go to the main screen

  ER: Quote icon is displayed in the widget
  AR: Quote icon is displayed in the widget
  attachments: link
```  

### 4. Push bug_structure.txt to the external repository:

```
artem@DESKTOP-4FHC137 MINGW64 /d/github/work_with_branches (Bug_reports)
$ git add .
warning: LF will be replaced by CRLF in bug_structure.txt.
The file will have its original line endings in your working directory

artem@DESKTOP-4FHC137 MINGW64 /d/github/work_with_branches (Bug_reports)
$ git commit -m 'add bug_structure.txt to the Bug_reports branch'
[Bug_reports de05d33] add bug_structure.txt to the Bug_reports branch
 1 file changed, 16 insertions(+)
 create mode 100644 bug_structure.txt

artem@DESKTOP-4FHC137 MINGW64 /d/github/work_with_branches (Bug_reports)
$ git push
Enter passphrase for key '/c/Users/artem/.ssh/id_rsa':
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 514 bytes | 514.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To github.com:artemlat/work_with_branches.git
   6041ed7..de05d33  Bug_reports -> Bug_reports
```

### 5. Merge "Bug_reports" branch to "main" branch:  

```
artem@DESKTOP-4FHC137 MINGW64 /d/github/work_with_branches (Bug_reports)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

artem@DESKTOP-4FHC137 MINGW64 /d/github/work_with_branches (main)
$ git merge Bug_reports
Updating 6041ed7..de05d33
Fast-forward
 bug_structure.txt | 16 ++++++++++++++++
 1 file changed, 16 insertions(+)
 create mode 100644 bug_structure.txt
```

### 6. Push "main" branch to the external repository:

```
artem@DESKTOP-4FHC137 MINGW64 /d/github/work_with_branches (main)
$ git add .

artem@DESKTOP-4FHC137 MINGW64 /d/github/work_with_branches (main)
$ git commit -m "add merged bug_structure.txt file to the external main branch"
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

artem@DESKTOP-4FHC137 MINGW64 /d/github/work_with_branches (main)
$ git push
Enter passphrase for key '/c/Users/artem/.ssh/id_rsa':
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
To github.com:artemlat/work_with_branches.git
   6041ed7..de05d33  main -> main
```












