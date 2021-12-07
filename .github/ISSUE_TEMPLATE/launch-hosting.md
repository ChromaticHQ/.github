---
name: Launch - Hosting
about: Prepare for a site launch with a checklist of common steps.
title: ''
labels: ''
assignees: ''

---

Please check off line-items as they are completed and leave notes if necessary.
If an item is not relevant to this project, [strike it out](https://docs.github.com/en/github/writing-on-github/basic-writing-and-formatting-syntax#styling-text)
(e.g. `~~Not relevant item~~`) or remove it. If child tickets are created for
any line-item, please update this ticket description to include references to

- [ ] Determine who will provide the SSL certificate.
- [ ] Setup HTTPS and test the SSL certificate.
- [ ] Setup SSL certificate reminders.
- [ ] Verify that the web server instance size is large enough.
- [ ] Verify that HTTP/2 is enabled.
- [ ] Configure redirects from www to the base URL (or vice-versa).
- [ ] Create and test redirect rules.
- [ ] Create and test reverse-proxy rules.
- [ ] Verify that asset compression is enabled.
