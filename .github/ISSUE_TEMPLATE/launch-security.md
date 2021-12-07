---
name: Launch - Security
about: Prepare for a site launch with a checklist of common steps.
title: ''
labels: ''
assignees: ''

---

Please check off line-items as they are completed and leave notes if necessary.
If an item is not relevant to this project, [strike it out](https://docs.github.com/en/github/writing-on-github/basic-writing-and-formatting-syntax#styling-text)
(e.g. `~~Not relevant item~~`) or remove it. If child tickets are created for
any line-item, please update this ticket description to include references to

- [ ] Consider installing & configuring the SecKit module.
- [ ] Verify that development related accounts/passwords have been reset or removed.
- [ ] Verify that proper permissions are set on settings.php and services.yml files.
- [ ] Confirm that development modules are disabled on production (e.g. kint, devel_generate, devel, etc).
- [ ] Verify that `$settings['trusted_host_patterns']` is configured.
- [ ] Verify that cron runs from page requests are disabled (`$settings['update_free_access'] = FALSE;)`.