To create a feature branch in git and then push to main, you can use the following steps:

Create a new branch from the main branch:
git checkout -b <feature-branch>

Make your changes on the feature branch:
# make your changes

Commit your changes:
git commit -m "Your commit message"

Push your changes to the remote repository:
git push origin <feature-branch>

Merge the feature branch into the main branch:
git checkout main
git merge <feature-branch>

Push the changes to the remote repository:
git push origin main