# Repolex Knowledge Graph of UKPLab/qnlpai2025-ham-classifier

RDF knowledge graph data for [UKPLab/qnlpai2025-ham-classifier](https://github.com/UKPLab/qnlpai2025-ham-classifier), parsed by [repolex](https://repolex.ai).

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
rlex download UKPLab/qnlpai2025-ham-classifier
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 40720adc5bfbc6c90f17007fffd904fec4916828
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 40720adc5bfbc6c90f17007fffd904fec4916828
│           └── chunk-001.nq.gz
├── blob
│   ├── 0d9360dc35d158ea1ccd025d9520994762579eec.nq.gz
│   ├── 120c6893b8af8f69dddc51b2734ed561b78c6091.nq.gz
│   ├── 1cf9b0c4970091c41f41355509d0ea25d0e08a2b.nq.gz
│   ├── 21e213fd8a9fe1a137d2fadd91c218542c3d5000.nq.gz
│   ├── 227528751dd28f9cd376b6618de4bafaf4bc60bd.nq.gz
│   ├── 261eeb9e9f8b2b4b0d119366dda99c6fd7d35c64.nq.gz
│   ├── 39ea55709b0ea6524ed4de5db3f1e20e84177e20.nq.gz
│   ├── 475c9c742d74bdefdc2d72b0a8c7cebd5cbb55b3.nq.gz
│   ├── 4cef27e61ea9ac6f982e68a89dcb12432298bb71.nq.gz
│   ├── 50eb19af9038f80d1879aebc4acb1e46667a801c.nq.gz
│   ├── 54c5b2a60ca9d24e3a0e294fe79c2c75337c912e.nq.gz
│   ├── 54fec73e88072e901d5b50f4efe223d5be608231.nq.gz
│   ├── 55221b187e3e43f445b9296e10a579a71da87423.nq.gz
│   ├── 6a25ab0345a84460b5d57549a540d8de1ba8708a.nq.gz
│   ├── 6e43ba06a9c80eb47ffc312e0958945544d65be9.nq.gz
│   ├── 78f0eea4a3d8da1f208812a92bde83b76ffc849a.nq.gz
│   ├── 7c72d260bac91d6af0a3ad52f03636c07aa68c3d.nq.gz
│   ├── 7ca76639c713a5e2877f445c1de3fe332ae707ee.nq.gz
│   ├── 829cafe545fbc5b6a622128620b975639019a6ef.nq.gz
│   ├── 8a32ee34b1603953ed79a91dec01453f67fb93c4.nq.gz
│   ├── 94a0ec8b1b1e4226fa0f4bd9e853902fff7f6769.nq.gz
│   ├── 986d121c5bf0ffdff69f0cda4b89245a77e09cd3.nq.gz
│   ├── 9ccc7363dcc9155dec920e64a9820737d3fff0e3.nq.gz
│   ├── a031e24284546f828de5a41555c4867666031127.nq.gz
│   ├── a8a745888435a1faecc66e4c8814a2ab1493002c.nq.gz
│   ├── ac696ef7fbb5f43f0e298c728acc9b7c758ec17e.nq.gz
│   ├── afc655aa85a23c0856ac1e46752602526ba52825.nq.gz
│   ├── b6d441f1fe18f4b4a8bb2fb3d29b0c7add6c83ef.nq.gz
│   ├── cc98b6933cd0df2705fd39225f24282258cd3685.nq.gz
│   ├── ce789246c514e8aa184449bb493518c30e0ecd05.nq.gz
│   ├── d6b7ef32c8478a48c3994dcadc86837f4371184d.nq.gz
│   ├── ed76eb6fafbc72271cd955160de5321e2f1a9207.nq.gz
│   └── f4a0d46cf4fdc1e17039b4af6c3e9b645f44f410.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 40720adc5bfbc6c90f17007fffd904fec4916828.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 40 files
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

[UKPLab/qnlpai2025-ham-classifier](https://github.com/UKPLab/qnlpai2025-ham-classifier)

---
*Parsed on 2026-11-08 by [repolex](https://repolex.ai)*
