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
git flow feature finish first_feature #will merge
```