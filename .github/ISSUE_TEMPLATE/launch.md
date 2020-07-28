---
name: Launch
about: Prepare for a site launch with a checklist of common steps.
title: ''
labels: 'devops'
assignees: ''

---

Many of the following items can simply be confirmed and checked off. Some may
warrant their own ticket that references back to a line item here.

## Functionality
- [ ] What is the actual site URL? benefits.sitename.com?
- [ ] SSL (Using CloudFlare or custom certificate?)
- [ ] DNS
- [ ] robots.txt
- [ ] Google Analytics
- [ ] Google Tag Manager
- [ ] Remove Apache http-auth
- [ ] Jenkins cache clear job
- [ ] Is the web server instance size large enough?
- [ ] Is Jenkins configured to automatically deploy your code, run cron, etc?
- [ ] Is New Relic configured?
- [ ] Is the VirtualHost configured to redirect from www to the base url (or vice-versa)?
- [ ] Is HTTPS enabled?
- [ ] Is Apache configured for HTTP/2?
- [ ] Is Google Analytics (or your analytics tool of choice) configured?
- [ ] Is robots.txt configured for production (ie. did you remove any changes that were made for development)?
- [ ] Is the Security Review module installed and providing a clean report?
- [ ] Are all of the checks on Drupal's status report page reporting green?
- [ ] Are all development related modules disabled?
- [ ] Are errors configured to be suppressed?
- [ ] Check logs for recurring PHP notices/warnings/errors
- [ ] Security
- [ ] check existence of straggling users/passwords from dev period (e.g. admin/admin)
- [ ] settings / services.yml file permissions (read only)
- [ ] error messages suppressed
- [ ] Do Drupal's settings.php & (if Drupal 8) services.yml files have the correct read-only permissions?

## Performance
- [ ] Page caching is enabled if appropriate.
- [ ] Render array cache metadata is set and tested.
- [ ] check settings.php and settings.local.php to turn on aggregation, turn off development.services.yml
- [ ] CDN
- [ ] Redis is enabled and connected
- [ ] CSS/JavaScript Aggregation
- [ ] Are we using New Relic?
- [ ] HTTP/2
- [ ] Cron runs from pages requests are disabled 
- [ ] External cron trigger enabled (Jenkins/Crontab/etc)
- [ ] Is Redis configured and enabled?
- [ ] Is a CDN configured?
- [ ] Is the CDN serving HIT's?
- [ ] Is Varnish serving HIT's?
- [ ] Is there a load balancer in front of your web head(s)?

## Development
- [ ] Jenkins jobs for QA (and check that PROD jenkins jobs all running)
- [ ] Dev-related modules disabled on PROD
- [ ] Stage File Proxy disabled on PROD
- [ ] Stage File Proxy enabled for non-PROD environments

## Additional Context
<!-- Add any other context or screenshots about the feature request here. -->
