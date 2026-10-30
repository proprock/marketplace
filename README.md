# proprock marketplace

Catalog of Claude Code plugins. Each plugin lives in its own repository; this repository only lists where to fetch it.

```text
claude plugin marketplace add https://github.com/proprock/marketplace.git
claude plugin install kaboost@proprock
```

Update and removal:

```text
claude plugin marketplace update proprock
claude plugin update kaboost@proprock
claude plugin uninstall kaboost@proprock
claude plugin marketplace remove proprock
```

## Plugins

| Plugin | Source repository | Plugin path |
| :- | :- | :- |
| `kaboost` | [proprock/kaBoost](https://github.com/proprock/kaBoost) | `plugins/kaboost`, pinned to `v0.1.0-rc.2` (release candidate) |

## Adding a plugin

Add an entry to `plugins` in `.claude-plugin/marketplace.json` with a `git-subdir` or `github` source, then run `claude plugin validate --strict .`. Pin `ref` or `sha` for releases.
