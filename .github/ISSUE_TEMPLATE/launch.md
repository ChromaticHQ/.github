---
name: Launch
about: Prepare for a site launch with a checklist of common steps.
title: ''
labels: ''
assignees: ''

---

Please check off line-items as they are completed and leave notes if necessary.
If an item is not relevant to this project, [strike it out](https://docs.github.com/en/github/writing-on-github/basic-writing-and-formatting-syntax#styling-text)
(e.g. `~~Not relevant item~~`) or remove it. If child tickets are created for
any line-item, please update this ticket description to include references to
those tickets.

## Preparation
- [ ] Determine production domain.
- [ ] Determine if any existing traffic needs to be proxied or redirected.
- [ ] Determine how redirects will be handled if they are needed.
- [ ] Determine where the starting database will come from.
- [ ] Determine who manages DNS.
- [ ] Determine the caching strategy.
- [ ] Take screenshots of "before" site.
- [ ] Add site to [web.archive.org](http://web.archive.org/).

## Security
- [ ] Consider installing & configuring the [SecKit module](https://www.drupal.org/project/seckit).
- [ ] Verify that development related accounts/passwords have been reset or removed.
- [ ] Verify that proper permissions are set on `settings.php` and
      `services.yml` files.
- [ ] Confirm that development modules are disabled on production
      (e.g. `kint`, `devel_generate`, `devel`, etc).
- [ ] Verify that `$settings['trusted_host_patterns']` is configured.

## Analytics
- [ ] Configure Google Tag Manager if applicable.
- [ ] Configure Google Analytics or your analytics tool of choice.
- [ ] Configure New Relic if applicable.
- [ ] Verify analytics tools are only reporting from the production environment
      or reporting separately depending on requirements.

## QA Site
- [ ] Determine if a QA site is needed.
- [ ] Confirm that `robots.txt` or the corresponding HTTP header is configured
      to block traffic to the QA site.
- [ ] Implement password protection with HTTP Authorization if required.
- [ ] Verify that proper testing API keys are configured if needed.

## Performance
- [ ] Enable Drupal Page caching.
- [ ] Enable Drupal Big Pipe caching if needed.
- [ ] Verify that custom render array cache metadata is set and tested.
- [ ] Determine if CSS/JavaScript aggregation should be enabled.
- [ ] Verify that development related services are disabled (e.g.
      `development.services.yml`)
- [ ] Verify Redis connectivity and Redis is used for caching.
- [ ] Verify that Redis is using the correct cache prefix if applicable.
- [ ] Configure and test the CDN if applicable.
- [ ] Verify the CDN is serving HITs if applicable.
- [ ] Verify Varnish is serving HITs if applicable.
- [ ] Configure and test the load balancer if applicable.
- [ ] Verify that cron runs from pages requests are disabled.

## Development
- [ ] Verify that the mapping in `sites.php` supports the production domain.
- [ ] Verify automatic deployments are working.
- [ ] Verify that PHP error messages are suppressed.
- [ ] Disable database logging.
- [ ] Enable syslog.
- [ ] Verify that config splits are enabled/disabled appropriately in all
      environments.
- [ ] Check logs for recurring PHP notices/warnings/errors.
- [ ] Fix recurring issues found in the site logs.
- [ ] Check the browser console for recurring errors.
- [ ] Fix recurring issues found in the browser console.
- [ ] Verify that Stage File Proxy is disabled on PROD.
- [ ] Enable and configure Stage File Proxy for non-production environments.
- [ ] Verify that config exports and imports cleanly.
- [ ] Determine the necessary cron frequency.
- [ ] Configure external cron trigger (Jenkins/Crontab/etc).
- [ ] Verify that the deployment process works.
- [ ] Check site error logs and fix persistent issues.
- [ ] Verify that Drupal's status report page is clear of issues.
- [ ] Verify that migrations are complete.
- [ ] Determine if git branching strategy or merge rules should be adjusted post
      launch.
- [ ] Verify that no API keys or sensitive credentials are stored in code.
- [ ] Verify if "helper" node types and/or taxonomy term pages should appear and
      hide or block access as needed.
- [ ] Verify that alias patterns and updates/redirects are working correctly.
- [ ] Verify that `$settings['hash_salt']` is set.
- [ ] Verify that `$settings['update_free_access'] = FALSE;` is set.
- [ ] Verify that `$settings['omit_vary_cookie']` is configured correctly.
- [ ] Verify that `$settings['file_public_path']` and `file_private_path` are
      configured correctly.
- [ ] Confirm that the 404 page is working and styled as expected.
- [ ] Verify that `$settings['reverse_proxy_*']` configuration is set correctly
      if a CDN or reverse-proxy is being used.
- [ ] Run performance tests with a tool such as Calibre, Lighthouse, or
      PageSpeed Insights and fix the issues and/or log post launch tickets.
- [ ] Configure field help/descriptive text.
- [ ] Optimize media creation/referencing experience.
- [ ] Verify that meta tags & JSON-LD are configured.
- [ ] Verify that images are being served in a efficient manner.

## Hosting
- [ ] Determine who will provide the SSL certificate.
- [ ] Setup HTTPS and test the SSL certificate.
- [ ] Setup SSL certificate reminders.
- [ ] Verify that the web server instance size is large enough.
- [ ] Verify that HTTP/2 is enabled.
- [ ] Configure redirects from `www` to the base URL (or vice-versa).
- [ ] Create and test redirect rules.
- [ ] Create and test reverse-proxy rules.
- [ ] Verify that asset compression is enabled.

## Infrastructure
- [ ] Setup database backups in consultation with the devops team.
- [ ] Create Jenkins production cache clear job if applicable.
- [ ] Verify that Drupal's `settings.php` and `services.yml` files have the
      correct read-only permissions.
- [ ] Confirm syslog visibility and connectivity with external tools.
- [ ] Verify that errors are configured to be suppressed.
- [ ] Setup Jenkins jobs for QA (and check that PROD jenkins jobs all running)
- [ ] Verify that Ansible playbooks follow the latest best practices.
- [ ] Verify file uploads work.
- [ ] Verify image styles work.
- [ ] Run load tests to validate infrastructure.
- [ ] Consult with the hosting provider for any platform specific launch steps
      or advice.

## Launch Prep
- [ ] Create a roll-back plan.
- [ ] Notify the devops team and confirm they understands what they need to do.
- [ ] Create ordered checklist and timeline.
- [ ] Determine who will make the go/no-go call for launch.
- [ ] Determine who will decide if a roll-back is needed.
- [ ] Determine who manages DNS and will update the entries for launch.
- [ ] Lower DNS TTL to ensure quick propagation on launch day.
- [ ] Verify that `robots.txt` is configured to allow traffic to the production
      site (i.e. remove any changes that were made for development).
- [ ] Verify that users of the site are aware of the cutover time/plan.
- [ ] Create a calendar invite with a video call link that can be shared with
      everyone who is involved with the launch.
- [ ] Verify that user accounts have been migrated or recreated, and that users
      have access they need.

## Site Launch
- [ ] Disable HTTP Authorization if applicable.
- [ ] Update DNS entries.
- [ ] Test the site manually for large obvious issues.

## Post Launch
- [ ] Monitor site log for errors.
- [ ] Verify caching is working as intended.
- [ ] Verify analytics is reporting as expected.
- [ ] Run performance tests with a tool such as Calibre, Lighthouse, or
      PageSpeed Insights to confirm the site performs as expected.
- [ ] Update QA environments to pull databases from the new production site.
- [ ] Update Stage File Proxy origin URL configuration to point to the
      production domain (e.g. `$config['stage_file_proxy.settings']['origin']`).
- [ ] Update automated or manual tests to point to the new production domain.
- [ ] Confirm that third party integrations are working as expected.
- [ ] Add site to Updown.io uptime monitoring.
- [ ] Disable migration related modules and source database connectivity as
      applicable.
