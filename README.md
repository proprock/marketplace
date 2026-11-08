# proprock marketplace

Catalog of Claude Code and Codex plugins. Each plugin lives in its own repository; this repository only lists where to fetch it.

## Claude Code

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

## Codex CLI

```text
codex plugin marketplace add proprock/marketplace
codex plugin add kaboost@proprock
```

Update and removal:

```text
codex plugin marketplace upgrade proprock
codex plugin add kaboost@proprock
codex plugin remove kaboost@proprock
codex plugin marketplace remove proprock
```

## Plugins

| Plugin | Source repository | Plugin path |
| :- | :- | :- |
| `kaboost` (Claude Code) | [proprock/kaBoost](https://github.com/proprock/kaBoost) | `plugins/kaboost`, pinned to `v0.2.0` (release) |
| `kaboost` (Codex) | [proprock/kaBoost](https://github.com/proprock/kaBoost) | `adapters/codex/package/kaboost`, pinned to `v0.2.0` (release) |

## Adding a plugin

Claude Code reads `.claude-plugin/marketplace.json`, Codex reads `.agents/plugins/marketplace.json` (and falls back to the Claude catalog only when its own is missing). Add an entry to `plugins` in each catalog the plugin supports, with a `git-subdir` or `github` source, then run `claude plugin validate --strict .`. Pin `ref` and `sha` for releases.
