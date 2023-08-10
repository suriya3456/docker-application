git commit --amend:

Sometimes you want to change a commit message that you already pushed or you forgot to add a small commit that is so related to your last commit that you don’t want to create a commit of it’s own. In this case you can use git commit --amend .

Using git commit --amend you can either change the last commit message or you can add an additional change to the last commit. If you want to push your changes, though, you have to use git push -f in either case.

-------------------------------------

 Make a new branch:

The gold standard for implementing a new feature is to create a new branch and put all the code in it. This keeps the existing code safe from bad implementation.


4) Stash/un-stash files:

One of the ways to resolve the checkout error is to stash the changes. This is usually done temporarily to save the work you have done so far in the current branch — if you are not ready to commit these changes.


To recover or undo the stashed changes, we can come back to the branch where we stashed the changes and pop them.

 --> git stash pop


 ---------------------------
 
 Reset to the last commit:

Having the power to reset or undo a task is a lifesaver. In my early days as a developer, I once made the mistake of making changes to live production code. It was a blunder. To my surprise, I was not fired. What saved me from doing any more damage was the reset command. It allowed me to revert all changes in an instant to the last working commit.