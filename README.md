# Repolex Knowledge Graph of hashicorp/go-retryablehttp

RDF knowledge graph data for [hashicorp/go-retryablehttp](https://github.com/hashicorp/go-retryablehttp), parsed by [repolex](https://repolex.ai).

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
rlex download hashicorp/go-retryablehttp
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── fd004584a46724fae09e2f21d7c382e15c893f42
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── fd004584a46724fae09e2f21d7c382e15c893f42
│           └── chunk-001.nq.gz
├── blob
│   ├── 07b85a1326d85ee4002e4e73d0f2fa059f835acb.nq.gz
│   ├── 0e8ca603d26cf0203e99c5d1f96fdca3cc2a5d33.nq.gz
│   ├── 135bf4c84a28c982eac1ea7dd4df9bf05cffcf80.nq.gz
│   ├── 145a62f218cbf9eae2ef0f5adf3dce424781cab7.nq.gz
│   ├── 1463bde96df064af17c9343b696fb3650e4cab09.nq.gz
│   ├── 29f802696093e1ada6770d88106b681261660529.nq.gz
│   ├── 3a22b99405e29adc793a6f461cad0bb948ce0a49.nq.gz
│   ├── 3fe4e59ada0fae6ac1e1ab3bcd1b8dcb6e3e6c5f.nq.gz
│   ├── 4af220d0dcfd715fe6895315020231b79642d48a.nq.gz
│   ├── 4e309e0b326d2ddd3dc8a449423e65aee4ea5915.nq.gz
│   ├── 515281a4f40ac719712ac00c2b563d77ce6cf96c.nq.gz
│   ├── 68a627c6d97ca702898c95158325e699671ac621.nq.gz
│   ├── 6ab87df8a4b3c40f4c8bd533cb2392e2075cd0c6.nq.gz
│   ├── 6f0751738f31da9985bf2d295bd19c4240266778.nq.gz
│   ├── 77406212d99e11be23385e307c20a58a81cfb8e6.nq.gz
│   ├── 877c03e4bad97ddb95078a714e80d4508c0175b9.nq.gz
│   ├── a1b6e17d61f62bab1ab2d2b0ca92d67a53d673b4.nq.gz
│   ├── a5da2ce821ecf5b45ea93558a9b922b8fac50ebc.nq.gz
│   ├── cf628da2370292da52510af7c0d97e2d47766e72.nq.gz
│   ├── d1e3a202581860e7cf2256aee33eb91a3e99591f.nq.gz
│   └── e6cd246866bb444449c371c7822c7cf1e13dae1d.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── fd004584a46724fae09e2f21d7c382e15c893f42.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 29 files
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

[hashicorp/go-retryablehttp](https://github.com/hashicorp/go-retryablehttp)

---
*Parsed on 2026-11-10 by [repolex](https://repolex.ai)*
