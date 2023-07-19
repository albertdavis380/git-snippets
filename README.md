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

git lfs install

*.zip filter=lfs diff=lfs merge=lfs -text

*.tar.gz filter=lfs diff=lfs merge=lfs -text

git add .gitattributes

git commit -m "Add Git LFS configuration"

git push origin master (or your preferred branch)

