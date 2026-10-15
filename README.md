# Repolex Knowledge Graph of sphinx-contrib/video

RDF knowledge graph data for [sphinx-contrib/video](https://github.com/sphinx-contrib/video), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [rlex](https://github.com/repolex-ai/rlex) query tool:

```bash
cargo install --git https://github.com/repolex-ai/rlex
```

Verify the install:

```bash
rlex --help
```

**rlex is designed to be used primarily by LLMs in a terminal.** Start up your favorite AI assistant and ask it to use rlex. It handles the SPARQL — you just ask questions in plain English.

To load this repo's data:

```bash
rlex download sphinx-contrib/video
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 4d04cefddc5da8aa621a19e6c49b52eca22cbf74
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 4d04cefddc5da8aa621a19e6c49b52eca22cbf74
│           └── chunk-001.nq.gz
├── blob
│   ├── 01f1c1083a53185ab08eb06ebb98c92bc4ea8b02.nq.gz
│   ├── 028460f7ea1388e852b0f79c802f9817412a6d0a.nq.gz
│   ├── 05f04eff25af67dcadd85abda8c0a5a0bceeb6ff.nq.gz
│   ├── 15e501c29c6480ea40792068443a511dec0e8416.nq.gz
│   ├── 1715fc0f5c84ea1b140aef9df49bae4784bb52f3.nq.gz
│   ├── 1dc64f142972cd73fba4f2d1cd72576a079bf4e7.nq.gz
│   ├── 246eccb44efb471e37b508f35fa09e0da94c76a0.nq.gz
│   ├── 356cff6f30023e56a8aed49897d5cfbbc1267139.nq.gz
│   ├── 366f5d81087854de411cbff3d57d84aeeb5395dd.nq.gz
│   ├── 3ceb0f8a80b060a5c7895f8b4a01702da631b1c5.nq.gz
│   ├── 3db9355101624b5a4792e1f67155955a45789c8c.nq.gz
│   ├── 4238d5b8857132d2040e4c8555eedc3836ae13fe.nq.gz
│   ├── 43bf3f3c0f91a4d53cd0c926b2596427b19d670d.nq.gz
│   ├── 444c246df12760cca46e4ab11afc57244a0bed23.nq.gz
│   ├── 6777a31eda80cb845a7bff383c4050fe535d68ff.nq.gz
│   ├── 69b366bf958918fca0c15493e8d383b43ba53f45.nq.gz
│   ├── 80665382b2296fe743feba82e1dc1aa5f19f79f6.nq.gz
│   ├── 89fdb54deb4f0cbd54f2b848b669a1990833368b.nq.gz
│   ├── 926a27924d105fd80a952115f0e7ec9f254f3b8b.nq.gz
│   ├── 93805e9e3dacb67e6594ef481a2445d2e879c3bf.nq.gz
│   ├── 96876f35e84eab125c20921867088f093c4a1c75.nq.gz
│   ├── a88ee3b503a30bcca56500a90d9e0c4e65f5439e.nq.gz
│   ├── b30df93f06cbf60734707ec5cb3741c6537d5678.nq.gz
│   ├── b3c671a4c39756726468cded0fcf1098f82ba894.nq.gz
│   ├── b5fa6c5a0e5018636b93ceab9a55dd8d55f385b3.nq.gz
│   ├── b66cbeefb57eb8236a989cf2b0f26d7ceb2990c0.nq.gz
│   ├── b7eb83d795942e6028a9a7a81a314005bfad723c.nq.gz
│   ├── b908cbe55cb344569d32de1dfc10ca7323828dc5.nq.gz
│   ├── badea3754130dfc67343207e58a48ff36fc5d45b.nq.gz
│   ├── c55a22f6a41bbb3995f04bacf7975a7955328f04.nq.gz
│   ├── c66a7472192e0a4134c574ba6e2e067fc129e6f7.nq.gz
│   ├── cfd8a7cffec0e75956ba7a1c36010a9a944318a5.nq.gz
│   ├── d116d5945fc7d9bc83f493a94305db88a5933c34.nq.gz
│   ├── d761b69ec83570344c8a22b732c647e66be57f58.nq.gz
│   ├── d989bb9c7e53d84df27c7a9b6eab5aafb019c72f.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── ebea718a7edca92ccb7844a2d83bebf2035bac18.nq.gz
│   ├── f5184e9e8fc2e7d3886ea2ca49e0c25c16cea0c6.nq.gz
│   ├── f8938f9b33d5244ab9827b0d84f0030691e812d0.nq.gz
│   └── fbb4604cc031af7af21af76183f199053abba5c6.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 4d04cefddc5da8aa621a19e6c49b52eca22cbf74.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 48 files
```

| Directory | What it contains |
|-----------|-----------------|
| `blob/` | Per-file AST graphs, content-addressed by git blob SHA. Each file in the source repo gets its own graph. |
| `aggregate/ast/` | Combined AST graph per parsed commit. Merges all blob graphs for a snapshot of the entire codebase at that point. |
| `aggregate/lsp/` | Language Server Protocol enrichment: resolved symbols, definitions, references, and type information. |
| `aggregate/dataflow/` | Interprocedural data flow edges between functions and modules. |
| `aggregate/repolex/` | Combined graph (AST + LSP + dataflow) per commit. |
| `commit/` | Git commit metadata (author, date, message, parent links). |
| `branch/` | Branch metadata. |
| `tag/` | Tag metadata. |
| `filetree/` | File tree snapshots per commit (which files existed and their blob SHAs). |
| `audit/` | Code architecture and graph audit reports per commit. |

## Source repository

[sphinx-contrib/video](https://github.com/sphinx-contrib/video)

---
*Parsed on 2026-10-15 by [repolex](https://repolex.ai)*
