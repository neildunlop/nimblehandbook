---
sidebar_label: 'Knowledge Base - How To'
---

# Maintaining the Knowledge Base
There are a couple of different ways to edit existing pages and add new pages to the Knowledge Base. The most flexible approach is to edit the site on your own machine. This takes a little setup, but once you're familiar you'll be able to get lots done quickly and easily.

##  Getting Setup

1. Install [Visual Studio Code](https://code.visualstudio.com/download).
2. Install [NPM](https://nodejs.org/en) - choose whichever version has 'LTS' in its name.
2. Install [Git](https://gitforwindows.org/)
3. Open the Windows Command Prompt and navigate to a suitable directory to place the Knowledge Base folder. 'C:\Dev' for example.
4. Checkout the Knowledge Base repository with the command `git clone https://Robiquity@dev.azure.com/Robiquity/kb/_git/kb`

You will now have a full copy of the Knowledge Base on your local machine in that target directory.  From here you can make as many local changes as you like, run the site locally, and check any changes you make before pushing back to the production site.

##  Running the Site Locally

1. Navigate to where you checked out the Knowledge Base Repository (`C:\Dev` for example).
2. Navigate to the sites root directory with `cd kb\www`
3. If this is the first time you've run the knowledge base, run `npm install` to download and install all the site dependencies.
4. To run the site, use `npm start` - after a short time you should be able to view the site in your browser using `http://localhost:3000`.

## Knowledge Base Basics

* All of the pages in the Knowledge Base are stored as Markdown documents, which means you only have a limited set of options for formatting the content.  We're aiming for substance over style!
* All of the pages are stored in a folder structure the 'docs' folder. `C:\Dev\kb\www\docs` Adding folders and files here will add new pages to the Knowledge Base.
* All of the images are stored in a folder structure the 'static\img' folder. `C:\Dev\kb\www\static\img` Adding pictures here will make them available for use in pages.
 
## Adding a Page and Committing it to Production

### Getting Set Up
Visual Studio Code is a convenient tool for editing the Knowledge Base and committing the changes, all in one place. The process for getting setup is as follows:

1. Open Visual Studio Code.
2. Click on 'File |  Open Folder' and select the `C:\Dev\kb` folder.
3. The site should appear in Visual Studio Code.
4. From the menu at the top of the Visual Studio Code window, click `Terminal` and choose `New Terminal`.
5. A new Terminal pane will appear at the bottom of the window.

### Making a Branch
All changes to the knowledge base need to go through a quick review before they make it to the live site. This process is known as a 'Pull Request'.  

The basic process for making changes, including making the pull request is as follows:

1. In the terminal, type `git pull` to retrieve all the changes that have been made to the remote repository and copy them to your instance. (This makes sure your local copy of the site is up to date before you make any changes. It's always worth doing this before you start making changes. Git can usually automatically handle resolving things when two people change the same file, but keep things in synch as often as possible makes life easier.) 
2. Make a new branch for your work with `git checkout -b name_of_your_branch`.  'name_of_branch' should be something short that reflects what you're doing, for example: `git checkout -b technique_folder_restructure`.

### Making Your Changes
3. Add your files and make and edits to content that you need.

### Checking Things Still Work
Its always a good idea to run things on your own machine to make sure everything works as expected, before you commit any changes.

4. In the terminal, type `npm start` to run the site locally and check your changes are as expected.
5. Once you're happy, in the terminal, type `CTRL-C` to stop the process.

### Committing Changes

6. In the terminal, type `git status` and you should see a list of all the files you've modified. If there is nothing in the list, you've probably forgotten to save the file you've been working on.
7. In the terminal, type `git add .` to add all your newly created or modified files to a local git staging area. (This basically tells git that it should care about these files and track any changes that are made to them).
8. Commit your changes to the local repository with `git commit -m"&lt;suitable message&gt;" (make sure your commit message describes the change you're making. This is how reviewers will get an idea of what your change is about.) (this commits the added / changed files to a local snapshot of the repository. The -m element is known as the commit message and lets others know what you did. You should try and make your commit messages useful).
9. In the terminal, type `git push`. (this synchronises the remote git repository, that everyone uses, with your local snapshot).    
10. You may get an error message:

```
fatal: The current branch technique_folder_restructure has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin <name_of_branch>

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.
```

11. To fix this just enter `git push --set-upstream <name_of_branch>` (where &lt;name_of_branch&gt; is replaced with the actual name of your branch)

### Raising a Pull Request

12. In a web browser, navigate to the Azure DevOps repository: https://dev.azure.com/Robiquity/kb/_git/kb
13. Click on 'Pull Requests' in the left hand menu.
14. In the list in the main area of the screen, you will see an entry for the branch that you just pushed.
15. Click on the 'Create Pull Request' button.
16. If you provided a reasonable branch name and commit message, you'll find a lot of the fields filled in.
17. In the Reviewers box, select two people from the list that you would like to review your submission and click 'Create'.
18. Click the 'Auto Complete' button at the top right of the screen. 

Your chosen reviewers will now be emailed and asked to review your changes. They may contact you to ask you to make some changes to your submission.

Once they approve the PR, because you selected auto-complete, the changes will be merged with the main branch and a build started to deploy the changes to the production site. 