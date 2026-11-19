# The MPL-2.0 histories, kept

Loom and Zengine were relicensed to AGPL-3.0-only on 2026-11-01, their histories rewritten for
the new public repositories. What they were before is kept here and on GitHub, private:

| file | what it is |
|---|---|
| `Loom-history.bundle` | every ref of `Krealsion/Loom-history` (the old `Krealsion/Loom`): 2 branches, 60 pull-request heads, its whole history, old `main` `174a186` |
| `Zengine-history.bundle` | every ref of `Krealsion/Zengine-history` (the old `Krealsion/Zengine`): 24 branches, 362 pull-request heads, 8 tags, old `main` `be62ea4d` |
| `Loom-map.txt`, `Zengine-map.txt` | one line a commit of the old `main`: the old hash, then its counterpart in the rewritten history |
| `private-map.txt` | one line a commit of this repository before 2026-11-18: the old hash, then its rewrite without the bundles |

A bundle is a repository in one file: `git clone Loom-history.bundle loom-mpl` gives it back, and
`git bundle list-heads` names its refs. On this machine these bundles are the old histories' only
copies: no clone, checkout or store holds them. The rewrite, its proof and its tools are
`Zen/reportbacks/relicense-agpl-history-RB.md` and `Zen/pass-tools/relicense-agpl/`.

Since 2026-11-18 the two bundles are outside this repository's history: they stay in this
folder on the drive, ignored (`.gitignore`), so that the plan could go to its private remote,
`Krealsion/Zen-Private`, with no MPL-era history in it. Every commit from the one that added
them on was rewritten then, its files otherwise unchanged; `private-map.txt` gives each old
hash and its new one, so an old hash in a report still finds its commit.
