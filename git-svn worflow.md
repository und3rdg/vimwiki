()git svn clone http://feature_branch

(master) git svn rebase

(master) git checkout -B work
(work) [commit commit commit]
(work)   git checkout master

(master) git svn rebase
(master) git checkout work

(work) git merge master
(work) git checkout -D _publish
      (git reset HEAD^) to revert

(_publish) git rebase master
(_publish) git diff work
(_publish) git checkout master

(master) git meerge --ff --squash _publish
(master) git svn dcommit


