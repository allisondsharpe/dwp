<h1> Portfolio Deployment Plan </h1>

This is my deployment plan for my Portfolio site. It outlines the process of putting my site onto the live server via Git.

This plan assumes a simple HTML page and a single git branch. For a more complex site, I would reccommend using multiple branches and merging them together.

    Save all changes in Local Repo

    Commit the changes
        git commit -am "Commit Message Here" to commit the entire project, or git add to specify individual files or groups of files, then git commit -m "Commit Message Here" to commit those changes.
    Push changes to Staging Server
        git push staging
    Test the Site
        This step ensures that the changes you made actually perform like they did in testing. If this isn't the case, determine the problems, fix them in the local repo, and repeat this process from step 1.
    Push changes to Production
        If the site performs as desired, push the changes to production
        git push starkDWP

