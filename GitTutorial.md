
# Tutorial for Git First-Timers: Clone A Repo And Submit Edits to the WTD Guide

*If you have any trouble following these steps, or if you find errors or omissions, please open an issue. You can also contact the author in the WTD Slack group: @ccromwell.*

Before you begin, you must have a GitHub account. If you don't, sign up at https://github.com/join


## 1. If you've never downloaded Git, get the latest version:
https://git-scm.com/downloads

If you'd like to find out whether Git is installed, and what version, use this command: 
````
$ git --version
````

## 2. Set up Git by telling it your name:

````
$ git config --global user.name "Mona Lisa"
````
For more information:  https://help.github.com/articles/setting-your-username-in-git/

## 3. And your email address:

````
$ git config --global user.email "email@example.com"
````
For more information: https://help.github.com/articles/setting-your-commit-email-address-in-git/

## 4. Fork the repo you want to work on

To fork the Repo, click the Fork button in the upper right hand corner. Now you have a copy of the repo in your collection.) If you need more help, use the GitHub docs: https://help.github.com/articles/fork-a-repo/

## 5. Make or choose a local folder and clone the repo

CAUTION: First decide where you want the cloned repo to be saved on you computer. Navigate there in the terminal before cloning (use the ``cd `` command). Git will create a new folder when you clone, inside whatever folder you have navigated to. 

CAUTION: Be sure to clone from your own GitHub, and not from the original repo that you forked -- you might not be able to push changes back upstream if you choose the wrong repo. 

The HTTPS method is recommended for first-timers. Here's an example: 

``$ git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY``

Most of that command is the HTTPS address of your repository (starting after the second word of the example above).
 
To acquire this HTTPS address, press the green *Clone or Download* button on the main page of the repo -- a pop-up window will show the address (be sure that HTTPS method is selected)

Then enter the command line example shown above, using the copied address. After this command executes, you should have a folder with a local clone of the repo. 
 
 TIP: Your username should be visible in the address, if you have chosen the HTTPS method, and if you are indeed cloning from your forked version of the repo. 

Additional help with the HTTPS method is here: https://help.github.com/articles/which-remote-url-should-i-use/#cloning-with-https-urls-recommended

(If you want to use the SSH method, you have to create a key pair, which will take longer, but free you from having to type your password. It's not covered in this tutorial.)

## 6. Navigate through the folder structure in your local Git repo and find a file you would like to edit.
(You can start with small changes like spelling and punctuation. Cloning is enough of a challenge for your first run.)

## 7. Open and edit the file, using a plain text editor.

If you don't have one that you like, you can download Atom, created by the folks at GitHub:
https://atom.io/

Bookmark the Restructured Text markup guide: 
http://www.sphinx-doc.org/en/master/rest.html

## 8. Save the file on your local machine.


## 9. Add the file:

````
$ git add <file name>
````


## 10. Check your status to make sure Git noticed:

````
$ git status
````

In this example output, the file documentarians.rst has been edited and then added:

````
$ modified:   documentarians.rst
````

## 11. Go ahead and commit.

````
$ git commit -a
````

You have to enter comments for the commit, so your terminal will automatically open a text editing utility. (You can probably save and close by typing ``CONTROL + O``, followed by ``CONTROL + X``, unless your default text editor is Vim or something equally challenging.)

## 12. Check your status again. It should have changed.

````
On branch master
Your branch is ahead of 'origin/master' by 1 commit.
  (use "git push" to publish your local commits)
````

Your local branch should be ahead by one commit, compared to the remote repo that you cloned.

## 13. You can push the changes up to your remote repo by doing a push:

````
$ git push origin master

````

If this succeeds, you should see some output that confirms success:


````
[master ceb7dbf] Changes made to documentarians.rst. This is a practice run of tutorial for WTD SF.
 1 file changed, 9 insertions(+), 9 deletions(-)
Clarences-MacBook-Pro:www Clarence$ git status
On branch master
Your branch is ahead of 'origin/master' by 1 commit.
  (use "git push" to publish your local commits)
nothing to commit, working tree clean
Clarences-MacBook-Pro:www Clarence$ git push origin master
Counting objects: 4, done.
Delta compression using up to 2 threads.
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 625 bytes | 0 bytes/s, done.
Total 4 (delta 3), reused 0 (delta 0)
remote: Resolving deltas: 100% (3/3), completed with 3 local objects.
To https://github.com/cwcromwell/www.git
   5606fb6..ceb7dbf  master -> master

````

You're not done yet. The changes are in your GitHub repo, but you need to share them with the folks who own the original project.

## 14. Create a pull request.

a. Go to the original WTD repo (not yours) and push the button that says New Pull Request. (It's only on the main page.)

b. Click the blue link that says Compare Across Forks

c. Use the third pulldown window from the left to choose the name of your fork repo
You should see the comment you saved when you made the commit. And if you scroll down, you should be able to see a diff of the changes to the document. 

d. Remember to push the green button that says "Create Pull Request"

## 15.  You're done. Time to celebrate. 

For more information on how to do this, see the GitHub documentation:
https://help.github.com/articles/creating-a-pull-request-from-a-fork/

## 16. Check out these resources to keep learning:

There's a free book about Git that you can download: 

https://git-scm.com/book/en/v2
