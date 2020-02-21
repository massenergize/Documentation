MassEnergize Software Dev+QA Work Flow: v0.1.0
Initial version: 2/14/20
PLUS meeting notes 2/17/2020 (Brad, Ellen, Steve, Aimee, Satra, Kaat)

This is the proposed process for software development and testing, starting from identifying bugs or feature requests, through deployment to the production site.  The main goal is to enable team members to know which issues  have been fixed and deployed, to efficiently test and avoid duplication of effort.

1. Bugs/enhancements/feature requests added, either:
	* directly by the MassE core team to the issues list on Github for the repository in question (some issues span multiple 			repositories):
		* [Community Portal](https://github.com/massenergize/frontend-portal/issues)
		* [Admin Portal](https://github.com/massenergize/frontend-admin/issues)	
		* [Back-end API](https://github.com/massenergize/api/issues)
		* [CarbonSaver](https://github.com/massenergize/frontend-carbonsaver/issues)
	* indirectly by the wider community of testers, through the issue tracking form, reviewed and transferred to the issues list by the team using the macro.

	Each issue should have a label (bug, enhancement, or other type)
 
2. Issues from the repositories are added to one of the project boards by the designated Product Owner (currently Kaat for both projects).  The project boards are how issues are tracked from start to finish.
	* [Community Portal - Version 2](https://github.com/orgs/massenergize/projects/3)
	* [Admin Portal (Version 2)](https://github.com/orgs/massenergize/projects/2)
	* [CarbonSaver (Version 1)](https://github.com/orgs/massenergize/projects/4)

	Adding to the project boards is accomplished by “Add Cards” at the far right of the project board, selecting the issue and generally moving it in the Backlog list.
 
3. After weekly discussion (or as needed), higher priority items get moved to ToDo list from Backlog by project owner. Higher priority issues are tagged as “priority #1” and can also go on top of the stack (in all columns).  At this point could assign to particular developers or let whoever has the time self-assign. At this point it should get added to a milestone. If critical add to closest milestone.
 
4. When issues are being worked on, developer should move the ticket to the In-progress list.   The developer tests locally, with a local DB before testing with hosted Dev or Prod DB. (See note 1).  If DB model changes requiring migrations are involved, testing on hosted DB should be coordinated with Sam who would do or supervise the migrations. Developers should ensure their code is consistent with current master by merging master into their branch and testing.

5. When changes are ready to merge for deployment, developer creates Pull-request (PR) to merge into master branch.  (Note 2).  PR should be reviewed by at least one other person for approval.   When approved, merge into master branch, this should automatically mark addressed issues as ‘closed’ (Note 3) and deploy to dev and to sandbox-dev. Tag the version in Github with number for deployment (Note 4).  
 
6. Use the Slack deployment workflow to list which issues were addressed. Note that anyone associated with this issue will also get a notification via Github -- this is the originator and the developer and anyone that is tagged in the issue/comment section with an @name....  This is the notification to the team that a deployment has happened so some issues ready to QA.  Then move those issues from In-Progress to QA (so lands in there in Closed state).
 
7. Once team tests the issues in QA, if they find them resolved, they move them to “Ready-to-Deploy”. If not resolved, re-open issue and  move back to “in progress” with further info added on what aspects did not work. Once you re- open an issue then the developers gets an email or pinged.
 
8. Aim to have issues “Ready-to-Deploy” to deploy to Prod on a schedule. (See note 6 for suggested Pre-deployment testing).  Tag the version on deploy to Prod, the Slack message informs team to check those issues in Prod.
 
9. If it  works in PROD, take it off the board.  See note 8 for community admin notification

Notes: for further discussion
=============================
1. Satra proposes only testing on local DB before deployment, which would be possible once we have a workable DB migration tool.
2. Satra proposes developer create a draft PR as soon as they start working on one or more issues.  Then when PR is ready remove draft status and request review ideally by at least one other person.  Brad concerned about keeping procedure appropriately lightweight
3. Satra: it would be good to have a development branch and master, so that hotfixes can be deployed without waiting for new features. (this may take a bit of time, but here is an example workflow: https://nvie.com/posts/a-successful-git-branching-model/)
4. Brad recommending Tag with version number for dev or prod deployments, Satra disagrees. 
 (This is where more work  is needed to make more efficient and resilient for other developers, e.g., automated tests.) [ this needs more clarification with Satra, Sam and Brad, Steve.]
5. To discuss: (Satra suggest we have pre-deployment prod site (STAGE?) where we test, that has same DB as prod to catch situation where it works on Dev but not on Prod: diff link (so DEV, predeploy, then PROD, esp when many towns - to discuss with Sam. Back end sync tool that can sync to two diff places - archival, predeploy)
6. To discuss: Comm admin who were put on the issue get informed? Or inform ALL Cadmins? ALSO Satra: consider a downtime for deployment for Cadmins (make it part of Cadmin training) - notification and/or banner
 
