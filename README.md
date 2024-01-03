# gitflow-test

Git flow is for easier management of branch control. instead of the standard 
```git checkout -b branch_name``` for standard new branches for development we can simply it based on the nature of the branch with ```git flow <branch_nature> start <branch_name>```. where branch nature comes into play is either its one of the following:

1. feature branch [feature/]
1. bugfix branch  [bugfix/]
1. release branch [release/]
1. hotfix branch  [hotfix/]
1. support branch [support/]

we will see these in the initalization of the gitflow. it is important to know that these once pushed should be replicated across all developers stations upon pulling the new project under the ```.git/hooks```


```
git flow feature start first_feature
git flow feature finish first_feature #will merge and delete the feature branch
```
but how do we manage features/releases/hotfix and such?
when we want to finish a branch (i.e. close it out)
``` 
git flow feature finish first_feature
Switched to branch 'develop'
Your branch is up to date with 'origin/develop'.
Updating 667bf7f..df6187c
Fast-forward
 README.md  | 6 ++++++
 feature.md | 1 +
 2 files changed, 7 insertions(+)
 create mode 100644 feature.md
To github.com:mrpainte/gitflow-test.git
 - [deleted]         feature/first_feature
Deleted branch feature/first_feature (was df6187c).

Summary of actions:
- The feature branch 'feature/first_feature' was merged into 'develop'
- Feature branch 'feature/first_feature' has been locally deleted; it has been remotely deleted from 'origin'
- You are now on branch 'develop'
```
but if we want to start the feature branch we will see:
```
git flow feature start second_feature
Branches 'develop' and 'origin/develop' have diverged.
And local branch 'develop' is ahead of 'origin/develop'.
Switched to a new branch 'feature/second_feature'

Summary of actions:
- A new branch 'feature/second_feature' was created, based on 'develop'
- You are now on branch 'feature/second_feature'

Now, start committing on your feature. When done, use:

     git flow feature finish second_feature
```
# what does this allow us to do?
