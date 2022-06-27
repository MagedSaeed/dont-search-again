# Show local commits before pushing them

```bash
git log origin/master..HEAD
```
## More links
- https://stackoverflow.com/a/2016954/4412324


# When master branch changed on remote

If the master branch name changed in remote, you can do the following to pull/reflect this change in the local repo:

```bash
git branch -m master main
git fetch origin
git branch -u origin/main main
git remote set-head origin -a
```
These settings are showned once as a pop-up on github interface but never come again.
