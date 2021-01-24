# GitHub Classroom Guide for Students

This is a guide for students to setup Git and GitHub for use with GitHub Classroom. We use RStudio in our class, so we will give instructions on how to use RStudio to setup Git locally.

### Steps for getting setup with GitHub
1. Register for account on GitHub (https://github.com/). We recommend using a username that incorporates your name (jfiksel, mtaub, lrjager)

2. Download R (https://cloud.r-project.org/) and RStudio (https://www.rstudio.com/).

3. Install Git. Instructions for Windows users & Mac in section 6 here: http://happygitwithr.com/install-git.html. Windows users should follow Option 1 in 6.2. Mac users can follow Option 1 in 6.3 if comfortable, otherwise follow Option 2. Below, I show how you would access the terminal on a Mac, as well as how to enter the commands given in the link. 

![Alt Text](http://g.recordit.co/ENAZXCmgs9.gif)

4. Setup options in Git to link your computer to your credentials on github. In you have a Mac, go to the terminal (Applications -> Utilities -> Terminal) as shown above. If you have a Windows, open Git BASH, which you should have downloaded in step 3. Enter the three lines of code here: http://happygitwithr.com/hello-git.html, changing the first two lines to your own name and email (this should be the email associated with your GitHub account). Below is an example of what this process looks like on a Mac:

![Alt Text](http://g.recordit.co/ibUp6dYimU.gif)

5. Generate a SSH key so you don’t need to enter your password every time you interact with GitHub. Open RStudio and complete the "From RStudio" version of the instructions on this page http://happygitwithr.com/ssh-keys.html. Test that your computer and github are communicating by following the instruction on this page https://docs.github.com/en/github/authenticating-to-github/testing-your-ssh-connection. This step shouldn't be strictly necessary, so you can move on if you've encountered problems in this step.


### Steps for downloading and editing assignments from GitHub Classroom

1. Make a folder on your own computer specifically for this class (maybe something like bios338 in your Documents folder, say). 

2. You will receive a link to an assignment for each new assignment. Follow the instructions for getting the homework repository set up. You should now have a repository for this homework. Note that after you accept an assignment for the first time, we will send you an invite to join the classroom organization as a member. Please accept this. You will probably get an email with the invitation, but you should also see a link at the top of your main GitHub page. Here is an image of what you should see after clicking the link:

![Alt Text](img/accept-assignment.png)

3. Enter the homework repository on GitHub (this is online--GitHub is different from Git!). Click “Clone or Download”, and make sure it says “Clone with SSH” in bold in the top left of the pop-up box. If not, click on the blue “Use SSH” button on the top right of the pop-up box. Now copy the link in the box to your clipboard. In the event that the SSH setup above did not work, you can simply navgate to t

4. In RStudio, go to File -> New Project. Click Version Control, then Git. Paste the link you just copied into the Repository URL box. Leave the Project directory name blank. Create this as a subdirectory of your homeworks folder. An RStudio project should now open up, which will allow you to start working on your homework assignment. You will probably see a blank console screen. However, in RStudio you should also see a list of all of the files available. Click on whatever file you want to edit (probably the .Rmd file) and edit away. If you save and close R Studio and want to go back to editing your project, open up R Studio, then go to File -> Open Project. Navigate to the project directory and double click on the .Rproj file.

Note that if you received an error in the above steps, you may have to clone with HTTPS instead of SSH. You can do this by again clicking on the "Clone or Download" button in the repository page, then clicking "Use HTTPS" in the top right of the pop-up box. Now copy the link and repeat this step.

Here is a visualization of cloning an assignment onto your computer through R Studio on a Mac:

![Alt Text](http://g.recordit.co/nKeMWFh4vS.gif)

5. Now you are ready to open code files associated with problem sets, make changes to those files to complete homework assignments, and eventually submit them by 'pushing' to github. Here's some general comments about that process. After you make changes to the homework assignment or make new files, commit them. What are commits you ask? Commits are essentially taking a snapshot of your projects. For example, if I make changes to a code so that it prints "Hello world", and then commit them with an informative message, I can look at the history of my commits and view the code that I wrote at that time. If I made some more changes to the function that resulted in an error, I could go back to the commit where the code was originally working. This prevents you from creating several versions of your homework (homework-v1, homework-v2, ...) or from trying to remember what your code originally looked like.

You can make commits using the GIT toolbar in RStudio (in RStudio make sure the toolbar is visible by doing View -> Show Toolbar).  Click the Commit button in the GIT toolbar dropdown menu. Check the files that you want to commit, enter your commit message, then hit Commit. You can read how to do this (and other stuff related to git and GitHub in RStudio) in more detail here: http://r-pkgs.had.co.nz/git.html#git-init. Here is also a short GIF showing how to do this:

![Alt Text](http://g.recordit.co/96UWQ9Avy2.gif)

Two things about committing. One, you should commit somewhat frequently - think doing so once you have a chunk of code that works and that is enough that you'd be sad if you had to write it again. Two, leave informative commit messages. "Added stuff" will not help you if you're looking at your commit history in a year. A message like "Added initial version of hello-world function" will be more useful. A good general intro to this can be found here: https://r-pkgs.org/git.html#git-commit

6.  At some point you'll want to get the updated version of the assignment files back onto GitHub, either so that teachers can help you with your code, or so that it can be graded. You can do this by using a command called `git push`. If you are ready to push, you can again click on the GIT toolbar dropdown menu in RStudio, and then click `Push branch`. You can also do this after you commit in RStudio by clicking Push in the top right corner of the Commit pop-up box. Here is a visualization of both options:

![Alt Text](http://g.recordit.co/TkOnIVLttw.gif)


### Steps for submitting your first problem set (ps0)

For the first problem set, you have just a couple steps, but it will make sure that everything is working with R, RStudio, git, and GitHub.

1. Once you've opened the assignment files in R studio (step 5 above) find in the files tab on the lower right panel in RStudio the file called something like "problem_set_submission.Rmd". Click on it to open it (it should pop up in the upper left panel). Read through the text within this file.

2. Make a new blank line 17 by putting your cursor just to the left of the text that says summary(cars)' and type this: print("hello world")

3. Save this file by using the save icon in the upper left (or under File > Save). Then click the "Knit" button in the upper left. A new window will pop up - check out the html file that you made and then just close this. 

4. Now in the upper right panel in the git tab, click the check boxes for "problem_set_submission.Rmd" and "problem_set_submisison.html" and then hit the commit button (this is the commit step described in step 5 above). A page will pop up. Add a commit message like "Completed problem set 0" or something into the "Commit message" box and then hit the commit button again to finalize this commit. Lastly, hit the Push (up-facing green arrow) button to push to GitHub. This is how each assignment will be submitted. You'll now be able to see your updated repository (with altered or new files) on your github page.

Note that you can push these files to github multiple times (for example, if you see something else you want to change). Just repeat steps 3 and 4 of this section. Keep in mind that the instructor will download a copy of each student's assignment files at the date and time that assignments are due, so changes can be pushed up to that point.


### Resources
* [Happy Git and GitHub for the useR](http://happygitwithr.com/)
* [The Unix Workbench](http://seankross.com/the-unix-workbench/)
* [Interactive learning guide for Git](http://learngitbranching.js.org/)
* [GitHub Guides](https://guides.github.com/)
* [Git setup for Windows (video)](https://youtu.be/F_fPEMnr1OQ)
* [Git setup for Mac (video)](https://www.youtube.com/watch?v=kbmSZwK0k-A&t)
* [How to clone, edit, and push homework assignments with GitHub Classroom (video)](https://youtu.be/pAcMgGbCtQw)
