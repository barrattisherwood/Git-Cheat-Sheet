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