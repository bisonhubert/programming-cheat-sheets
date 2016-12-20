# Git Cheat Sheet

- [Branching](#branching)
- [Rebasing](#rebasing)
- [Undo Commits](#undo-commits)
- [Ignoring Files Locally](#ignoring-files-locally)

### Branching
BRANCHING OFF A BRANCH + PUSHING UP CHANGES
* create a feature branch off testing branch
`$ git checkout -b my_feature testing`
...some work
`$ git commit -m "Add tests"`
`$ git checkout testing`
`$ git merge --no-ff my_feature`
`$ git push origin testing`


### Rebasing
`$ git rebase -i <branch-merging-to>`
* select which commits to squash
`$ git push -f`

```bash
rebase last three commits into one
git checkout feature
git rebase -i HEAD~3
$
```




### Undo Commits
* all commits
`$ git reset HEAD~`
* last 3 commits
`$ git reset HEAD~3`
* by specific commit
```bash
$ git log
// check which commit is one prior to a merge
$ git reset --hard commit_sha
```


### Ignoring Files Locally
* ignore a local file
```bash
git update-index --assume-unchanged [<file>...]
```

* show all ignored files
```bash
git check-ignore *
```

* remove an ignored file from the ignored list
```bash
git update-index --no-assume-unchanged [<file>...]
```

