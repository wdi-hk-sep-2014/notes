# Using GitHub

## Objective

- Being a developer in the open source GitHub community
- Learn the workflow to contribute a open source project

## Steps

1. Visit the GitHub link https://github.com/wdi-hk-sep-2014/PepperLunchClone
2. Click the `Fork` button at top-right corner, fork the project to your own account
3. Go to your Terminal, type `git clone https://github.com/[username]/PepperLunchClone.git`
4. The project will be downloaded to your computer
5. Make changes
6. Commit the changes using `git add -A` and `git commit -m "Modify something"`
7. Push the code to your own repository in GitHub by `git push`
8. Create a pull request on GitHub, from your own to the owner
    - You may get accepted
    - Your pull request may be rejected
9. To update the latest code, you need to configure a remote for the original repository using `git remote add upstream https://github.com/wdi-hk-sep-2014/PepperLunchClone`
10. Then, you may need to discard your own commit by `git reset --hard [commit hash]`
11. Pull the latest code using `git pull upstream master`
12. Check the commit hash using `git log`

## Remarks

Since some time our commit may be rejected, doing `git reset` is one step more. It is suggested to make a new branch to do your changes.

1. Run `git checkout -b [my_change]`
2. Modify the code and commit
3. Push the code using `git push -u origin [my_change]`
4. Create the pull request from your branch to the owner's master branch
5. If you want to sync the fork, just checkout the master branch by `git checkout master`
6. You can fetch the changes using `git fetch upstream`
7. Then pull the changes using `git pull upstream master`
8. Optionally, you can sync with your own GitHub repository using `git push origin master`

## Successful Completion

- You should see the folder of source code available in your computer
- Try to do the `rails new`
- Try to create the first scaffold

## Reference Links

- [Using pull requests](https://help.github.com/articles/using-pull-requests/)
- [Configuring a remote for a fork](https://help.github.com/articles/configuring-a-remote-for-a-fork/)
- [Syncing a fork](https://help.github.com/articles/syncing-a-fork/)
- [How do I sync a fork without deleting local changes?](http://stackoverflow.com/questions/10307153/how-do-i-re-grab-a-forked-git-repo-without-deleting-and-re-forking)

