# How to delete all commit history in github?

Checkout

git checkout --orphan latest_branch

Add all the files

git add -A

Commit the changes

git commit -am "commit message"

Delete the branch

git branch -D main

Rename the current branch to main

git branch -m main

Finally, force update your repository

git push -f origin main


----------------------------------------------------------


# Here's how you can ignore big size files using Git LFS:

Initialize Git LFS in your repository:
Open your terminal or command prompt, navigate to your WordPress project's root directory, and run the following command:

git lfs install


Specify the file types to be tracked with Git LFS: Create or update your .gitattributes file in the root directory of your WordPress project. This file defines which files should be tracked using Git LFS. Add the file types you want to track. For example, to track all .zip and .tar.gz files, add the following lines to the .gitattributes file:

*.zip filter=lfs diff=lfs merge=lfs -text

*.tar.gz filter=lfs diff=lfs merge=lfs -text



Add, commit, and push the .gitattributes file:

git add .gitattributes

git commit -m "Add Git LFS configuration"

git push origin master (or your preferred branch)

