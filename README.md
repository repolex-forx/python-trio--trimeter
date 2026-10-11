# Repolex Knowledge Graph of python-trio/trimeter

RDF knowledge graph data for [python-trio/trimeter](https://github.com/python-trio/trimeter), parsed by [repolex](https://repolex.ai).

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
rlex download python-trio/trimeter
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 85d50671c3c754d149c6211fa32fe81d5b07b79d
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 85d50671c3c754d149c6211fa32fe81d5b07b79d
│           └── chunk-001.nq.gz
├── blob
│   ├── 07b11e33ee3dbf7cea86ac36f0d6c7c34cbbdc42.nq.gz
│   ├── 0d0fb77cfb9712d5eb9784f839fe74e1ff50c778.nq.gz
│   ├── 104c402ebf17ef55f9cdca2114f0a4449f6dd039.nq.gz
│   ├── 217f71916a70051bc69a85206acb159e374d22b9.nq.gz
│   ├── 291bfeaa3b207e4173c50080f22cfb473363ee5a.nq.gz
│   ├── 2afa25f3ef54ed1d6714048e702b01628593e02c.nq.gz
│   ├── 2c71c9d662a8386fb39cb4c7d1bd35c67ea1275e.nq.gz
│   ├── 31c3c9c64f1aae3314c1d3266f259da6ec444ed7.nq.gz
│   ├── 47ad4b1d6f68df976d9c63307c411ebab7daa205.nq.gz
│   ├── 480f6caa2b6a86d3ff22923c1f63ef0bc8eb4261.nq.gz
│   ├── 490c03a02a385026c9d8b1f6856cd3845e7d99e2.nq.gz
│   ├── 4edd4b18b3f9a2893c3d0a37e5e747a5f09cebe7.nq.gz
│   ├── 51f3442917839f8e0f0cccb52b3c10968ad0779e.nq.gz
│   ├── 58be8ddbaf4335bf8d90d4c3f0ebe9bfcb335d5b.nq.gz
│   ├── 5f4a13a225db317dbb3f4cb3ca1e5dc5b10eec2a.nq.gz
│   ├── 67898ba6f5cffa770a3110d8c996c8203cbbdc26.nq.gz
│   ├── 768f7dc828751a61dad364c62f24b7545cf781b1.nq.gz
│   ├── 7882d18b55efc9cbd0b86e5dcd7b6f3f13864dbc.nq.gz
│   ├── 7b49407e521b7160ba69deee70cfdf793e98a79d.nq.gz
│   ├── 7fd470cc4a53edc88602df3b0be7f9f3c30f23ab.nq.gz
│   ├── 80082270a9c0e60ee201a527972014174b99e068.nq.gz
│   ├── 875b9400fc07395740255d5f67e6b4e8e1b77b90.nq.gz
│   ├── 88be15576ce8a3fc965d9be216a0b6c65cce505d.nq.gz
│   ├── 9ba33cd8765c7703beb81ae804f783a296ec3b43.nq.gz
│   ├── adc002d6b33ea9862d20e9568a0b2f963966d642.nq.gz
│   ├── b8bb97185926d7daed314609753173945ed4ff1a.nq.gz
│   ├── bbc779137b57cdb41aef79306c96b5b9be08bf7a.nq.gz
│   ├── d645695673349e3947e8e5ae42332d0ac3164cd7.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── f38c5167733eb2fd1cb677450f876788a4aa603e.nq.gz
│   ├── fb0a3fd052a2ec4cfd5ecaae43ffbce18cd434a8.nq.gz
│   └── ffceb54742e3b96bfa792c048ed28a9e30509793.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 85d50671c3c754d149c6211fa32fe81d5b07b79d.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 40 files
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

[python-trio/trimeter](https://github.com/python-trio/trimeter)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
