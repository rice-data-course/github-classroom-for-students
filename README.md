# GitHub Classroom Guide for Students

This is a guide for students to setup Git and GitHub for use with GitHub Classroom. We use RStudio in our class, so we will give instructions on how to use RStudio to setup Git locally. However, this is not necessary.

### Steps for getting setup with GitHub
1. Register for account on GitHub (https://github.com/). We recommend using a username that incorporates your name (jfiksel, mtaub, lrjager)

2. Download RStudio (https://www.rstudio.com/) and R (https://cran.r-project.org/)

3. Install Git. Directions for both Windows & Mac here: http://happygitwithr.com/install-git.html. Windows users should follow Option 1 in 7.2. Mac users can follow Option 1 in 7.3 if comfortable, otherwise follow Option 2. Below, I show how you would access the terminal on a Mac, as well as how to enter the commands given in the link. Windows users should consult the video posted under Resources

![Alt Text](http://g.recordit.co/ENAZXCmgs9.gif)

4. Setup options in Git. In you have a Mac, open up the shell in R Studio by clicking Tools -> Shell. If you don't want to enter RStudio, you can go to the terminal if you have a Mac (Applications -> Utilities -> Terminal) as shown above. If you have a Windows, open Git BASH, which you should have downloaded in step 3. Enter the three lines of code here: http://happygitwithr.com/hello-git.html, changing the first two lines to your own name and email (this should be the email associated with your GitHub account). Note that Windows users should read section 8.1 in the above link carefully. Below is an example of what this process looks like on a Mac:

![Alt Text](http://g.recordit.co/ibUp6dYimU.gif)

5. Generate a SSH key so you don’t need to enter your password every time you interact with GitHub. First check to see if you have a SSH key. Go into the shell (again, either through RStudio, Terminal for Mac, or Git Bash for Windows) and complete on this page http://happygitwithr.com/ssh-keys.html, which is Chapter 12 in Happy Git with R. The instructions are quite thorough, so if you want to follow along with a visualization, I recommend watching the Git setup videos under resources. This is covered starting at 9:32 in the Mac video and 9:18 in the Windows video.

6. Follow the instructions here (http://happygitwithr.com/push-pull-github.html) to ensure you can connect to GitHub from your computer. Here are step-by-step GIFs from a Mac that help visualize this process.


### Steps for downloading and editing assignments from GitHub Classroom

1. Make a folder specifically for this class (maybe something like bios-338). 

2.  You will receive link to an assignment for each new assignment. Follow the instructions for getting the homework repository set up. You should now have a repository for this homework. Note that after you accept an assignment for the first time, we will send you an invite to join the classroom organization as a member. Please accept this. You will probably get an email with the invitation, but you should also see a link at the top of your main GitHub page. Here is an image of what you should see after clicking the link:

![Alt Text](img/accept-assignment.png)

3. Enter the homework repository on GitHub (this is online--GitHub is different from Git!). Click “Clone or Download”, and make sure it says “Clone with SSH” in bold in the top left of the pop-up box. If not, click on the blue “Use SSH” button on the top right of the pop-up box. Now copy the link in the box to your clipboard.

4.  In RStudio, go to File -> New Project. Click Version Control, then Git. Paste the link you just copied into the Repository URL box. Leave the Project directory name blank. Create this as a subdirectory of your homeworks folder. An RStudio project should now open up, which will allow you to start working on your homework assignment. You will probably see a blank console screen. However, in RStudio you should also see a list of all of the files available. Click on whatever file you want to edit (probably the .Rmd file) and edit away. If you save and close R Studio and want to go back to editing your project, open up R Studio, then go to File -> Open Project. Navigate to the project directory and double click on the .Rproj file.

Note that if you received an error in the above steps, you may have to clone with HTTPS instead of SSH. You can do this by again clicking on the "Clone or Download" button in the repository page, then clicking "Use HTTPS" in the top right of the pop-up box. Now copy the link and repeat this step.

Here is a visualization of cloning an assignment onto your computer through R Studio on a Mac:

![Alt Text](http://g.recordit.co/nKeMWFh4vS.gif)

5.  After you make changes to the homework assignment, commit them. What are commits you ask? Commits are essentially taking a snapshot of your projects. For example, if I make changes to a code so that it prints "Hello world", and then commit them with an informative message, I can look at the history of my commits and view the code that I wrote at that time. If I made some more changes to the function that resulted in an error, I could go back to the commit where the code was originally working. This prevents you from creating several versions of your homework (homework-v1, homework-v2, ...) or from trying to remember what your code originally looked like.

You can make commits using the GIT toolbar in RStudio (in RStudio make sure the toolbar is visible by doing View -> Show Toolbar). I have made a video on how to do this here (available under resources--How to clone, edit, and push homework assignments with GitHub Classroom), and you can read how to do  this in RStudio in more detail here: http://r-pkgs.had.co.nz/git.html#git-init.  Click the Commit button in the GIT toolbar dropdown menu. Check the files that you want to commit, enter your commit message, then hit Commit. Here is also a short GIF showing how to do this:

![Alt Text](http://g.recordit.co/96UWQ9Avy2.gif)

Two things about committing. One, you should commit somewhat frequently - think doing so once you have a chunk of code that works and that is enough that you'd be sad if you had to write it again. Two, leave informative commit messages. "Added stuff" will not help you if you're looking at your commit history in a year. A message like "Added initial version of hello-world function" will be more useful.

6.  At some point you'll want to get the updated version of the assignment back onto GitHub, either so that teachers/TAs can help you with your code, or so that it can be graded. You can do this by using a command called `git push`. If you are ready to push, you can again click on the GIT toolbar dropdown menu in RStudio, and then click `Push branch`. You can also do this after you commit in RStudio by clicking Push in the top right corner of the Commit pop-up box. Here is a visualization of both options:

![Alt Text](http://g.recordit.co/TkOnIVLttw.gif)

### Resources
* [Happy Git and GitHub for the useR](http://happygitwithr.com/)
* [The Unix Workbench](http://seankross.com/the-unix-workbench/)
* [Interactive learning guide for Git](http://learngitbranching.js.org/)
* [GitHub Guides](https://guides.github.com/)
* [Git setup for Windows (video)](https://youtu.be/F_fPEMnr1OQ)
* [Git setup for Mac (video)](https://www.youtube.com/watch?v=kbmSZwK0k-A&t)
* [How to clone, edit, and push homework assignments with GitHub Classroom (video)](https://youtu.be/pAcMgGbCtQw)
