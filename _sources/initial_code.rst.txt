Uploading the Pintos code to your repository
--------------------------------------------

Once a repository has been created for you, you must upload the Pintos code into it. To do so, please make sure to follow the steps described in this page. If we make any changes to the Pintos code, it will be easier for you to automatically merge those changes into your code if you uploaded the Pintos code as described in this page.


* If you are new to Git, make sure you've read the `Using Git <git.html>`_ page.
* Make sure you have added your SSH public key to your GitLab account (otherwise, you will only have read-only access to the GitLab server). You can do this in this page: https://mit.cs.uchicago.edu/profile/keys. If you do not know what an SSH key is, or do not know how to generate one, read https://help.github.com/articles/generating-ssh-keys.
* Only one of the team members needs to initialize the repository. In other words, do *not* follow these instructions more than once. Once one of you has initialized the repository, the other team member will be able to simply create a local copy of the (initialized) Git repository that you are both sharing.
* The first thing you need to do is create an empty local repository. In an empty directory, run the following::

        git init

* Next, run the following command, making sure to substitute ``studentA-studentB`` with your repository name::

        REPO_NAME=studentA-studentB
        git remote add origin git@mit.cs.uchicago.edu:mpcs52030-spr-17/$REPO_NAME.git
        git remote add upstream https://github.com/uchicago-cs/pintos.git
        git pull upstream master
        git push -u origin master

At this point, you can just run ``git push`` and ``git pull`` to push/pull to/from your repository on the CS GitLab server.
If we push any changes to the Pintos code itself, you can incorporate it into your code by running ``git pull upstream master``
