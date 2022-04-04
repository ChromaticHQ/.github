---
name: Launch - Security
about: Checklist of security related tasks to complete for a site launch.
title: Launch - Security
labels: ''
assignees: ''

---

Please check off line-items as they are completed and leave notes if necessary.
If an item is not relevant to this project, [strike it out](https://docs.github.com/en/github/writing-on-github/basic-writing-and-formatting-syntax#styling-text)
(e.g. `~~Not relevant item~~`) or remove it. If child tickets are created for
any line-item, please update this description to include references to them.

- [ ] Consider installing & configuring the [SecKit module](https://www.drupal.org/project/seckit).
- [ ] Verify that development related accounts/passwords have been reset or removed.
- [ ] Verify that proper permissions are set on `settings.php` and `services.yml` files.
- [ ] Confirm that development modules are disabled on production (e.g. `kint`, `devel_generate`, `devel`, etc).
- [ ] Verify that `$settings['trusted_host_patterns']` is configured.
- [ ] Verify that database updates via the UI are disabled (`$settings['update_free_access'] = FALSE;`).
