# Quick `git rebase` command demo

Part - I
---
1. Create a repo - by default it is `master` branch
2. Freeze a commit `m1` - milestone1

Part - II
---
1. Create a new `branch` called `b1-cut-from-commit-m1` from `master`
2. Freeze a commit `b1` - feature1 


|`master` commit messages stack | `b1-cut-from-commit-m1` commit messages stack|
|---|---|
|`m1`| `b1` <br> `m1`|
|Now assume there is a change made to master as `m2` and the new commit stack for master looks like below  <br> `m2` <br> `m1` | If we do `git rebase master` from `this` branch. <br> Then <br> 1. It may result in conflicts. <br> 2. We have to fix those conflicts. <br> 3. unlike `git merge` no extra merge commit is needed<br> Now, the commit message stack for this branch looks clean and it seems as if the branch is cut from latest master i.e., branch commits are always on top of master commits<br> `b1` <br>`m2` <br> `m1`|


