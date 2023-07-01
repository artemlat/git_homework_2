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

### 3. Push all branches to the external repository:

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






