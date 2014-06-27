# Module 1: GIT

Prior to completing the module below it is highly recommended that you look at the following learning material.  **Even if you consider yourself a GIT expert, there is material in the resources below that even seasoned GIT users are not aware of.  It only helps you more.**

* [GIT Official Site's Documentation book](http://git-scm.com/book)
* CodeSchool.com
  * [Try Git](http://www.codeschool.com/courses/try-git)
  * [Git Real](http://www.codeschool.com/courses/git-real)
  * [Git Real 2](http://www.codeschool.com/courses/git-real-2)
* Tutsplus.com
  * [Git Essentials](https://tutsplus.com/course/git-essentials)

You'll need the indatus login for some of this which is on [helpdesk.indatus.com](http://helpdesk.indatus.com) (INDATUS > IT > Development > Learning Resources > Paid Resource Logins).  Email bwebb@indatus.com if you encounter any issues.


## The Test

1.  Init a new git repo
2.  Create a new file called `friends.txt` with the first and last name of 5 people on lines 1-5
3.  Add the file to the repo
4.  Commit the file to the repo with a message of "these are my friends"
5.  Create a remote repository in your gitlab.indatus.com namespace called `git_test` and add it as a remote repo
6.  Push your changes to the remote repo
7.  Go into gitlab, view the `friends.txt` file, edit it to add a 6th friend, and commit it in the browser with the message "added another friend".
8.  Now pull the code to your local repo
9.  Create a branch called `party` and switch to it
10. Now in the `party` branch add 4 more friends names to `friends.txt` for a total of 10, commit those changes with a message of "adding more friends for the party"
11. Now switch back to the `master` branch, edit the `friends.txt` file (which has 6 friends) and add 9 friends for a total of 15. Make sure you include some of the friends you added in the `party` branch but not all of them.  Commit this with a message of 'new friends'.
12. Now merge the `party` branch into the `master` branch.  This should cause a CONFLICT.  Edit the `friends.txt` file and fix the merge conflict, removing duplicate names.  The total number of names you'll have at the end of this process will depend on the number of people you duplicated between the `master` and `party` branches.
13. Commit the changes with the default merge message.
14. Push all branches to the remote repository
15. Switch to the `party` branch and rebase it from the `master` branch.  Push the `party` branch updates to the remote repo.
16. In the `party` branch add a new file called `family.txt`, add 2 family member's names on line 1 and 2.
17. Add the `family.txt` file, then stash it, switch to the `master` branch and pop the stash and stage the file in the repo.
18. Now create another file called `pets.txt` and in it put 2 names of your pets, if you don't have any make them up.
19. Add both files and commit them with the message "some of my family and pets".
20. Now take that last commit and split it into 2 commits, 1 for each file with messages "my family" and "my pets".  Then push to the remote repo.
21. Look at the git log in `oneline` and verify your commit messages.
22. Now in a new working directory create a totally new git repo called `community`, create a new remote for it in your gitlab account (in your own namespace). Add the remote to your local git repo.
23. Create a new file called `address.txt` with your address in it, stage, commit and push the changes with a relevant commit message.
24. Now bring in your `git_test` repo to the `community` repo as a submodule, stage your changes and commit with a relevant commit message.
25. Now make go into the `git_test` submodule folder, add a file called `todo.txt` and put a todo item in it.  Stage commit and push the file to the repo.
26. Now get out of the `git_test` folder to your `community` root, and stage the `git_test` folder, add a commit with the message "first commit with submodule" and push to the remote repo.
27. Now create a `v1.0` tag with the message 'ready for review' and push the tag to the remote repo.
28. Do the same thing with the `git_test` repo.
29. Now in both `community` and `git_test` repos within GitLab enable "Issues" as a feature and save. Then go to project members and add all team leaders and dept. manager.
30. In the `community` repo, create a new GitLab Issue titled "Review Module 1 - Git Test" and @mention all the team leaders and the department manager in the description. For example, `@tharvey @bkuhl please review`.