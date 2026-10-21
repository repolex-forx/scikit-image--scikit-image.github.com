# Repolex Knowledge Graph of scikit-image/scikit-image.github.com

RDF knowledge graph data for [scikit-image/scikit-image.github.com](https://github.com/scikit-image/scikit-image.github.com), parsed by [repolex](https://repolex.ai).

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
rlex download scikit-image/scikit-image.github.com
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── cb9a4ad05633e9fb5910ebd0bc079cde29a42a5d
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── cb9a4ad05633e9fb5910ebd0bc079cde29a42a5d
│           └── chunk-001.nq.gz
├── blob
│   ├── 056760ee8aa51c108ce204a42929f9fa06f8bd22.nq.gz
│   ├── 13c26c91ea6d8c129df54b5969db0953469cbac6.nq.gz
│   ├── 176ab33e44dbb8e017679d9db2a739fdbd6cd4dc.nq.gz
│   ├── 1a1e3a75c77283c36e002b18319d5bb9005658e8.nq.gz
│   ├── 37a97895651e01ec97968a4d143596b4ae3c2459.nq.gz
│   ├── 3bf6484a29d8da269f9bc874b25493a45fae3bae.nq.gz
│   ├── 43e2fb978f9dc259473f761b7e727e0d8c2f5e94.nq.gz
│   ├── 4615d4dee9f199da685c7741a783280b1cdb6969.nq.gz
│   ├── 4738b2edc4c51ab1f431777853d38ca2e06ce7d5.nq.gz
│   ├── 51bc56e9f2b611f73176f2bbe2806dca00f518b6.nq.gz
│   ├── 532caa617753fb4d0791fc99cdfcb63784233ee9.nq.gz
│   ├── 57767864227c56d2a5903a4a731e0817ef09d335.nq.gz
│   ├── 5f2b0a250ae3c6dbd5982c3c7ef66b05a8e919ee.nq.gz
│   ├── 645a2be37d4f6c870af94ca5e99b69d17da98f81.nq.gz
│   ├── 6f72eb809c491d7bfb62867dd55a3ac1094c13ba.nq.gz
│   ├── 7107cec93a979b9a5f64843235a16651d563ce2d.nq.gz
│   ├── 7a26ae4771627162d228f6ef7625ed64aa7c75e6.nq.gz
│   ├── 7d17b3bdc64ce398bc3d2369c8d8685f44405071.nq.gz
│   ├── 7e0ed7bd96bdd75e2bf364882db861e2b6981474.nq.gz
│   ├── 7e4c114f212585b10b77123e4cb1b1cc703a2d35.nq.gz
│   ├── 807cdb176c003a8a1c747195e96bf1f76e638294.nq.gz
│   ├── 978324ef05185ee4f40512d1c3d711a8c132213a.nq.gz
│   ├── a74e103a8311f978c415a35cd852a7f4b9b7f770.nq.gz
│   ├── a858a410e4faa62ce324d814e4b816fff83a6fb3.nq.gz
│   ├── a9969993201f9cee63cf9f49217646347297b643.nq.gz
│   ├── b8e4b4a319a44776baaacccf4dc77db47f1b0faf.nq.gz
│   ├── bffc39ef19b57ccb8360dd3c95264bab8de6cb03.nq.gz
│   ├── d93e2ed0e5752e27c96c455005c7e67bfbbc1d6d.nq.gz
│   ├── d96755fdaf8bb2214971e0db9c1fd3077d7c419d.nq.gz
│   ├── e29b1c754bae03bf3b1fb8e796ff91c90f3f0adc.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e6fa0c492606870865463b0045343b2f10a1c26c.nq.gz
│   ├── efc123f9ed2098970c04b6cca0c00e143e6a5444.nq.gz
│   ├── f186a08bac739180989cea5cbd6dc25503e70dc4.nq.gz
│   ├── f7a5a9bf84acfc1eada1ea6cb9eb2efeba1a855c.nq.gz
│   ├── fbb264a34300c5904088919084561d11b63daa76.nq.gz
│   └── fc87ecd4fd046aa1c2919964a3442b404a982694.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── cb9a4ad05633e9fb5910ebd0bc079cde29a42a5d.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 45 files
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

[scikit-image/scikit-image.github.com](https://github.com/scikit-image/scikit-image.github.com)

---
*Parsed on 2026-10-21 by [repolex](https://repolex.ai)*
