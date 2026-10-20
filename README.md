# Repolex Knowledge Graph of lepture/otpauth

RDF knowledge graph data for [lepture/otpauth](https://github.com/lepture/otpauth), parsed by [repolex](https://repolex.ai).

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
rlex download lepture/otpauth
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 72374ac8157ce3f5cf89e90c359fa92652984d4c
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 72374ac8157ce3f5cf89e90c359fa92652984d4c
│           └── chunk-001.nq.gz
├── blob
│   ├── 2113b338737396f4e80ec1fa0b589acf0d22707c.nq.gz
│   ├── 221dfeb38cf8bffd5ed8d39e55673ea4747f89be.nq.gz
│   ├── 294c9b2565bb6f79d31189bd0e6473a2553acdf2.nq.gz
│   ├── 2ad8fcce56dd46400e26bbb03f87d3971e571eb6.nq.gz
│   ├── 2bd4965ea07812def8935aa75920937e2d2fcfd2.nq.gz
│   ├── 4a3b68cec29f5d6dc5ef9828b70b7afca02d4d23.nq.gz
│   ├── 62834fbd2b471c3b60f6ffde5632c11452ce61cb.nq.gz
│   ├── 640b69f6de9ab197d8b63c55be7c1de471e3591b.nq.gz
│   ├── 664a2cc3caab85f675da41d16028e85918367c6f.nq.gz
│   ├── 6afe53ae5f5e1268eeae1b1863e8753439ac8231.nq.gz
│   ├── 7225e232bf031f71d92fe58ae521939c06e98ed0.nq.gz
│   ├── 7cc5acda57edc3e36440f47930037e2a3a9dd0ac.nq.gz
│   ├── 81ba25f48907f69d7b6603d2f6200c6be8d0c319.nq.gz
│   ├── 837a1211d558d311bab7be2ee8360d8bc252aab4.nq.gz
│   ├── 8e7e649da973bff62abf483958b03ae6c4921bc8.nq.gz
│   ├── 9273f91ed69724daacde9eb4c010d720c401ae74.nq.gz
│   ├── 974ed8fa90806f2e91811ee550772aecb3a2b2c1.nq.gz
│   ├── 9e4e44d15f941e8032817ab5f12b34adcd537118.nq.gz
│   ├── a0e574f232c2b5d1b3ad61c7664535bf00e8c27d.nq.gz
│   ├── a86764b4397701062f9be9cde1af6c4333524a25.nq.gz
│   ├── a86b679e3b2c6f4f928c839158630b87184427f9.nq.gz
│   ├── aa079ec57f87bbc3cbcfd564af912ef69547bda5.nq.gz
│   ├── afb9f2e16b8a43f1c047c38e32219879516a5612.nq.gz
│   ├── b74d89d9866fdda7bf50613ffd05e9206bdc6d1b.nq.gz
│   ├── c8b6ee384dbf1f56d4d0a911d446a4f45ad0c49b.nq.gz
│   ├── ccc821e9346de22c755ff48aa65943f80d72f83e.nq.gz
│   ├── db639a750358c8140b7efb680a1af57b408ee22d.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── f3aad3d35357d072203c4bbe331f999a88e48439.nq.gz
│   ├── fb83d4ed420c2da3de0431b953d18cc7b83dcb18.nq.gz
│   ├── fbc88f939c241013e2bed36e604cb490727eb22a.nq.gz
│   ├── fc0b58cbeaed6fe4438a95c8eb4b6b4baab5ea69.nq.gz
│   └── fe0f3a2d610a9214f4d9d9857d9822d6b45bc3e2.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 72374ac8157ce3f5cf89e90c359fa92652984d4c.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 41 files
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

[lepture/otpauth](https://github.com/lepture/otpauth)

---
*Parsed on 2026-10-20 by [repolex](https://repolex.ai)*
