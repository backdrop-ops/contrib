Backdrop Contributed Project Group Application
==============================================

Interested in joining the growing Backdrop contributor community at
https://github.com/backdrop-contrib?

To apply simply create a request as an issue at
https://github.com/backdrop-ops/contrib/issues/new.

Please note: It is completely optional to post your modules, themes, or layouts
in the Backdrop contrib group.

If you have started writing or porting a project for Backdrop, please include a
link to the module, theme, or layout you have written. If you have posted the
code under your own GitHub account you will be able to easily transfer the
entire repository to live under
`https://github.com/backdrop-contrib/[your_project_name]` after joining the
Backdrop Contributed Project Group.

Benefits of joining:

- Benefit from official security procedures for keeping your code healthy.
- Version information packaged into GitHub download automatically.
- Co-maintain your project with other Backdrop contrib developers.
- Share the responsibilities of managing all the issue queues.
- Collaborate with the larger Backdrop community.

Requirements to join:

- You must agree to the Backdrop Contributed Project Agreement, below.
- You must either submit your first Backdrop project for a quick spot-check /
  review, or submit links to PRs or commits to existing Backdrop projects.
- If you are not submitting code for review at the time of application (for the
  purposes of managing issues) you must have at least one recommendation from a
  person who is already a member of the Backdrop contrib group.

Rejected applications:

- No rejected application to the Backdrop contrib group is final.
- In the rare case that your application is rejected, you are welcome to reapply
  after a waiting period of 1 month.
- After 1 month has passed, please open a new issue in the queue and try again.
- Please carefully review the reason for rejection so that history does not
  repeat itself.

New Project Checklist
---------------------

All projects must meet these minimum requirements.

