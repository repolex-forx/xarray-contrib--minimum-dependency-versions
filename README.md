# Repolex Knowledge Graph of xarray-contrib/minimum-dependency-versions

RDF knowledge graph data for [xarray-contrib/minimum-dependency-versions](https://github.com/xarray-contrib/minimum-dependency-versions), parsed by [repolex](https://repolex.ai).

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
rlex download xarray-contrib/minimum-dependency-versions
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 300e3abc7e76337827a38961dbccc9ad5f41892b
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 300e3abc7e76337827a38961dbccc9ad5f41892b
│           └── chunk-001.nq.gz
├── blob
│   ├── 0375d65848b2ecdc4a2e70b9d18d2852725a683d.nq.gz
│   ├── 1068df57621695ccf0a2f9a13e26626de7e2ad03.nq.gz
│   ├── 13df3f1da7ab566a7576a927eb77a8420c3b792e.nq.gz
│   ├── 1e0decd15b1cda2704de4db9ced819ef1a739be8.nq.gz
│   ├── 2022866450d76df6cebcf7fbe6c0c4cac1d3f5c7.nq.gz
│   ├── 21cbe21419759874bdaeb02d70e20a87f3dbede9.nq.gz
│   ├── 24f7c246672c94f31abeba66f939f7b77999cb01.nq.gz
│   ├── 27dcfc0e1e1866c85e92ff48e5dbbf096412a7de.nq.gz
│   ├── 4990b75fe5037baf23a806d6c28f162938700fb4.nq.gz
│   ├── 5901b6b148579f02495ceee08111740e07206d67.nq.gz
│   ├── 59a629b59c60797dd05fe0f6102a2c4904b7510d.nq.gz
│   ├── 5bae0b5e7a4186b902e7a29b258e97a51ec9b977.nq.gz
│   ├── 5f89818f9e63c2f6829c7706c57f223cdb5bbd38.nq.gz
│   ├── 64cffeb03ccfaacfc39a4f184ade952458134036.nq.gz
│   ├── 6dd144a36facee8ff8816d40f3b00a9972cee8fd.nq.gz
│   ├── 6f97076fbef59af0c0645a28deb419d72052ec35.nq.gz
│   ├── 767cf67b7be730deecddf882d247ba653e5ec2e3.nq.gz
│   ├── 875a59e01bfa35ffe65f15777b66dd2e9f2eb26e.nq.gz
│   ├── 9469398cf5a7d4dcfa1877ed612784aa33c266cc.nq.gz
│   ├── 9ab3f67655cdc166650fe5d1b997787daaa80e87.nq.gz
│   ├── a2e88bdd9479df459156ca7f831cbf11d48d51d9.nq.gz
│   ├── a4df9d13b4db9f747ca3115f99e3f5eb2a91b49c.nq.gz
│   ├── b01e3759ed3001e40c8d67f2e20d00be406735e3.nq.gz
│   ├── b3d620f2c4b8cf1b62e4046f66f1016018bbd4cd.nq.gz
│   ├── b89a03f00a69af32e4cf915ad8d44d37fe84680f.nq.gz
│   ├── cc1334eeb659caf9bc48801988b0262cf06c1357.nq.gz
│   ├── da7bafb8b8bc935a2f5846c2dc8fae292f337591.nq.gz
│   ├── df1c64dfe4fcef6ee0b5df90950607e39a1362aa.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── e83c2afd5e70f71a3f737db6779ba240ce9153b4.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 300e3abc7e76337827a38961dbccc9ad5f41892b.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 38 files
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

[xarray-contrib/minimum-dependency-versions](https://github.com/xarray-contrib/minimum-dependency-versions)

---
*Parsed on 2026-10-28 by [repolex](https://repolex.ai)*
