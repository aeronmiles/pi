# pi

Public workspace for [Pi](https://pi.dev) coding-agent experiments, packages, and harnesses.

## Contents

| Path | Description |
|------|-------------|
| [`fusion-harness/`](./fusion-harness) | Fork of [disler/fusion-harness](https://github.com/disler/fusion-harness) — fuse architect + builder models behind `/opinion`, `/fusion`, and `/auto-validate` |

## Prerequisites

- [Pi coding agent](https://github.com/earendil-works/pi) (`npm install -g @earendil-works/pi-coding-agent`)
- [just](https://github.com/casey/just), [jq](https://jqlang.github.io/jq/), [uv](https://docs.astral.sh/uv/) (for fusion-harness)

## Clone

```bash
git clone --recurse-submodules git@github.com:aeronmiles/pi.git
cd pi
```

If you already cloned without submodules:

```bash
git submodule update --init --recursive
```

## fusion-harness

```bash
cd fusion-harness
cp .env.example .env   # if present; or export provider keys
just fh-workhorse      # cheap test pair
# just fh-sota         # frontier pair
```

See [`fusion-harness/README.md`](./fusion-harness/README.md) for commands, architecture, and flags.

## Submodules

This repo tracks external harnesses as git submodules so upstream history stays intact.

```bash
# Update fusion-harness to the latest commit on its default branch
git submodule update --remote fusion-harness
git add fusion-harness
git commit -m "Bump fusion-harness"
```

## License

Unless noted otherwise, original files in this repository are MIT.
Harness submodules retain their own licenses (fusion-harness is MIT).
