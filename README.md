# Repolex Knowledge Graph of pytest-dev/pytest-iam

RDF knowledge graph data for [pytest-dev/pytest-iam](https://github.com/pytest-dev/pytest-iam), parsed by [repolex](https://repolex.ai).

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
rlex download pytest-dev/pytest-iam
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 09b1d5cfc4dc8eb97702b1510a2b585efeb6b25b
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 09b1d5cfc4dc8eb97702b1510a2b585efeb6b25b
│           └── chunk-001.nq.gz
├── blob
│   ├── 2808575548afefd62f8550754585b4c0d8daadf0.nq.gz
│   ├── 39fbdb738c52ed7a7ba1967be790ea14ccfb350b.nq.gz
│   ├── 3b772f6f2b60b0218303c1caff08206bcc16de8d.nq.gz
│   ├── 41e67b37945bfb45329053310fac3b04cb3c9640.nq.gz
│   ├── 441b78925bdc85f7dbd6c70f63e46781005c966e.nq.gz
│   ├── 4afc7d3ff2687745d45a65b6930d5b583c448298.nq.gz
│   ├── 5c5af3e9ae4bfcf4296d7233a3d3b51356b5d0c2.nq.gz
│   ├── 6388053d045ce18b5f45f9c4f2b4b40f0fd9695b.nq.gz
│   ├── 776a323da5b144f534dc0cde567e1fb43d910eb1.nq.gz
│   ├── 844e0d42e93dc5b86af08923577623b934a10c42.nq.gz
│   ├── 9612698d7c86bef5c8e6bc990ab66017d936f0a9.nq.gz
│   ├── 9b8f7ce303a1eadc7ea00220b04733def7aa326a.nq.gz
│   ├── a55c085857c3abc05157eaba62aee1bac554d3d4.nq.gz
│   ├── a6e4c5d884dd56cb8973731f902d609cb40e47fe.nq.gz
│   ├── bba0e819fcb5a9d62877e22c045f8460901642a3.nq.gz
│   ├── c3c4ba1ebb31a662541e8e756863612b160442e2.nq.gz
│   ├── d63c122fb88659ca1ad7e65d7c497ce41a221039.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e996c97e08532b52755ded05a5948fb490d9b5c0.nq.gz
│   ├── ebd5c756ff951730c705223340c49c114bea9736.nq.gz
│   ├── f1fd78bebfff878aa31a3b6655ee696099000ba3.nq.gz
│   └── f36ace84018bc9eb22b126bf807134897b1ad7c6.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 09b1d5cfc4dc8eb97702b1510a2b585efeb6b25b.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 30 files
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

[pytest-dev/pytest-iam](https://github.com/pytest-dev/pytest-iam)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
