# Managing Git Commit History with 'git rebase'

Since `git rebase` is one of the more useful advanced features of Git, I
thought it might be helpful to give some examples of common rebase operations.

One important piece of advice: **never** use `git rebase` in a branch that
you share with others unless you absolutely have to and have communicated
this to them.  Once you use `git rebase`, the commit history (including
commit hashes) will be completely different even if you just ran `git rebase`
without changing any commits.

My general workflow is this:

- Create a private feature branch either based on a common shared branch (master, develop, 
  etc).  Usually I will prefix it with my username, e.g. `daviwil/my-feature-branch`
  
- Start working on the feature, making any commits that I need to make.  I'll even make
  commits of code that doesn't compile just so that I can push the current state to
  GitHub to have it backed up.
  
- Once I'm ready to merge my work back into a shared branch, I run `git rebase` to clean
  up my commit history and eliminate some of those intermediate commits.  I may also
  reorder my commit history, squash multiple related commits, and rewrite commit
  messages to give a more coherent change history.
  
This workflow allows me to quickly make progress coding without worrying about creating a
good commit history.  Once I'm finished with my code and am fully understand the scope of
my changes, I can sculpt the commit history to be more helpful to anyone who looks over
it in the future.

## Common Tasks

### Fixing the wording of a commit somewhere in your history

*TODO: Add description and examples.*

### Avoiding merge commits from other branches (especially master)

*TODO: Add description and examples.*

### Squashing "oops" commits

*TODO: Add description and examples.*

### Re-ordering commits

*TODO: Add description and examples.*

### Changing the author of a commit

*TODO: Add description and examples.*

### Extracting unrelated commits from a feature branch

*TODO: Add description and examples.*