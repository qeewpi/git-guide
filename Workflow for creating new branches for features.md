### 1. Start with the main branch:
All feature branches are created off the latest code state of a project. This guide assumes this is maintained and updated in the main branch.

```bash
git checkout 17.0
git fetch origin 
git reset --hard origin/17.0
```

### 2. Create the repository
This switches the repo to the 17.0 branch, pulls the latest commits and resets the repo's local copy of main to match the latest version.

### 3. Create a new-branch
Use a separate branch for each feature or issue you work on. After creating a branch, check it out locally so that any changes you make will be on that branch.
```bash
git checkout -b <tag/ticket#_shortdescription_initial>
```
This checks out a branch called new-feature based on 17.0, and the -b flag tells Git to create the branch if it doesn’t already exist.

For the guidelines in naming the branch, refer to the [Internship Project Onboarding Powerpoint Slides](https://docs.google.com/presentation/d/1LINVQgTBiO4kdD4QlNe1LBbFpGnc2T1iwKYvlhYjJvk/edit?usp=sharing).
### 4. Update, add, commit, and push changes
On this branch, edit, stage, and commit changes in the usual fashion, building up the feature with as many commits as necessary. Work on the feature and make commits like you would any time you use Git. When ready, push your commits, updating the feature branch on Bitbucket.
```bash
git status
git add <some-file>
git commit
```

### 5. Push feature branch to remote
It’s a good idea to push the feature branch up to the central repository. This serves as a convenient backup, when collaborating with other developers, this would give them access to view commits to the new branch.
```bash
git push -u origin new-feature
```
This command pushes new-feature to the central repository (origin), and the `-u` flag adds it as a remote tracking branch. After setting up the tracking branch, git push can be invoked without any parameters to automatically push the new-feature branch to the central repository. To get feedback on the new feature branch, create a pull request in a repository management solution like Bitbucket Cloud or Bitbucket Data Center. From there, you can add reviewers and make sure everything is good to go before merging.

