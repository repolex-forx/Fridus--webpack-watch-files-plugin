# Repolex Knowledge Graph of Fridus/webpack-watch-files-plugin

RDF knowledge graph data for [Fridus/webpack-watch-files-plugin](https://github.com/Fridus/webpack-watch-files-plugin), parsed by [repolex](https://repolex.ai).

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
lexq download Fridus/webpack-watch-files-plugin
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── c8ea2e848feba052693d62e59f938f9aed661c25
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── c8ea2e848feba052693d62e59f938f9aed661c25.nq.gz
│   └── repolex
│       └── c8ea2e848feba052693d62e59f938f9aed661c25
│           └── chunk-001.nq.gz
├── blob
│   ├── 497639e98f6fdd67d01520a523b30d6184002267.nq.gz
│   ├── 4c5ba5718a42141fabbb6f40cb96f90602143a42.nq.gz
│   ├── 5848e78f797a6b3c43dae210faab665c5644507f.nq.gz
│   ├── 5b95eab52c46b2072ecdab9be8a9ea849a9c0f60.nq.gz
│   ├── 5f331977030c46fbcb4085ed49a52e047538d532.nq.gz
│   ├── 87771c768d042a199b03431004e77fd199f97b5d.nq.gz
│   ├── 88db0ecdf19dff385b2d2a14d9be004932e94f35.nq.gz
│   ├── 8974748db28b8c0213a982a0628f54fa3ffcf043.nq.gz
│   ├── a751a66a7189223351ddd91a3c10fef5abfec925.nq.gz
│   ├── b184dcc59a8395d55ecdd30f3b8f62cddb0a035a.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── ec274b71a8c1fa85fb38c079a9c1131218a8cd99.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── c8ea2e848feba052693d62e59f938f9aed661c25.nq.gz
├── filetree
│   └── c8ea2e848feba052693d62e59f938f9aed661c25.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 22 files
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

[Fridus/webpack-watch-files-plugin](https://github.com/Fridus/webpack-watch-files-plugin)

---
*Parsed on 2026-04-19 by [repolex](https://repolex.ai)*
