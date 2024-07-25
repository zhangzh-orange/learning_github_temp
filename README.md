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

git add <changed_file>

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