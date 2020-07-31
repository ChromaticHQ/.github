---
name: Launch
about: Prepare for a site launch with a checklist of common steps.
title: ''
labels: 'devops'
assignees: ''

---

Many of the following items can simply be confirmed and checked off. Some may
warrant their own ticket that references back to a line item here.

## Preparation
- [ ] Determine production domain.
- [ ] Determine if any existing traffic needs to be proxied or redirected.
- [ ] Determine how redirects will be handled if they are needed.
- [ ] Determine where the database will come from.
- [ ] Determine who manages DNS
- [ ] Configure Google Analytics or your analytics tool of choice
- [ ] Determine the caching strategy


- [ ] Create Jenkins production cache clear job
- [ ] Run load tests to validate infrastructure
- [ ] Verify that the web server instance size large enough
- [ ] Verify automatic deployments are working
- [ ] Configue New Relic
- [ ] Configure redirects from www to the base url (or vice-versa)
- [ ] Verify that HTTP/2 is enabled.

- [ ] Is the Security Review module installed and providing a clean report?
- [ ] Are all of the checks on Drupal's status report page reporting green?
- [ ] Are all development related modules disabled?


## Security
- [ ] Security Review module (https://www.drupal.org/project/security_review)
- [ ] Verify that development related accounts/passwords have been reset or removed.
- [ ] Verify that read only permissions are set on settings files and services.yml files.
- [ ] Confirm that development modules are disabled on produciton (`kint`, `devel_generate`, `devel`, etc)
- [ ] Verify that `$settings['trusted_host_patterns']` is configured for Drupal.
- [ ] Verify that the mapping in `sites.php` supports the production domain.

## Analytics
- [ ] Configure Google Tag Manager

## QA Site
- [ ] Determine if a QA site is needed.
- [ ] Confirm that `robots.txt` is configured to block traffic to the QA site.
- [ ] Implement password protection with http-auth if required.

## Performance
- [ ] Enable Drupal Page caching.
- [ ] Enable Drupal Big Pipe caching if needed.
- [ ] Verify that custom render array cache metadata is set and tested.
- [ ] Determine if CSS/JavaScript aggregation should be enabled.
- [ ] Verify that development related services are disabled (e.g. `development.services.yml`)
- [ ] Verify Redis connectivity and Redis is used for caching.
- [ ] Verify that Redis is using the correct cache prefix if applicable.
- [ ] Configured and test the CDN if applicable.
- [ ] Verify the CDN is serving HIT's if applicable.
- [ ] Verify Varnish is serving HIT's if applicable.
- [ ] Configure and test the load balancer if applicable.
- [ ] Verify that cron runs from pages requests are disabled.
Is asset bundling configured properly?

## Hosting
- [ ] Setup HTTPS and determine who will provide the SSL cert.
Do we have https setup and SSL certificate reminders in place?

## Infrastructure
- [ ] Setup database backups.
- [ ] Verify that Drupal's `settings.php` and `services.yml` files have the correct read-only permissions.
- [ ] Confirm syslog visibility and connectivity with external tools.
- [ ] Verify that errors are configured to be suppressed.
- [ ] Setup Jenkins jobs for QA (and check that PROD jenkins jobs all running)
- [ ] Verify that Ansible playbooks follow the latest best practices.
- [ ] Verify file uploads work.
- [ ] Verify image styles work.

## Development

- [ ] Verify that PHP error messages are suppressed.
- [ ] Disable database logging.
- [ ] Enable syslog.
- [ ] Config splits are enabled/disabled appropriately.
- [ ] Check logs for recurring PHP notices/warnings/errors.
- [ ] Verify that Stage File Proxy is disabled on PROD.
- [ ] Enable Stage File Proxy for non-production environments.
- [ ] Verify that config exports and imports cleanly.
- [ ] Configure external cron trigger (Jenkins/Crontab/etc).
- [ ] Verify that the deployment process works.
- [ ] Check site error logs and fix persistent issues.

## Launch Day
- [ ] Disable http-auth if applicable.
- [ ] Notify the devops team and confirm they understands what they need to do.
- [ ] Create ordered checklist and timeline.
- [ ] Determine who manages DNS and will do the cutover.
- [ ] Verify that `robots.txt` is configured to allow traffic to the production
      site (i.e. did you remove any changes that were made for development)?

