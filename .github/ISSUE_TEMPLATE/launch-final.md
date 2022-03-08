---
name: Launch - Final
about: Final checklist of tasks to complete before a site launch.
title: ''
labels: ''
assignees: ''

---

Please check off line-items as they are completed and leave notes if necessary.
If an item is not relevant to this project, [strike it out](https://docs.github.com/en/github/writing-on-github/basic-writing-and-formatting-syntax#styling-text)
(e.g. `~~Not relevant item~~`) or remove it. If child tickets are created for
any line-item, please update this description to include references to them.

## Migration
- [ ] Confirm that the content migration is complete.

## Account Management
- [ ] Set expectations for post-launch support
- [ ] Determine what our next engagement will look like.
- [ ] How long will the team continue working under the current engagement after launch?
- [ ] What bugs will we fix after launch without incurring cost?
- [ ] What PTO or resourcing shifts does the client need to be aware of?

## General
- [ ] Validate that initial QA is complete.
- [ ] Validate that all content has been entered/updated.
- [ ] Set expectations with the client about what will happen on launch day.
- [ ] Determine if the launch date is still feasible given the results of QA.

## Project Management
- [ ] Validate that all development work is complete and notify the client.
- [ ] Determine and communicate the expectations we have of the client prior to launch.
- [ ] Validate that all parties are clear on what will and will not be going live at launch.
- [ ] Plan project close actions.
- [ ] Document process for denoting launch blocker bugs.

## Launch Prep
- [ ] Create a roll-back plan.
- [ ] Notify the devops team and confirm they understand what needs to occur.
- [ ] Create an ordered checklist and timeline.
- [ ] Determine who will make the go/no-go call for launch.
- [ ] Determine who will decide if a roll-back is needed.
- [ ] Determine who manages DNS and confirm they will be available to update the entries for launch.
- [ ] Lower DNS TTL to ensure quick propagation on launch day.
- [ ] Verify that `robots.txt` is configured to allow traffic to the production site (i.e. remove any changes that were made for development).
- [ ] Verify that users of the site are aware of the cut-over time/plan.
- [ ] Create a calendar invite with a video call link that can be shared with everyone who is involved with the launch.
- [ ] Verify that user accounts have been migrated or recreated, and that users have access they need.
- [ ] Validate that bug fixes are complete or will be completed on time.
- [ ] Confirm that the final QA is complete.
- [ ] Confirm that we have launch approval from the needed stakeholders.
- [ ] Implement a code freeze state and communicate this with the team.

## Launch Day
- [ ] Let the client know when the launch process begins.
- [ ] Disable HTTP Authorization if applicable.
- [ ] Update DNS entries.
- [ ] Update SSL certs as needed.
- [ ] Test the site manually for large obvious issues.
- [ ] Run through the previously created test plan.
