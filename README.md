Backdrop Contributed Project Group Application
==============================================

[Apply to join](https://github.com/backdrop-ops/contrib#backdrop-contributed-project-group-application)
the growing [Backdrop contributor community](https://github.com/backdrop-contrib).

If you have started writing or porting a project for Backdrop, please post the
module, theme, or layout under your own GitHub account, and provide a link in
your application. You will be able to easily transfer the entire repository to
the backdrop-contrib GitHub group after you are a member.

You can learn more about
[the application process](https://backdropcms.org/contribute/add-ons)
on backdropcms.org.


New Project Checklist
---------------------

All projects must meet these minimum requirements.

- [ ] If porting a Drupal project, Maintain the Git history from Drupal 7. See
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

1. You will not push changes, merge PRs, or create releases for a repository for
   which you are not a current maintainer (unless you are a member of the
   `Backdrop Bug Squad`).

1. You must agree to license your code contributions as GPL-2.0 or GPL-3.0.

1. Any project you create or maintain must include a copy of the GPL-2.0 or
   GPL-3.0 `LICENSE.txt` file in the root of your repository. The GPL license
   applies to all code that directly interacts with parts of Backdrop licensed
   as GPL-2.0 or GPL-3.0. See the [Backdrop License FAQ](https://backdropcms.org/license)
   for a more detailed explanation.

1. You must confirm that you have the right to distribute any additional code,
   libraries, images, fonts or other assets written or created by any third
   party with code licensed as GPL-2.0 or GPL-3.0.

1. Any project you create or maintain must include a `README.md` file containing
   at the least the following:
    1. A description of the project
    1. Basic documentation or installation instructions.
    1. License information for the project (GPL-2.0 or GPL-3.0)
    1. License information for any additional assets (SIL OFL fonts, CC-SA
       images, etc)
    1. A list of the current maintainers for the Backdrop project
    1. Credits acknowledging past maintainers, creators, and others worthy.

   You may use this [example README.md](https://github.com/backdrop-ops/contrib/blob/master/examples/README.md)
   to get started.

1. Any project you create or maintain will have the GitHub issue tracker enabled
   for official communication.

1. You will work with the `Backdrop Security Team` to address any vulnerabilities
   in any project you create or maintain, if necessary.

   * If you are not available the day a security release is needed (usually a
     Wednesday), you understand that the `Backdrop Security Team` may create a
     security release on your behalf.

1. You will work with the Backdrop Community to review issues in the queue
   and submitted Pull Requests.

   * If your project has Pull Requests for issues that are tagged "Bug" that have
     been marked "Reviewed and Tested By the Community" for a period of 2 weeks
     or more, a member of the `Backdrop Bug Squad` may merge the pull request
     on your behalf.
   * If the bug is severe enough the `Backdrop Bug Squad` may also create a new
     release for your project.

1. If any of the above requirements are not met, your access to the Backdrop
   Contrib group -- including all projects and even those that you may have
   originally authored -- may be revoked.

1. If your project becomes Abandoned and you do not respond to an issue to grant
   a new maintainer within 2 weeks, your project may be modified by a Backdrop
   Contrib Administrator without your explicit consent, to add a new maintainer.

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

1. Clean up your code so it's ready for community collaboration.

1. If you started your project with a title like `backdrop-port-of-xyz`, change
   the name of the project to exactly match the Drupal project (e.g. `xyz`).

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

1. Make sure you are subscribed to notifications for the project's issues. The
   GitHub issue queue is where all the communication for your project happens,
   and when new issues are created, you need to know about them and respond in a
   timely manner otherwise your project might be considered abandoned following
   the procedure listed below.

1. If your project is a port of a Drupal project, it is a best practice to
   subscribe to the issue queue on drupal.org. That way you can be updated when
   issues are fixed. You can then decide if you want any of those commits in
   your project.
   * If you fix bugs or or add new features, please consider letting
     the maintainer(s) of the original project know about it. You might post
     your patches in the Drupal queue for the other project to consider.
   * If you have found a security issue that applies to both projects, please
     coordinate the release of the fix with the maintainers of the original
     project **through non-public channels** so that potential attackers can not
     take advantage of either Backdrop or Drupal sites.


Releases
--------

Tag [a release](https://help.github.com/articles/creating-releases/). You must
tag a release in the format of "1.x-1.0.0" for the packaging script to work.
You can see right away on the release page if there was an error during the
packaging process. If successful, your ported project should appear on the
[modules listing page](https://backdropcms.org/modules) or the
[themes listing page](https://backdropcms.org/themes) on BackdropCMS.org.


Security Releases
-----------------

You will need to work with the Backdrop Security Team in order to make a
security release for your project. Please contact security@backdropcms.org to
begin this process.

You and the security team will choose a Wednesday to coordinate the release, and
on that day, when you publish the release on GitHub, someone from the Backdrop
Security Team will need to update the project release node on backdropcms.org to
inidciate that a release is a security release.


The Backdrop Bug Squad
----------------------

The `Backdrop Bug Squad` consists of trusted members of the backdrop-contrib
group who will help contributors stay on top of minor bug fixes and User
Interface improvements.

Find out more about the
[Backdrop bug squad](https://backdropcms.org/contribute/bug-squad) on
backdropcms.org.

You may apply to become a member of the Backdrop Bug Squad. Please
[create an issue in this repository](https://github.com/backdrop-ops/contrib/issues/new)
requesting to join.

GitHub members can can be view The Bug Squad team, here:
https://github.com/orgs/backdrop-contrib/teams/bug-squad/members


Abandoned Projects
------------------

A project is considered Abandoned when there is no maintainer listed in the
`README.md` file.

The ony people who can make changes to an abandoned project are the `Backdrop
Security Team` and the `Backdrop Bug Squad`.

An abandoned project will not have any new releases other than a secutity
release issued by the `Backdrop Security Team` or a bug-fix release issued
by the `Backdrop Bug Squad`. A project must have a current maintainer listed in
the `README.md` file to have a new release containing new features, or any
substantial changes.


Determining Abandoned Projects
------------------------------

If you believe that a project has been abandoned but there is a maintainer
listed in the `README.md` file, you can open an issue asking the maintainer if
the project is abadoned.

- If the maintainer responds within 2 weeks, the project has not been abandoned.
- If the maintainer does NOT respond within 2 weeks, you can [create an issue in this repository](https://github.com/backdrop-ops/contrib/issues/new)
  to request that the maintainer's name be removed from the `README.md` file.
  Please include a link to the issue you filed for the project.
- Please understand that removing all maintainers will halt all forward
  progress for the project, as no new releases will be allowed until there is at
  least one maintainer listed again.
- Other options include:
  * Offer to co-maintain the project with the current maintainer.
  * Locate another person who would be willing to co-maintain the project.
  * Offer to take over maintainership of the project.
  * Locate another person who would be willing to take over maintainership of
    the project.

If you are unhappy with the speed of progress or the amount of work being done
on a particular project, you might want to offer to co-maintain the project,
at least for a little while, to help move things along.


Adopting Abandoned Projects
---------------------------

You may apply to adopt an abandoned project. The procedure is as follows:

1. If you haven't already, please join the Backdrop Contrib group by submitting
   an application (see above).

1. File an issue with the current project requesting to help maintain the
   project.

  - If written permission is granted by a current maintainer, create a PR that
    adds your name to the README.md file in the list of maintainers.
  - If the project does not have a listed maintainer, or if a current maintainer
    does not respond within 2 weeks, [create an issue in this repository](https://github.com/backdrop-ops/contrib/issues/new)
    to take over the project. Please include a link to the issue you filed for
    the abandoned project.

1. After confirming the project has been abandoned, a Backdrop Contrib
   administrator will add your name to the list of maintainers in that project's
   README.md file.

1. You may now maintain the project directly as though given permission by the
   current maintainer. Likewise, you may now grant permission for others to
   co-maintain the project as well.
