# gaspol-one

One marketplace for the GASPOL suite: **build it** (`gaspol-dev`), **fund it** (`gaspol-pitch`), **sell it** (`gaspol-catalog`).

Each plugin lives in its own repository; this marketplace only points at them, so installing from here is identical to installing from each repo — you just add one source instead of three.

## Install

```bash
/plugin marketplace add alisadikinma/gaspol-one
/plugin install gaspol-dev@gaspol-one
/plugin install gaspol-pitch@gaspol-one
/plugin install gaspol-catalog@gaspol-one
```

To install from a local checkout instead:

```bash
/plugin marketplace add /path/to/gaspol-one
```

## Plugins

| Plugin | Version | What it does |
|---|---|---|
| [gaspol-dev](https://github.com/alisadikinma/gaspol-dev) | 1.19.0 | 21 skills + 4 agents for execution fidelity — anti-placeholder enforcement, plan verification, TDD, debugging, worktree isolation, cross-project knowledge base, auto-trigger bootstrap. |
| [gaspol-pitch](https://github.com/alisadikinma/gaspol-pitch) | 0.1.0 | 7 skills for investor/accelerator pitch decks — discovery, narrative, draft, adversarial investor review, visual, finish. Marp deck + per-slide image prompts. |
| [gaspol-catalog](https://github.com/alisadikinma/gaspol-catalog) | 0.5.0 | 7 skills for B2B sales catalogs and offer decks — a loop: reads your own knowledge base first, interviews only the gaps, and writes back what the deal taught, then storyline, master catalog once, per-prospect variants many times, render-prompt authoring, two-layer text + rendered-image gate. |

## The common thread

All three block on an adversarial review before output ships: `gaspol-dev` refuses placeholder data and unverified completion claims, `gaspol-pitch` runs a skeptic-investor linter, `gaspol-catalog` reviews both the copy and the rendered image. `gaspol-catalog` reuses `gaspol-pitch`'s review engine with a different rubric.

They are independent — install any one alone.

## Updating

Bump a plugin's `version` here whenever its own `plugin.json` version changes; the entries are duplicated by design so the marketplace can be browsed without cloning each repo.

## License

MIT — see each plugin repository for its own license file.
