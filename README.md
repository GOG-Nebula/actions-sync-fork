# action-sync-fork

Syncs galaxy integration forks with upstream

## **_Example_** Usage

```yaml
name: sync-upstream
on:
  schedule:
    - cron: '23 * * * *'
  workflow_dispatch:
jobs:
  sync:
    runs-on: ubuntu-latest
    steps:
      - uses: GOG-Nebula/actions-sync-fork@main
        with:
          upstream_owner: urwrstkn8mare
          upstream_repo: galaxy-riot-integration
          upstream_branch: test
          reviewers: urwrstkn8mare,UncleGoogle,AndrewDWhite
          token: ${{ secrets.GITHUB_TOKEN }}
```

## TODO

- [x] better logging in the action
- [x] update the readme
- [x] fix this repo's workflows (incl making them use yarn instead of npm)
- [ ] add tests (maybe not worth it)
- [x] improve code readablitiy
