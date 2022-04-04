---
name: Launch - Hosting
about: Checklist of hosting related tasks to complete for a site launch.
title: Launch - Hosting
labels: ''
assignees: ''

---

Please check off line-items as they are completed and leave notes if necessary.
If an item is not relevant to this project, [strike it out](https://docs.github.com/en/github/writing-on-github/basic-writing-and-formatting-syntax#styling-text)
(e.g. `~~Not relevant item~~`) or remove it. If child tickets are created for
any line-item, please update this description to include references to them.

- [ ] Determine who will provide the SSL certificate.
- [ ] Setup HTTPS and test the SSL certificate.
- [ ] Setup SSL certificate reminders.
- [ ] Verify that the web server instance size is large enough.
- [ ] Verify that HTTP/2 is enabled.
- [ ] Configure redirects from www to the base URL (or vice-versa).
- [ ] Create and test redirect rules.
- [ ] Create and test reverse-proxy rules.
- [ ] Verify that asset compression is enabled.
- [ ] Determine who is responsible for the DNS and what needs to happen and when.
- [ ] Determine who is responsible from the hosting provider. What do they need from us to deliver when and how we want them to?
- [ ] Determine who is responsible from the client’s IT team. Security team? What do they need from us to deliver when and how we want them to?
