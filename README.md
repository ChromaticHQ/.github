# Overview

This repository exists to share Github templates and configuration with other
repositories within the [`ChromaticHQ`](https://github.com/ChromaticHQ)
organization.

**This repository is public**. It needs to be public for other repositories to
be able to leverage the templates that it provides.

The approach was taken from
[this help page](https://help.github.com/en/github/building-a-strong-community/creating-a-default-community-health-file).

## Stalebot Configuration

The default [StaleBot](https://github.com/probot/stale)
[configuration](.github/stale.yml) included in this repository can be enabled
by configuring a repository's `.github/stale.yml` to contain the following:

```yaml
_extends: .github
```

## Launch Issue Templates

We previously created a collection of launch related issue templates. We found
that they were rarely/never used and just got in the way. To solve this we
moved them into a folder so they won't appear as issue templates.

They can still be accessed here:
- https://github.com/ChromaticHQ/.github/tree/main/.github/ISSUE_TEMPLATE/launch
