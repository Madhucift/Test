# Test

This is a test repository to ensure that you are able to download a repository from R.

# Set-up Instructions for the Course

## Get an account on GitHub

If you don't already have an account on GitHub, go to [github.com](github.com) and click the "sign up" link near upper right 
of the page.  It is pretty self-explanatory.  Go ahead and get a **free** account.  

The free GitHub account does not have private repositories.  Everything is public and viewable.  You can upgrade (for money) and get private repositories.  Or _if you are a student_, you can get private repositories from GitHub for free.  Go to [https://education.github.com/pack](https://education.github.com/pack) to sign up for your free student pack.  You will need to upload proof that you are a student or faculty.

## Install GitHub Desktop

1. Go to [desktop.github.com](https://desktop.github.com/) and install.
2. Open GitHub Desktop, go to 'GitHub Desktop > Preferences' menu.  
3. Under 'Accounts', sign into your GitHub account.
3. Under 'Git', enter your name (or initials) and the email you used for your GitHub account.

## Install RStudio and R

1. **RStudio:** Install the latest "development" version of RStudio becuase it has features that we may want to use during this course.  Get it from [https://www.rstudio.com/products/rstudio/download/preview/](https://www.rstudio.com/products/rstudio/download/preview/) and install the appropriate one for your OS.

1. **R:**  Make sure you have the latest version of R.  
Go to [https://cran.r-project.org/](https://cran.r-project.org/) and find the download link for your computer system.

1. **bookdown:** package.  We want the latest development version, which 
can be obtained from GitHub by issuing the following commans at the R prompt (i.e. in the console window of RStudio:)
```{r get-bd, eval=FALSE}
install.packages("devtools")  
devtools::install_github("rstudio/bookdown")
```

1. Install **other packages** that we are going to be need. I have created a package on GitHub that declares the packages you will need. When you install this it will install the packages you need.

```{r get-packages, eval=FALSE}
devtools::install_github("RVerse-Tutorials/RWorkflowsetup")
```

## Create a workshop folder

Create a folder/directory on your computer for the workshop materials.  You can create it anywhere you want.  But name it `RWorkflow` just so we all use the same folder name for the workshop.

## Disqus forum

I have added a Disqus forum to the course website.  [Create an account](https://disqus.com/) if you would like to be able to add comments/questions.  This will allow people to pose questions to the group and allow me (and others) to answer.

## Downloading repositories

You will need to download repositories from [RVerse-Tutorials](https://github.com/RVerse-Tutorials) for many of the labs.  There are a few ways that you can do this.

### Method #1 Download from within R

This is the method I will show. Here is code to download the repository 'Test' from with R.  For others, just change the name of the repository.

```
library(RWorkflowsetup)
repo = "Test"
download.repo(repo)
```

### Method #2

1. From RStudio, go to the menu option
'File->New Project...'. Then from the resulting dialog, choose
"Version Control".  Then choose "Git".  Then it asks for a "repository URL".
Supply this: `https://github.com/RVerse-Tutorials/Test` and 
leave the "Project Directory Name" empty.  And then choose a directory 
in which to put it and click OK.

2. Click on the 'More' link in the Git Window of RStudio, and click 'Shell'.  Then issue this command.
```
git remote rm origin
```
This detaches the cloned repository from the remote repository on GitHub from where you cloned it. That will pull the RStudio project off of GitHub, make a local clone
of it on your hard drive and open.

### Method #3

Go to https://github.com/RVerse-Tutorials/Test and click 'Clone or download' and chose 'Download Zip'.  Unzip and you'll probably want to remove  'master' added to the end of the repository name.

If you chose, 'Clone in Desktop', you'll need to open a terminal window, navigate to the new folder you just downloaded, and run the git code `git remote rm origin` from within the terminal to detach the repository from the RVerse-Tutorials GitHub account.
