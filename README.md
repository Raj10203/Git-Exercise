
# Git-Exercise

A Git practical example demonstrates the fundamental concepts of version control, such as creating branches, making commits, and pushing changes to a remote repository. It helps to understand collaboration workflows, including pull requests, merges, and handling conflicts effectively.


## Pull Request


1. Go to GitHub, navigate to "Pull Requests," and click "New Pull Request.
2. Select your branch as the source and the target branch (usually main or develop).
3. Tag relevant reviewers for feedback.
4. Make any changes based on review comments and push updates.
5. Once approved, merge your Pull Request into the target branch.


## Cherry-pick, Reset
 
1. Reset the branch to a previous commit 

   ```bash  
    git reset --hard <commit-hash> 

2. Find the commit to cherry-pick.

    ```     
    git log --oneline
3. Cherry-pick the commit.

    ```  
    git cherry-pick <commit-hash?

## Rename, merge commits by Rebase -i, Delete

1. Start Interactive Rebase
    ```
    git rebase -i HEAD~3
2. Rename a Commit by selecting reword

    ```
    pick <commit-hash> Commit message before rename
    reword <commit-hash> Commit message you want to rename
    pick <commit-hash> Another commit

3. Merge Commits (Squash)

    ```
    pick <commit-hash> First commit message
    squash <commit-hash> Second commit message (will be merged into the first)
    squash <commit-hash> Third commit message (will be merged into the first)

4. Complete the Rebase
    ```
    git rebase --continue
5. Push Changes (Force Push if Necessary)
    ```
    git push --force

6. for delete last 3 commit
    ```
    git reset --hard HEAD~3

## Tag for each release 

1. Create a Tag
    ``` 
    git tag  <tag-name>  -> for last commit

    git tag <tag-name> <commit-hash> -> for specific commit

2. Push the Tag to the Remote Repository
    ```
    git push origin <tag-name>

3.  Verify the Tag
    ``` 
    git tag
Thats it!







