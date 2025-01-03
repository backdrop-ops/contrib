Backdrop Contributed Project Group Application
==============================================

Join the growing Backdrop contributor community at
https://github.com/backdrop-contrib.

To apply, create a request as an issue in this queue:
[https://github.com/backdrop-ops/contrib/issues/new](https://github.com/backdrop-ops/contrib/issues/new?assignees=klonos&labels=Maintainer+application&template=application--contrib-group.md&title=Contrib+Group+Application%3A)

If you have started writing or porting a project for Backdrop, please include a
link to the module, theme, or layout. If you have posted the code under your
own GitHub account you will be able to easily transfer the entire repository
to live under `https://github.com/backdrop-contrib/[your_project_name]` after
joining the Backdrop Contributed Project Group.

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

- [ ] Maintain the Git history from Drupal 7. See
    [this article](http://tag1consulting.com/blog/how-maintain-contrib-modules-drupal-and-backdrop-same-time-part-2).
- [ ] Include a README.md file that includes license and maintainer information.
    You can use [this example](https://raw.githubusercontent.com/backdrop-ops/contrib/master/examples/README.md).
- [ ] Include a LICENSE.txt file that indicates the contributed code is GPL-2.0
    (or in rare cases GPL-3.0 -- please see below). Please use [this text for GPL-2.0](https://raw.githubusercontent.com/backdrop-ops/contrib/master/examples/LICENSE.txt).
  * If your project includes a library that is licensed under GPL-3.0, LGPL-3.0,
    Apache-2.0, AGPL-3, or any other license that the Free Software Foundation
    has determined to [only be compatible with GPL-3.0](http://www.gnu.org/licenses/license-list.html#GPLCompatibleLicenses),
    then you must license your project as GPL-3.0. Please use [this text for GPL-3.0](https://raw.githubusercontent.com/backdrop-ops/contrib/master/examples/LICENSE-GPL-3-0.txt).
  * The GPL-3.0 license will prevent your project from one day being included in
    Backdrop core, so please only use this license when necessary.

Backdrop Contributed Project Agreement
--------------------------------------

By joining the [Backdrop Contributed Project Group](https://github.com/backdrop-contrib)
(Backdrop Contrib, for short) you agree to the following:

1. You will not push changes to a repository for which you are not a current
   maintainer (even though joining the Backdrop Contrib group will grant you
   access to push to any project within).

1. You must agree to license your code contributions as GPLv2 or later.

1. Any project you create or maintain must include a copy of the [GPL-2.0
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
    1. License information for the project (GPL-2.0)
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

1. Clean up your code so it's ready for community collaboration.

1. If you started your project with a title like "backdrop-port-of-xyz", change
   the name of the project to exactly match the Drupal project (e.g. "xyz").

1. Transfer the project to the backdrop-contrib organization following the steps
   mentioned [in this post](https://help.github.com/articles/transferring-a-repository-owned-by-your-personal-account/#transferring-to-an-organization).
    1. After clicking 'I understand, transfer this repository', you'll be shown
       the 'Team Access' screen where you choose who will have access to this
       repo. Tick 'Authors' and 'Security' and 'Bug Squad' then click 'Transfer'.
    1. Visit the repository's new page, and go to 'Settings'.
    1. Click 'Collaborators & teams' in the left menu.
    1. Under 'Teams', set 'Authors' to Triage, 'Security' to Admin and 'Bug Squad' to Write.

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

1. Make sure you are subscribed to notifications for the project's issues. The
   GitHub issue queue is where all the communication for your project happens,
   and when new issues are created, you need to know about them and respond in a
   timely manner otherwise your project might be considered abandoned following
   the procedure listed below.

1. If your project is a port of a Drupal project, it is a best practice to
   subscribe to the issue queue on drupal.org. That way you can be updated when
   issues are fixed. You can then decide if you want any of those commits in
   your project. Similarly, if you fix bugs or or add new features, please
   consider letting the maintainer(s) of the original project know about it.
   It would be even better to post a patch in the Drupal queue for them to
   review. If you have found a security issue that applies to both, please try
   to coordinate the release of the fix with the maintainers of the original
   project **through non-public channels** so that potential attackers do not
   take advantage of either Backdrop or Drupal sites.


Releases
--------

Backdrop uses the GitHub release system to distribute its modules, themes and layouts.  

For an asset to be released by GitHub, it must have a git tag, because GitHub uses the  tag to generate the version (and file name) of the release. Backdrop conforms to the Semantic Versioning Format in terms of its tags; a 3 digit version number along with an optional suffix [Learn more about Semantic Versioning](https://www.baeldung.com/cs/semantic-versioning).   

Here are some examples:
- The simplest tag/version expresses the fact that a **new** Backdrop asset is now production grade and ready for release.  In the following example, a newly crafted production-grade Backdrop asset is being released for the first time ("1.x-1.0.0").
- A slightly more complicated tag/version expresses the fact that the asset has been **imported** from some other system.  The following example features a version 3.x Drupal asset that was ported over to Backdrop, with its tag/version indicating as such ("1.x-3.0.0").  
- The most complex tag/version handles the situation of a **premature** release.  This happens in order to solicit or enable feedback,  programming assistance, documentation support or testing from others.  Premature releases must feature a tag/version that clearly indicates they are premature ("alpha", "beta", ...), coupled with a tracking number that indicates their pre-production iteration ("1", "2", ...).  In the following two examples, Backdrop assets are being released prematurely, with their tag/version numbers clearly indicating that they should be approached with caution ("1.x-1.0.0-alpha1", "1.x-3.0.0-beta2").

The most common order of operations is as follows:
  1. Add a tag using `git tag 1.x-1.0.0`
  1. Push the tag up to the contrib repository.
  1. Visit the page for the tag in GitHub and
[create a release from that page](https://docs.github.com/en/repositories/releasing-projects-on-github/managing-releases-in-a-repository).
  1. Wait. This process can take anywhere 5 seconds to 5 minutes.
  1. Refresh the GitHub release page. You should see a "Download XYZ" link appear.

If successful, your project should appear on
the [modules](https://backdropcms.org/modules),
[themes](https://backdropcms.org/themes) or [layouts](https://backdropcms.org/layouts)
listing pages on BackdropCMS.org.

If there was an error during the packaging process, an error message from the
packager will be attached instead.


Security Releases
-----------------

You will need to work with the Backdrop Security Team in order to make a
security release for your project. Please contact security@backdropcms.org to
begin this process. Please see the [Security Release Documentation](https://docs.backdropcms.org/documentation/security-releases)
for more details.


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
