![Build](https://github.com/mongolyy/backlog-pr-link-action/workflows/Build/badge.svg)

# backlog-pr-link-action

GitHub Actions: Link PR to backlog issue.

## Usage

```yaml
# .github/workflows/backlog-pr-link.yml
name: 'Link PR to Backlog'

on:
  pull_request:
    types: [opened, edited]

jobs:
  backlog-pr-link:
    runs-on: ubuntu-latest
    steps:
      - uses: toshimaru/backlog-pr-link-action@v0.2.0
        with:
          backlog-api-key: "${{ secrets.BACKLOG_API_KEY }}"
          backlog-host: "your-org.backlog.com"
          backlog-doing-status-id: "2"
          backlog-done-status-id: "3"
```
