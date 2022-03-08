---
name: Launch - Planning
about: Checklist of initial planning related tasks to complete for a site launch.
title: ''
labels: ''
assignees: ''

---

Please check off line-items as they are completed and leave notes if necessary.
If an item is not relevant to this project, [strike it out](https://docs.github.com/en/github/writing-on-github/basic-writing-and-formatting-syntax#styling-text)
(e.g. `~~Not relevant item~~`) or remove it. If child tickets are created for
any line-item, please update this description to include references to them.

- [ ] Determine when/if a content freeze should occur.
- [ ] Determine who is responsible for entering/updating content and when that will occur.
- [ ] Determine launch date and time.
- [ ] Determine production domain.
- [ ] Determine if any existing traffic needs to be proxied or redirected.
- [ ] Determine how redirects will be handled if they are needed.
- [ ] Determine where the starting database will come from.
- [ ] Determine who manages DNS.
- [ ] Determine the caching strategy.
- [ ] Take screenshots of "before" site.
- [ ] Add site to [web.archive.org](http://web.archive.org/).

## QA Process
- [ ] Determine if a QA site is needed.
- [ ] Confirm that `robots.txt` or the corresponding HTTP header is configured to block traffic to the QA site.
- [ ] Implement password protection with HTTP Authorization if required.
- [ ] Verify that proper testing API keys are configured if needed.
