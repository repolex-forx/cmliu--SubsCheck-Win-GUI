# Repolex Knowledge Graph of cmliu/SubsCheck-Win-GUI

RDF knowledge graph data for [cmliu/SubsCheck-Win-GUI](https://github.com/cmliu/SubsCheck-Win-GUI), parsed by [repolex](https://repolex.ai).

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
rlex download cmliu/SubsCheck-Win-GUI
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 3bca96943791a1f9b79a6dde535cd79ba54fc7b9
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 3bca96943791a1f9b79a6dde535cd79ba54fc7b9
│           └── chunk-001.nq.gz
├── blob
│   ├── 017016f75e2c9a74b8dfdb5e6d8e7c3b9dd8e749.nq.gz
│   ├── 071264be7e0046983e2f8d5f8a7f5c19595d9c7d.nq.gz
│   ├── 1f666f268bc6af87ca66d64b28d790bd5214274e.nq.gz
│   ├── 1ff0c423042b46cb1d617b81efb715defbe8054d.nq.gz
│   ├── 2b72784fd3273b07e764f7b1d6c45547f381906e.nq.gz
│   ├── 324eaf572aa5a064805b1d1a879f53c4437814e0.nq.gz
│   ├── 35b03079ccd702aed35de3ae67d65000a37c0591.nq.gz
│   ├── 39645652af62950ebf3b28ec3a5400dcec30b1c4.nq.gz
│   ├── 3c950719d34f143cdb70401b0151933935639d8c.nq.gz
│   ├── 44ccdb8dc7a25f0de6ae859f81231e2709b62c8e.nq.gz
│   ├── 515365994e7a88946fb3e4a01fa91508a361ddc1.nq.gz
│   ├── 52d9dd11e90bc026556d7c641563c7147ac365ee.nq.gz
│   ├── 5eeef28dea91e4f4cd2d562642be06df57f683c2.nq.gz
│   ├── 66ef724618504e91956fdc82ac0121d551b346e0.nq.gz
│   ├── 8aa26455d23acf904be3ed9dfb3a3efe3e49245a.nq.gz
│   ├── 97dcaa1a455196b6d741e54fab8722dc58daa061.nq.gz
│   ├── a96d2cb2147683cf5d0ba1922b324f7bbdeffb09.nq.gz
│   ├── adea5b1ce34122f728c8199fec406e5e1265ecab.nq.gz
│   ├── b7ecb666be3f9da4eed3df1aabdeab3f4499e929.nq.gz
│   ├── bfbc9196cce2d6b1cb0891c2b4ff7f090151e53e.nq.gz
│   ├── c367db0a86eb6ed44fd409931f99ab31bd17f655.nq.gz
│   ├── c728cb4fb82c07069371d32e9737a69f7a4f5917.nq.gz
│   ├── cdc9f01c481d724d824a4754d51da0898cf1b18f.nq.gz
│   ├── d749cb460d29ce7d49edcb8cf50ce22c927f7ad8.nq.gz
│   ├── d7dcef7a9eeff4c9fd002b37860c8bc6551e68fc.nq.gz
│   ├── eae8cb87212ab7c67826bd03c09285b78f6b1741.nq.gz
│   ├── ecdcf8a54da312b76ada87a3054152b813ce1f9d.nq.gz
│   ├── f6989a71087f8a0a0752ab6742b82faf1970a9f0.nq.gz
│   ├── fa095ad26cfcc86a49672a3c907aa0154481a1fb.nq.gz
│   ├── fd40057b42eecf240db82d48fb6c969a531cbd66.nq.gz
│   └── ff3352c1f9e483347feee1d33209ecd44023e74a.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 3bca96943791a1f9b79a6dde535cd79ba54fc7b9.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 39 files
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

[cmliu/SubsCheck-Win-GUI](https://github.com/cmliu/SubsCheck-Win-GUI)

---
*Parsed on 2026-11-09 by [repolex](https://repolex.ai)*
