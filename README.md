# Repolex Knowledge Graph of executablebooks/sphinx-conditional-asset

RDF knowledge graph data for [executablebooks/sphinx-conditional-asset](https://github.com/executablebooks/sphinx-conditional-asset), parsed by [repolex](https://repolex.ai).

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
rlex download executablebooks/sphinx-conditional-asset
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 0228a75ff0f582147878960c4d660f212fc287fe
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 0228a75ff0f582147878960c4d660f212fc287fe
│           └── chunk-001.nq.gz
├── blob
│   ├── 202fe28644c671b99fa9f9c8272ed704549ef753.nq.gz
│   ├── 3f805711d418d8f6dae35755777836ca14213b91.nq.gz
│   ├── 4842c4455d9b07d1a54e11ed8e472823524bc041.nq.gz
│   ├── 54b656ad4432e7ed010b10ad0f3cd06da6c12acb.nq.gz
│   ├── 844c8c874657db72e9e69093d5eef04189568269.nq.gz
│   ├── 8a85dd86bd38373d74db9a5a9cd8a09b2401259a.nq.gz
│   ├── 955739806f8b5ff67a0298ce5d7a9e4a883e667f.nq.gz
│   ├── 970578a0eabbd358d9a6fe8b9da82daa94c43070.nq.gz
│   ├── a2d1418547ad3e63b874946e1653d59c145874b2.nq.gz
│   ├── a6abc14f697bccbaeb2f72c563bcc934ee3a8955.nq.gz
│   ├── b19a7b0294a75316e838c224f4f38c5faa707464.nq.gz
│   ├── b6e47617de110dea7ca47e087ff1347cc2646eda.nq.gz
│   ├── bcd81f7a6d11914d9173c2452869209130f1f6cc.nq.gz
│   ├── c78b43e164bed1d093590f98a9edc6e9333becb2.nq.gz
│   ├── d4bb2cbb9eddb1bb1b4f366623044af8e4830919.nq.gz
│   ├── dab6ba48f3dcb26eae65920afb84113b1ebb141f.nq.gz
│   ├── e0074aa34e987476a214065f5532b302f0613e6f.nq.gz
│   ├── e5583af64c675fba12d2442a0f403d2fefbd7aaf.nq.gz
│   ├── ebac2f76c91ef919706dcd6db2498dce211ce8f1.nq.gz
│   └── f233c62331786f6b85e55f6b84db3d6b962a5590.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 0228a75ff0f582147878960c4d660f212fc287fe.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 28 files
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

[executablebooks/sphinx-conditional-asset](https://github.com/executablebooks/sphinx-conditional-asset)

---
*Parsed on 2026-10-21 by [repolex](https://repolex.ai)*
