---
name: Launch
about: Prepare for a site launch with a checklist of common steps.
title: ''
labels: 'devops'
assignees: ''

---

Please check off line-items as they are completed and leave notes if necessary.
If an item is not relevant to the site launch, [strike it out](https://docs.github.com/en/github/writing-on-github/basic-writing-and-formatting-syntax#styling-text)
ex: `~~Not relevant item~~`. If child tickets are created for any line-item,
please update this ticket description to include references to those tickets.

## Preparation
- [ ] Determine production domain.
- [ ] Determine if any existing traffic needs to be proxied or redirected.
- [ ] Determine how redirects will be handled if they are needed.
- [ ] Determine where the database will come from.
- [ ] Determine who manages DNS.
- [ ] Determine the caching strategy.

## Security
- [ ] Review the [Security Review module](https://www.drupal.org/project/security_review).
- [ ] Verify that development related accounts/passwords have been reset or removed.
- [ ] Verify that proper permissions are set on settings and services.yml files.
- [ ] Confirm that development modules are disabled on produciton
      (`kint`, `devel_generate`, `devel`, etc).
- [ ] Verify that `$settings['trusted_host_patterns']` is configured.

## Analytics
- [ ] Configure Google Tag Manager if applicable.
- [ ] Configure Google Analytics or your analytics tool of choice.
- [ ] Configure New Relic if applicable.
- [ ] Verify analytics tools are only reporting from the production environment.

## QA Site
- [ ] Determine if a QA site is needed.
- [ ] Confirm that `robots.txt` or the corresponding HTTP header is configured
      to block traffic to the QA site.
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

## Hosting
- [ ] Determine who will provide the SSL certificate.
- [ ] Setup HTTPS and test the SSL certificate.
- [ ] Setup SSL certificate reminders.
- [ ] Verify that the web server instance size is large enough.
- [ ] Verify that HTTP/2 is enabled.
- [ ] Configure redirects from `www` to the base URL (or vice-versa).
- [ ] Verify that redirects are working correctly.
- [ ] Verify that asset compression is enabled.

## Infrastructure
- [ ] Setup database backups.
- [ ] Create Jenkins production cache clear job
- [ ] Verify that Drupal's `settings.php` and `services.yml` files have the
      correct read-only permissions.
- [ ] Confirm syslog visibility and connectivity with external tools.
- [ ] Verify that errors are configured to be suppressed.
- [ ] Setup Jenkins jobs for QA (and check that PROD jenkins jobs all running)
- [ ] Verify that Ansible playbooks follow the latest best practices.
- [ ] Verify file uploads work.
- [ ] Verify image styles work.
- [ ] Run load tests to validate infrastructure.

## Development
- [ ] Verify that the mapping in `sites.php` supports the production domain.
- [ ] Verify automatic deployments are working.
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
- [ ] Verify that Drupal's status report page is clear of issues.
- [ ] Verify that migrations are complete.

## Launch Prep
- [ ] Create a roll-back plan.
- [ ] Notify the devops team and confirm they understands what they need to do.
- [ ] Create ordered checklist and timeline.
- [ ] Determine who will make the go/no-go call for launch.
- [ ] Determine who will determine if a roll-back is needed.
- [ ] Determine who manages DNS and will update the entries for launch.
- [ ] Lower DNS TTL.
- [ ] Verify that `robots.txt` is configured to allow traffic to the production
      site (i.e. remove any changes that were made for development).
- [ ] Verify that users of the site are aware of the cutover time/plan.

## Site Launch
- [ ] Disable http-auth if applicable.
- [ ] Update DNS entries.
- [ ] Test the site for egregious issues.

## Post Launch
- [ ] Monitor site log for errors.
- [ ] Verify caching is working as intended.
- [ ] Verify analytics is reporting as expected.
- [ ] Run performance tests to confirm the site works as expected.