- [ ] Include a README.md file that includes license and maintainer information.
You can use [this example](https://raw.githubusercontent.com/backdrop-ops/contrib/master/examples/README.md).
- [ ] Include a LICENSE.txt file that indicates the contributed code is GPL v2
      (or in some cases, GPLv3).
  * Please use [this text for GPL v2](https://raw.githubusercontent.com/backdrop-ops/contrib/master/examples/LICENSE.txt).
  * If your project includes a library that is GPL v3 then you must license your
    project as GPL v3. The GPL v3 license will prevent your project from being
    included in Backdrop core in the future, so please only use this license
    when necessary. You may use [this text for GPL v3](https://raw.githubusercontent.com/backdrop-ops/contrib/master/examples/LICENSE=GPLv3.txt).
- [ ] Maintain the Git history from Drupal 7. See
[this article](http://tag1consulting.com/blog/how-maintain-contrib-modules-drupal-and-backdrop-same-time-part-2).

Backdrop Contributed Project Agreement
--------------------------------------

By joining the [Backdrop Contributed Project Group](https://github.com/backdrop-contrib)
(Backdrop Contrib, for short) you agree to the following:

1. You will not push changes to a repository for which you are not a current
   maintainer (even though joining the Backdrop Contrib group will grant you
   access to push to any project within).

1. You must agree to license your code contributions as GPLv2 or later.

1. Any project you create or maintain must include a copy of the [GPL v2
   `LICENSE.txt` file](https://github.com/backdrop-ops/contrib/blob/master/examples/LICENSE.txt)
   in the root of your repository. The GPLv2 license applies to all code that
   directly interacts with parts of Backdrop licensed as GPLv2 or later. See the
   [Backdrop License FAQ](https://backdropcms.org/license) for a more detailed
   explanation.

1. You must confirm that you have the right to distribute any additional code,
   libraries, images, fonts or other assets written or created by any third
   party with code licensed as GPLv2 or later.

1. Any project you create or maintain must include a `README.md` file containing
   at the least the following:
    1. A description of the project
    1. Basic documentation
    1. License information for the project (GPL v2)
    1. License information for any additional assets (SIL OFL fonts, CC-SA
       images, etc)
    1. A list of the current maintainers for the Backdrop project
    1. Credits acknowledging past maintainers for the Backdrop or Drupal
       projects

   You may use this [example README.md](https://github.com/backdrop-ops/contrib/blob/master/examples/README.md)
   to get started.

1. You will work with the Backdrop Security Team to address any vulnerabilities
   in any project you create or maintain, if necessary.

1. Any project you create or maintain will have the GitHub issue tracker enabled
   for official communication.

1. If any of the above requirements are not met, your access to the Backdrop
   Contrib group -- including all projects and even those that you may have
   originally authored -- may be revoked.

1. If your project becomes abandoned and you do not respond to an issue to grant
   a new maintainer within 2 weeks, your project may be modified by a Backdrop
   Contrib Administrator to add a new maintainer, without your explicit consent.

Additional Notes For Non-coders
-------------------------------

1. If an applicant is not (yet) a coder but would still like access to the
   contrib group (for example, for updating documentation or managing issue
   queues) the applicant must get at least one recommendation from another
   person who already has commit access to the contrib group.

1. Any non-coder applicant still agrees to the same contributed project author
   agreement as coders (above).

1. Any non-coder applicant needs to additionally promise that should they ever
   wish to author new code in the Backdrop contrib group, they will also undergo
   the same code spot-check process a new contributor needs to undergo at the
   time they add the code.

What To Do After Your Application Is Accepted
---------------------------------------------
When you are ready:

1. Clean up your project as much as possible.

1. If you started your project with a title like "backdrop-port-of-xyz", change
   the name of the project to exactly match the Drupal project (e.g. "xyz").

1. Transfer the project to the backdrop-contrib organization following the steps
   mentioned [in this post](https://help.github.com/articles/transferring-a-repository-owned-by-your-personal-account/#transferring-to-an-organization).
    1. After clicking 'I understand, transfer this repository', you'll be shown
       the 'Team Access' screen where you choose who will have access to this
       repo. Tick both 'Authors' and 'Security', then click 'Transfer'.
    1. Visit the repository's new page, and go to 'Settings'.
    1. Click 'Collaborators & teams' in the left menu.
    1. Under 'Teams', set 'Authors' to Admin and 'Security' to Write.

1. If your repository has a 'master' branch, you'll need to create a new
   '1.x-1.x' branch to replace it:
    1. Create the new '1.x-1.x' branch
       ```
       git checkout master
       git pull origin master
       git checkout -b 1.x-1.x
       git push origin 1.x-1.x
       ```
    1. Go to 'Settings' in the GitHib repo and click 'Branches' in the left
       menu.
    1. Change the default branch from 'master' to '1.x-1.x'.
    1. Delete the 'master' branch
       `git push origin --delete master`

1. Tag [a release](https://help.github.com/articles/creating-releases/). You
   must tag a release in the format of "1.x-1.0.0" for the packaging script to
   work. You can see right away on the release page if there was an error during
   the packaging process. If successful, your ported project should appear on
   the [modules listing page](https://backdropcms.org/modules) or the
   [themes listing page](https://backdropcms.org/themes) on BackdropCMS.org.

1. Make sure you are subscribed to notifications for the project's issues. The
   GitHub issue queue is where all the communication for your project happens,
   and when new issues are created, you need to know about them and respond in a
   timely manner otherwise your project might be considered abandoned following
   the procedure listed below.

1. If your project is a port of a Drupal project, it's considered a best
   practice to subscribe to the issue queue on drupal.org. That way you can be
   updated when issues are fixed. You can then decide if you want any of those
   commits in your project. Similarly, if you fix bugs or or add new features,
   please consider letting the maintainer(s) of the original project know about
   it. It would be even better to post a patch in the Drupal queue for them to
   review. If you have found a security issue that applies to both, please try
   to coordinate the release of the fix with the maintainers of the original
   project **through non-public channels** so that potential attackers do not
   take advantage of either Backdrop or Drupal sites.


Abandoned Projects
------------------

You may apply to adopt an abandoned project. The procedure is as follows:

1. If you haven't already, please join the Backdrop Contrib group by submitting
   an application (see above).

1. File an issue with the current project requesting to help maintain the
   project.

  - If written permission is granted by a current maintainer, create a PR that
    adds your name to the README.md file in the list of maintainers.
  - If a current maintainer does not respond within 2 weeks, [create an issue
    in this repository](https://github.com/backdrop-ops/contrib/issues/new)
    to take over the project. Please include a link to the issue you filed with
    the abandoned project.

1. After confirming the project has been abandoned, a Backdrop Contrib
   administrator will add your name to the list of maintainers in that project's
   README.md file.

1. You may now maintain the project directly as though given permission by the
   project maintainers, and likewise now grant permission to others to maintain
   the project.
