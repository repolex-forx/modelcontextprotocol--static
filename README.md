# Repolex Knowledge Graph of modelcontextprotocol/static

RDF knowledge graph data for [modelcontextprotocol/static](https://github.com/modelcontextprotocol/static), parsed by [repolex](https://repolex.ai).

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
rlex download modelcontextprotocol/static
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── a9ba437d9fbbe92076a24b20d56449ac7c7786ac
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── a9ba437d9fbbe92076a24b20d56449ac7c7786ac
│           └── chunk-001.nq.gz
├── blob
│   ├── 563be3c1333fa26f77db75d431855973a8e638ba.nq.gz
│   ├── 59967b5a383c24a8ac4ab6726534302e09e54d30.nq.gz
│   ├── 64a431d693bc8b6d9c1684c7d9841f2786b47a9b.nq.gz
│   ├── 8022347ae2bb618c07af5801bbf2a52dc6a9af85.nq.gz
│   ├── 8766b2a49d545eb6d11b5344ded1f1008462f680.nq.gz
│   ├── 9f11b755a17d8192c60f61cb17b8902dffbd9f23.nq.gz
│   ├── 9f6469b7962e6d02844ec6f0d7aed14f27b4c19f.nq.gz
│   ├── a03c40cb2c18444b208b3696ec5778604cd37764.nq.gz
│   ├── b5031a009ced607665b1359a145d074e2c41220a.nq.gz
│   ├── bcf5ba5af6a33ac2de5344d24eb3db48860e4e73.nq.gz
│   └── e4e0a9271bdc8e72b0945bba9728fc02660b184b.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── a9ba437d9fbbe92076a24b20d56449ac7c7786ac.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 19 files
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

[modelcontextprotocol/static](https://github.com/modelcontextprotocol/static)

---
*Parsed on 2026-10-09 by [repolex](https://repolex.ai)*
