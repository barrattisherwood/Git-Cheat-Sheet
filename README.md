# Git-Cheat-Sheet
My Git cheat sheet readme

## Git Aliases
File system root for user:
```
cd
```

Open .bashrc with VS Code
```
code ~/.bashrc
```

```
alias ga='git add'
alias gaa='git add .'
alias gaaa='git add --all'
alias gau='git add --update'
alias gb='git branch'
alias gbd='git branch --delete '
alias gc='git commit'
alias gcm='git commit --message'
alias gcf='git commit --fixup'
alias gco='git checkout'
alias gcob='git checkout -b'
alias gcom='git checkout master'
alias gcos='git checkout staging'
alias gcod='git checkout develop'
alias gd='git diff'
alias gda='git diff HEAD'
alias gi='git init'
alias glg='git log --graph --oneline --decorate --all'
alias gld='git log --pretty=format:"%h %ad %s" --date=short --all'
alias gm='git merge --no-ff'
alias gma='git merge --abort'
alias gmc='git merge --continue'
alias gp='git pull'
alias gpr='git pull --rebase'
alias gr='git rebase'
alias gs='git status'
alias gss='git status --short'
alias gst='git stash'
alias gsta='git stash apply'
alias gstd='git stash drop'
alias gstl='git stash list'
alias gstp='git stash pop'
alias gsts='git stash save'
```

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