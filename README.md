# Simpsons Characters
An example HTML webpage used for the 2019 NIC IMG Git Workshop

## Getting Setup

1. Create a Github account if you don’t have one already. The free plan should be fine for now.

2. Start up Github desktop and sign in to your Github account. If you are working on your personal computer then you’ll need to download it first. You’ll also need to configure git with your name and email.

3. Select “Clone a repository” using `/chris-geelhoed/simpsons-characters` as the URL. You can now set the location on your hard drive that the project will save to, or you can just leave the default.

4. If the clone was successful then you should now have the HTML project saved on your computer. From Github desktop, you should now see options to open the project in a code editor (eg VS Code or Atom), in a file explorer (eg Finder on Mac), and in Github itself.

5. Open the project in VS Code. You might need to change Github Desktop’s preferences to do this. From here you can read and edit the source code of the project that was just cloned. If you are working on a personal computer you can download VS Code for free or you can use your preferred text editor if you have one.

6. Open the project in the file explorer and identify the `index.html` file. Double clicking this should open a Simpsons Characters webpage in the browser.

7. One part of the exercises requires that you push some changes to your own personal remote (not the public `/chris-geelhoed/simpsons-characters` remote, which was used to clone the project originally).

   1. First, login to your personal Github account and create a repository called “simpsons-characters”. There is no need for a description or README, but ensure that the repository is set to private. Also go to settings and set `chris-geelhoed` as a collaborator - this is how I can see your work!

   2. Since our project already has an “origin” remote setup (the one we used to originally clone the project), we can’t use the Github Desktop Quick Setup here. We need to use the command line to change the origin remote repository manually. Click the clipboard button to copy the HTTPS git remote url provided. It should look similar to `https://github.com/chris-geelhoed/simpsons-characters.git`, but with your own Github account name being referenced in place of “chris-geelhoed”.

   3. Open a computer terminal in the project's root directory. This can also be done from VS Code by going to "Terminal" and selecting "New Terminal" from the dropdown.

   4. Type `git remote set-url origin <remote-url>` into your terminal (Make sure to replace `<remote-url>` with the url you copied to your clipboard after setting up a personal repository.) and press enter. This command changes the origin remote from `/chris-geelhoed/simpsons-characters` to your own personal Github repository.

   5. Now if you run `git remote -v` from your terminal you should see the origin remote references your personal Github repo.
   
Congrats! You are now setup to use Github and Github Desktop and can get going on the workshop exercises!

## Exercises

*Please submit the answer to these questions by editing the README and committing those changes to your personal github repository. Ensure that your instructor has the url of your github repository before you leave the workshop.*

1.  A some point in time Bootstrap CSS was included in the project via a public CDN. Browse the repository’s history to identify the SHA hash, commit time, and code changes that correspond to this change. Hint: You don’t need to inspect any HTML or CSS to find this. Instead, refer to the project’s git history.

2.  Find commit `b674e87` and the subsequent commit `c1299a8` in the project’s history. Which commit message do you think is better? Why? Hint: Imagine that these changes were made by a teammate or coworker. Which commit would be more helpful to you?

3.  Public websites often use “meta tags” to control how content is displayed on social media websites like Facebook or Twitter. Add the following lines of code to the main head tag of `index.html`, right below the final stylesheet reference. This will ensure that “The Simpsons Characters” will be taken as the page title.
```
<meta property="og:title" content="The Simpsons Characters">
<meta property="og:description" content="A list of notable Simpsons characters">
```

   Commit these changes and push to the master branch of your personal remote repository.

4.  Use Github Desktop to change your current branch from `master` to `feature/family` (This is called "Checking out" a branch). What differences do you see between this branch and the master branch? You might notice that the width of these new characters are not proportional with each other. Keeping Marge at the preset 59px, edit the widths of the other characters from the `styles.css` file. Commit these changes and push them to the `feature/family` branch of your personal remote repository.

5.  Tech giants like Facebook, Twitter, and Google all use version control systems to manage their projects (Be that Git, another commercially available option like Mercurial, or an internally developed alternative), but they don’t make most of their code publicly available online. Why do you think this is?
