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
- [ ] Determine where the database come from.
- [ ] Confirm `robots.txt` is configured to block traffic to the QA site.
- [ ] Setup database backups.
- [ ] Setup HTTPS and determine who will provide the SSL cert.
- [ ] Determine who manages DNS
- [ ] Configure Google Analytics or your analytics tool of choice
- [ ] Determine the caching strategy
- [ ] Configure Google Tag Manager
- [ ] Disable Apache http-auth
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
- [ ] Are errors configured to be suppressed?
- [ ] Check logs for recurring PHP notices/warnings/errors
- [ ] Security
- [ ] Verify that development related accounts/passwords have been reset or removed.
- [ ] settings / services.yml file permissions (read only)
- [ ] Verify that PHP error messages are suppressed
- [ ] Verify that Drupal's `settings.php` and `services.yml` files have the correct read-only permissions

## Performance
- [ ] Enable Drupal Page caching
- [ ] Verify that custom render array cache metadata is set and tested.
- [ ] Determine if CSS/JavaScript aggregation should be enabled.
- [ ] Verify that development related services are disabled (e.g. `development.services.yml`)
- [ ] Configured and test the CDN
- [ ] Verify that cron runs from pages requests are disabled.
- [ ] Configure external cron trigger (Jenkins/Crontab/etc)
- [ ] Verify Redis connectivity
- [ ] Verify the CDN is serving HIT's
- [ ] Verif Varnish is serving HIT's?
- [ ] Configure and test the load balancer

## Development
- [ ] Jenkins jobs for QA (and check that PROD jenkins jobs all running)
- [ ] Development related modules disabled on PROD (`kint`, `devel_generate`, `devel`, etc)
- [ ] Stage File Proxy disabled on PROD
- [ ] Stage File Proxy enabled for non-PROD environments
- [ ] Site mapping in `sites.php` for production domain
- [ ] Clean configuration export/import process.
- [ ] Config splits are enabled/disabled appropriately.
- [ ] Disable database logging
- [ ] Enable syslog
- [ ] Confirm syslog visibility and connectivity with external tools
- [ ] Verify that `robots.txt` is configured to allow traffic to the production
      site (i.e. did you remove any changes that were made for development)?

## Launch Day
- [ ] Create ordered checklist and timeline

## Additional Context
<!-- Add any other context or screenshots about the feature request here. -->
