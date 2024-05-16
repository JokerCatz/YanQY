# git basic work flow

## [source repo] <= [self forked repo] , no body can update [source repo] without PR

## fork [source repo] to [self forked repo] first

## at [self forked repo] , init remote , only need do this one time

    // add [source repo] to remote and make a alias name `upstream`
    > git remote add upstream https://github.com/{URL}.git  

## sync [self forked repo] master branch same as [source repo] master branch

    {
      // [self forked repo] master should be old version
      > git checkout master
      // update [source repo = upstream] status , and make [self forked repo] master branch same as [source repo] master branch
      > git fetch upstream ; git merge upstream/master
      // you can use this update [self forked master] branch to last version and effect to remote [self forked repo]
      //> git push 
    }

## normal work flow

    // master branch at [self forked repo] , not [source repo] , and it should be old version
    > git checkout master

    // do fix code ... testing .... and finish the ticket

    // add branch for the PR , this branch will base on the old version of master branch at [self forked repo] 
    > git branch add_WTF
    // switch branch
    > git checkout add_WTF
    // add files or change to commit
    //> git add ...
    // commit text: "WIP" , this commit base on the old version of master branch at [self forked repo] , and make a new commit
    > git commit

    {
      // [self forked repo] master should be old version
      > git checkout master
      // update [source repo = upstream] status , and make [self forked repo] master branch same as [source repo] master branch
      > git fetch upstream ; git merge upstream/master
      // you can use this update [self forked master] branch to last version and effect to remote [self forked repo]
      //> git push 
    }

    // switch branch , but plz remember here is still old version of master branch at [self forked repo] and + 1 commit
    > git checkout add_WTF
    // rebase to last version of master branch at  [self forked repo] and + 1 commit , and now should be [source repo] branch last version + 1 commit
    > git rebase master
    // push the +1 commit (may add new branch at self forked remote branch)
    > git push
    // goto github to new PR