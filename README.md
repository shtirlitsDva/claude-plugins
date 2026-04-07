# shtirlitsDva plugins

Personal [Claude Code](https://claude.com/claude-code) plugin marketplace.

## Install

From any machine with Claude Code installed, add the marketplace and then install whichever plugins you want:

```
/plugin marketplace add shtirlitsDva/claude-plugins
/plugin install revdiff@shtirlitsDva-plugins
/plugin install revdiff-planning@shtirlitsDva-plugins
```

The three commands are idempotent and can be re-run on any new machine.

## Plugins

| Name | Source repo | Description |
|---|---|---|
| `revdiff` | [`shtirlitsDva/revdiff`](https://github.com/shtirlitsDva/revdiff) | Review diffs, files, and documents with inline annotations in a TUI overlay. |
| `revdiff-planning` | [`shtirlitsDva/revdiff`](https://github.com/shtirlitsDva/revdiff) (subdirectory `plugins/revdiff-planning`) | Automatic plan review with revdiff. |

Each plugin lives in its own upstream repository — this marketplace is a thin aggregator, so plugin updates flow naturally from the source repos without needing edits here.

## Adding a new plugin

Edit [`.claude-plugin/marketplace.json`](.claude-plugin/marketplace.json), append a new object to the `plugins` array, commit, push. That's it.

- Plugin at the root of another GitHub repo → `"source": { "source": "github", "repo": "owner/repo" }`
- Plugin in a subdirectory of another GitHub repo → `"source": { "source": "git-subdir", "url": "owner/repo", "path": "relative/path" }`
- Plugin living in this same repo → `"source": "./plugins/whatever"`
