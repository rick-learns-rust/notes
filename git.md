To set up a secure connection between your computer and github, follow the instructions found here:

https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account

ensure you do at least prerequisite #2.

==

To add a repository created by cargo new <name>, do the following actions:

in GitHub:
select 'Your repositories' from the user menu (top right)
click the 'New' button
enter <repository name>
select a license (I usually select MIT)
click 'Create Repository' button

locally (in the project directory):
git add . //add all the files to the repository
git commit -m "first commit" //commit the added files
git branch -m main //cargo creates master branch, rename it
//create a relationship with github (I'm using SSH)
git remote add origin git@github.com:rick-learns-rust/<repository name>.git
git push -u -f origin main //push the code to github

in Github:
click on the repository
select the 'Settings' tab
click Code and Automation/Branches
click 'Branch protection rule' button
enter 'main' for Branch name pattern
select your desired protections
click 'Create' button
