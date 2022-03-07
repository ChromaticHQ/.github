---
name: Launch - Development
about: Prepare for a site launch with a checklist of common steps.
title: ''
labels: ''
assignees: ''

---

Please check off line-items as they are completed and leave notes if necessary.
If an item is not relevant to this project, [strike it out](https://docs.github.com/en/github/writing-on-github/basic-writing-and-formatting-syntax#styling-text)
(e.g. `~~Not relevant item~~`) or remove it. If child tickets are created for
any line-item, please update this description to include references to them.

- [ ] Verify that the mapping in `sites.php` supports the production domain.
- [ ] Verify that PHP error messages are suppressed.
- [ ] Disable database logging for production.
- [ ] Enable syslog for production.
- [ ] Verify that config splits are enabled/disabled appropriately in all environments.
- [ ] Check logs for recurring PHP notices/warnings/errors.
- [ ] Fix recurring issues found in the site logs.
- [ ] Check the browser console for recurring errors.
- [ ] Fix recurring issues found in the browser console.
- [ ] Verify that Stage File Proxy is disabled on PROD.
- [ ] Enable and configure Stage File Proxy for non-production environments.
- [ ] Verify that config exports and imports cleanly.
- [ ] Determine the necessary cron frequency.
- [ ] Validate that a cron trigger is configured and the frequency is acceptable.
- [ ] Verify that the deployment process works.
- [ ] Verify that Drupal's status report page is clear of issues.
- [ ] Verify that migrations are complete.
- [ ] Configure field help/descriptive text.
- [ ] Optimize media creation/referencing experience.
- [ ] Verify that meta tags & JSON-LD are configured.
- [ ] Verify that images are being served in an efficient manner.
- [ ] Verify that no API keys or sensitive credentials are stored in code.
- [ ] Determine if "helper" node types and/or taxonomy term pages should appear and hide or block access as needed.
- [ ] Verify that alias patterns and updates/redirects are working correctly.
- [ ] Verify that $settings['hash_salt'] is set.
- [ ] Verify that $settings['update_free_access'] = FALSE; is set.
- [ ] Verify that $settings['omit_vary_cookie'] is configured correctly.
- [ ] Verify that $settings['file_public_path'] and file_private_path are configured correctly.
- [ ] Confirm that the 404 page is working and styled as expected.
- [ ] Verify that $settings['reverse_proxy_*'] configuration is set correctly if a CDN or reverse-proxy is being used.
- [ ] Run performance tests with a tool such as Calibre, Lighthouse, or PageSpeed Insights and fix the issues and/or log post launch tickets.
