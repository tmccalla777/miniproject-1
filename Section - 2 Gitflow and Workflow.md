# What is Gitflow Workflow ?
## Gitflow Workflow is a Git workflow design that was first published and made popular by Vincent Driessen at nvie. The Gitflow Workflow defines a strict branching model designed around the project release. This provides a robust framework for managing larger projects.  
# The overall flow of Gitflow is:
1. A develop branch is created from master
2. A release branch is created from develop
3. Feature branches are created from develop
4. When a feature is complete it is merged into the develop branch
5. When the release branch is done it is merged into developand master
6. If an issue in master is detected a hotfix branch is created from master
6. Once the hotfix is complete it is merged to both develop and master
