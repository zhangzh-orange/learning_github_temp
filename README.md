# learning_github_temp

-----

1. Clone repository:

git clone website

2. Build a new branch, to save revised code, rather than save new code to main branch.
This command is like copy main branch's code to your own branch.

git checkout -b <my-feature>

3. Check difference between local and git:

git diff

4. Add changed_file to git:

git add <changed_file> / git add .

5. Commit changed files to git, and enter the commit message for your changes. :

git commit

Then you will enter into a editor page for editting message. (my default editor is vim)

Press "c" to edit the commit message.

Press "Esc", input "wq" to back to vim start mode, and save the message.

Press "ZZ" to exit vim editor and back to git console.

6. Push your code to github, with building a new branch (not save into main branch):

git push origin <my-feature>

7. Sometimes when we commit code to our branch, the main branch's code have has some updates.
We need to synchronize the main branch and our own branch, and check if our own update still work.

7.1 Update our local main branch:

7.1.1 Switch to the main branch:

git checkout main

7.1.2 Update, synchronize the remote main branch to our local main branch:

git pull origin master

7.2 Update our own -feature branch:

git checkout <my-feature>

git rebase main # synchronize the main branch to our own -feature branch

If rebase conflict occurs, we need to choose which one to remain manually.

7.3 Push rebase code to github (force)

git push -f origin <my-feature>

8. Pull request, merge your code to main branch (feature branch holder do this on github)

9. Squash and merge (main branch holder do this on github)

10. Delete -feature branch at remote github.

11. Delete -feature branch of local git:

git checkout main

git branch -D <my-feature>

12. Pull the latest update of main branch:

git pull original master