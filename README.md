# Repolex Knowledge Graph of asottile/setuptools-download

RDF knowledge graph data for [asottile/setuptools-download](https://github.com/asottile/setuptools-download), parsed by [repolex](https://repolex.ai).

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
rlex download asottile/setuptools-download
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 6379d3f20ee346402792914c0fafe168d7357231
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 6379d3f20ee346402792914c0fafe168d7357231
│           └── chunk-001.nq.gz
├── blob
│   ├── 3d93aefb2da505dba9c0114404cfaaeee5ad0d3f.nq.gz
│   ├── 804e9c76906dd843c433caddf64ec60b5d111d89.nq.gz
│   ├── 9482f768745d8e8abc388faa00348c049e1dbfc1.nq.gz
│   ├── 96cab5490247374ae97a457438899960951b7cf4.nq.gz
│   ├── b1447c3015af9511f2dee402ca4b5ad62adf5dce.nq.gz
│   ├── b9d2108db8e527a6e0fafe5552d6226b32b39bff.nq.gz
│   ├── ca1d90ea180858ae143c0e62d920e350d3acc62d.nq.gz
│   ├── cf4350e288bcb286188c09ebb3414224a82935fd.nq.gz
│   ├── d571cda0e9a6e8f3e65da4dbee1c104030c28305.nq.gz
│   ├── deafa40b4e5451facb45893d86045597137b3b79.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── f4f4b98c230ac21ac6b8d200f3471a976678f414.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 6379d3f20ee346402792914c0fafe168d7357231.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 20 files
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

[asottile/setuptools-download](https://github.com/asottile/setuptools-download)

---
*Parsed on 2026-10-20 by [repolex](https://repolex.ai)*
