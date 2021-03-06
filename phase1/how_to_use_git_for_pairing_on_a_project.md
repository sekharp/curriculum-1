How to use git for pairing on a project
---------------------------------------

[Video](https://vimeo.com/156561999)

* **Pairing**: two people working on one computer.
* **Project**: One codebase with multiple team members contributing to it.

Git will facilitate this approach through branches and merging.

Branches are versions of the code that you give a name to
and have independent histories.

Merging is when you bring multiple branches together into a single branch.

The Process
-----------

Pick one person to host the main repository, we'll call them "Host".
Give the pair commit access to it on gihub, we'll call them "Pair".
Commit access will allow them to directly push changes to the repository.
Pair clones from Host's repository.
When working on either computer, follow this process:

1. Go to the master branch `$ git checkout master`
1. Make sure everything is committed `$ git status`,
   Things get weird when you change branches with uncommitted work...
   you'll probably lose it.
1. Make sure you have the latest copy of the code `$ git pull`
   You want to be working from the most recent code.
1. Create a new branch for whatever you're working on `$ git checkout -b iteration_3`
   (again, make sure you're on the master branch when doing this)
1. Do work on this branch, same as normal.
1. Push to github with `$ git push -u origin iteration_3`
1. On Github, create a pull request to the master branch
1. If there are any other members of the team than the pair,
   then ask that member to review the code and merge it
   when they consider it acceptable.
   If there arn't, then go ahead and merge it now.
   You can do this within github.
1. Go back to the master branch `$ git checkout master`
1. Pull the new changes `$ git pull`


The Git Game!
-------------

For each team member:

* 1 point: A pull request from the member
* 1 point: The branch name is be the team member's name
* 1 point: The pull request adds a new file with that member's name
* 1 point: Someone else on the team will pull it into master
           Each member get's a max of 1 point here, so for 3
           points, you'd need 3 members to pull. If only one pulls
           all 3 requests, then you only get 1 point.
* 1 point: Pull the changes into master and see all three commits

Assuming 3 members, that's 5 points each for a total of 15.
Which team will win?!
