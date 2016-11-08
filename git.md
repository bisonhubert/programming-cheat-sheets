# Git Cheat Sheet

- [Branching](#branching)gs

### Branching
BRANCHING OFF A BRANCH + PUSHING UP CHANGES
* create a feature branch off testing branch
`$ git checkout -b my_feature testing`
...some work
`$ git commit -m "Add tests"`
`$ git checkout testing`
`$ git merge --no-ff my_feature`
`$ git push origin testing`
`$ git push origin my_feature`


REBASING
`$ git rebase -i <branch-merging-to>`
* select which commits to squash
`$ git push -f`


UNDO COMMITS
* all commits
`$ git reset HEAD~`
* last 3 commits
`$ git reset HEAD~3`


IGNORING FILES LOCALLY
git update-index --assume-unchanged [<file>...]


SHOW IGNORED FILES
git check-ignore *


Remove from ignored:
git update-index --no-assume-unchanged [<file>...]
