# 102_Read_03

## Git intro

- [Answer](#answer)

## Answer

1. What is Version Control?
    - A system that records & tracks changes and allows one to re-visit previous revisions of a file/set of files.
2. What is `cloning` in Git?
    - Cloning in Git is creating a copy of an existing Git repository and all versions of all files.
3. What is the command to track and stage files?
    - `git add []` followed by the file name tracks a singular file
    - `git add *` tracks all files in repository
        - Remember **ACP**; **A**dd > **C**ommit > **P**ush
4. What is the command to take a snapshot of your changed files?
    - `git commit -a` commits a snapshot of all modifications to tracked files
5. What is the command to send your changed files to Github?
    - `git origin push master` sends changed files from local “master” branch to remote repo named “origin”
        - If its a cloned repo, git will auto-name the repo which was cloned “origin” and your local repo, “master”. Names subject to change by user
