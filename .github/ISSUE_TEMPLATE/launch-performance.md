---
name: Launch - Performance
about: Prepare for a site launch with a checklist of common steps.
title: ''
labels: ''
assignees: ''

---

Please check off line-items as they are completed and leave notes if necessary.
If an item is not relevant to this project, [strike it out](https://docs.github.com/en/github/writing-on-github/basic-writing-and-formatting-syntax#styling-text)
(e.g. `~~Not relevant item~~`) or remove it. If child tickets are created for
any line-item, please update this description to include references to them.

- [ ] Enable Drupal Page caching if applicable.
- [ ] Enable Drupal Big Pipe caching if needed.
- [ ] Verify that custom render array cache metadata is set and tested.
- [ ] Determine if CSS/JavaScript aggregation should be enabled.
- [ ] Verify that development related services are disabled (e.g. development.services.yml)
- [ ] Verify Redis connectivity and Redis is used for caching.
- [ ] Verify that Redis is using the correct cache prefix if applicable.
- [ ] Configure and test the CDN if applicable.
- [ ] Verify the CDN is serving HITs if applicable.
- [ ] Verify Varnish is serving HITs if applicable.
- [ ] Configure and test the load balancer if applicable.
