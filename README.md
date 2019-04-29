# Git-Cheat-Sheet
My Git cheat sheet readme

## To generate SSH keys
* Git bash `ssh-keygen`
* Default location okay
* Enter pass phrase if you wish
* Keep private key safe (id_rsa)
* copy public key into github (id_rsa-pub)
* www.github.com -> Settings -> SSH and GPG keys
* Add new SSH Key
* Add Title for device and key into text fields
* Add SSH Key

## To switch remote repo
### Existing:
```
$ git remote -v
> origin  git@github.com:USERNAME/REPOSITORY.git (fetch)
> origin  git@github.com:USERNAME/REPOSITORY.git (push)
```
### Change:
```
$ git remote set-url origin https://github.com/USERNAME/REPOSITORY.git
```
### Confirm change:
```
$ git remote -v
# Verify new remote URL
> origin  https://github.com/USERNAME/REPOSITORY.git (fetch)
> origin  https://github.com/USERNAME/REPOSITORY.git (push)
```

## Amend most recent commit
```
git commit --amend -m "New commit message"
```
If you've already pushed your commit up to your remote branch, then you'll [need to force push the commit](https://stackoverflow.com/questions/41003071/why-must-i-force-push-after-changing-a-commit-message) with:
```
git push <remote> <branch> --force
# Or
git push <remote> <branch> -f
```