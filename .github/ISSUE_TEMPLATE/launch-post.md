---
name: Launch - Post Launch
about: Checklist of tasks to complete after a site launch.
title: ''
labels: ''
assignees: ''

---

Please check off line-items as they are completed and leave notes if necessary.
If an item is not relevant to this project, [strike it out](https://docs.github.com/en/github/writing-on-github/basic-writing-and-formatting-syntax#styling-text)
(e.g. `~~Not relevant item~~`) or remove it. If child tickets are created for
any line-item, please update this description to include references to them.

## Development
- [ ] Monitor site log for errors.
- [ ] Verify caching is working as intended.
- [ ] Verify analytics is reporting as expected.
- [ ] Run performance tests with a tool such as Calibre, Lighthouse, or PageSpeed Insights to confirm the site performs as expected.
- [ ] Update Stage File Proxy origin URL configuration to point to the production domain (e.g. $config['stage_file_proxy.settings']['origin']).
- [ ] Confirm that third party integrations are working as expected.
- [ ] Add site to [updown.io](https://updown.io) uptime monitoring.
- [ ] Disable migration related modules and source database connectivity as applicable.
- [ ] Configure Sentry if applicable.

## Ongoing Process
- [ ] Update automated or manual tests to point to the new production domain.
- [ ] Determine if the git branching strategy, merging rules, or any development workflows should be adjusted.
- [ ] Update QA environments to pull databases from the new production site.
- [ ] Update or create database backup scripts to backup the production site.
