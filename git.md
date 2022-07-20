# Show local commits before pushing them

```bash
git log origin/master..HEAD
```
## More links
- https://stackoverflow.com/a/2016954/4412324


# When master branch name changed on remote

If the master branch name changed in remote, you can do the following to pull/reflect this change in the local repo:

```bash
git branch -m master main
git fetch origin
git branch -u origin/main main
git remote set-head origin -a
```
These settings are showned once as a pop-up on github interface but never come again.

# Removing a branch locally before commiting it to remote

```bash
git branch -d  local_branch_name
```

## More
- https://www.freecodecamp.org/news/git-delete-branch-how-to-remove-a-local-or-remote-branch/


# Branches

## Switch to existing branch

```bash
git checkout <branch_name>
```

## Create new branch and switch to it

```bash
git checkout -b <branch_name>
```

### More:
- https://devconnected.com/how-to-switch-branch-on-git/


# Discarding local changes in git

```bash
git restore .
git resotre path/to/file
```
## More
- https://stackoverflow.com/a/52713/4412324

# Git configuration (setting username and email)

To list the saved data:
```bash
git config --list
```
to set:
```bash
git config user.name "Your Name"
git config user.email "youremail@yourdomain.com"
```

## More:
- https://linuxize.com/post/how-to-configure-git-username-and-email/
