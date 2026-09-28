# Repolex Knowledge Graph of asimov-modules/asimov-http-module

RDF knowledge graph data for [asimov-modules/asimov-http-module](https://github.com/asimov-modules/asimov-http-module), parsed by [repolex](https://repolex.ai).

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
rlex download asimov-modules/asimov-http-module
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 1f78f07407852e1a4262561f019f257e2e091b07
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 1f78f07407852e1a4262561f019f257e2e091b07.nq.gz
│   └── repolex
│       └── 1f78f07407852e1a4262561f019f257e2e091b07
│           └── chunk-001.nq.gz
├── blob
│   ├── 10b359dd05935c73efb064470f9ecda90f6d28aa.nq.gz
│   ├── 17e51c385ea382d4f2ef124b7032c1604845622d.nq.gz
│   ├── 6b23d61018f43b840f8d2ff3b45a1c02d76df38d.nq.gz
│   ├── 75e3b65f99b29f48ab230e3eab3de8d0b7a9229f.nq.gz
│   ├── 8bcfa2698147dd6f559522cae1f1d044e690fda7.nq.gz
│   ├── 9fe50de16e59d550235aa6d7d15ee12ddf054414.nq.gz
│   ├── a36fedab8db68b26a76fbbf1de1f549e4a12261b.nq.gz
│   ├── a9b485a9d1ad59e2f3d1b95a741a90438d97769e.nq.gz
│   ├── aaea248dbcd4f715f33922d8099878f043feeb76.nq.gz
│   ├── af9908b08f4b33c32a0080af73f53bc0fa0cdce4.nq.gz
│   ├── b327239d8733bc42af6f1d40cc8e7f12de8e14d4.nq.gz
│   ├── b37f738a0130903c236c149deeb67702e1bd16dd.nq.gz
│   ├── b4720fb6865a3037067b82f2cb7690c99fa6821a.nq.gz
│   ├── cf42f6893594e2f8be2b722de51123d65e4d61c4.nq.gz
│   ├── e3e57a8ce4ccbf74759a6df8fa4a3980ff1c9209.nq.gz
│   ├── ee4d9362508d63f9e156fe9ee1b11ebc1a3e86d6.nq.gz
│   ├── efb98088164f5786b17e83ed384971fc3c74f93c.nq.gz
│   └── f5ba4a491bcab30fbd43d5444fd47561484ed09c.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 1f78f07407852e1a4262561f019f257e2e091b07.nq.gz
├── filetree
│   └── 1f78f07407852e1a4262561f019f257e2e091b07.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

14 directories, 27 files
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

[asimov-modules/asimov-http-module](https://github.com/asimov-modules/asimov-http-module)

---
*Parsed on 2026-09-28 by [repolex](https://repolex.ai)*
