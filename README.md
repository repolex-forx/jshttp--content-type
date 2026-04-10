# Repolex Knowledge Graph of jshttp/content-type

RDF knowledge graph data for [jshttp/content-type](https://github.com/jshttp/content-type), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [lexq](https://github.com/repolex-ai/lexq) query tool using [uv](https://docs.astral.sh/uv/getting-started/installation/).

If you have uv installed, just copy/paste this into your terminal:

```bash
uv tool install git+https://github.com/repolex-ai/lexq
```

This installs lexq onto your system, in your user context. Verify the install:

```bash
lexq --help
```

**lexq is designed to be used primarily by LLMs in a terminal.** Start up your favorite LLM and ask it to use the lexq tool. It's that easy!

To load this repo's data:

```bash
lexq download jshttp/content-type
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 6115a4064e4dfd9845241c3f89c233ee2423deeb
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 6115a4064e4dfd9845241c3f89c233ee2423deeb.nq.gz
│   └── repolex
│       └── 6115a4064e4dfd9845241c3f89c233ee2423deeb
│           └── chunk-001.nq.gz
├── blob
│   ├── 1609417b32a883f75e16528c8713fe41e3b4974c.nq.gz
│   ├── 34b1a2de37216b60b749c23b6f894e51d701ecf0.nq.gz
│   ├── 41840e7bc3e48cda894597cd18e562a37a174f7c.nq.gz
│   ├── 458367139eb9f0af3daa5449ff0a3d9e2e189582.nq.gz
│   ├── 5c2209663baa583c5753aebd8aeff1836b8f085f.nq.gz
│   ├── 62562b74a3b5a79e82ca417b02e0f597d85f5e2f.nq.gz
│   ├── 9616619732184386339de80f415b250843dffba9.nq.gz
│   ├── 9808c3b2b6602da61eb4afcb4caf33368e3e2bd4.nq.gz
│   ├── 9db19f63fb96592d8d3bced654a72d47c12cef97.nq.gz
│   ├── c1a922a9afba84293f449dc4b661124fbac2fd5d.nq.gz
│   ├── c58268ad26e98c128bf936c8fd32c63453d23f82.nq.gz
│   ├── c6a7986ce8fe668508ecdfc7540228efbc9cffd4.nq.gz
│   └── f15b98e249d653f23d7e121037bde0eae1817582.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 6115a4064e4dfd9845241c3f89c233ee2423deeb.nq.gz
├── filetree
│   └── 6115a4064e4dfd9845241c3f89c233ee2423deeb.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 23 files
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

## Source repository

[jshttp/content-type](https://github.com/jshttp/content-type)

---
*Parsed on 2026-04-10 by [repolex](https://repolex.ai)*
