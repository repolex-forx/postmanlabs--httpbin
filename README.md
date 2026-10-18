# Repolex Knowledge Graph of postmanlabs/httpbin

RDF knowledge graph data for [postmanlabs/httpbin](https://github.com/postmanlabs/httpbin), parsed by [repolex](https://repolex.ai).

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
rlex download postmanlabs/httpbin
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── f8ec666b4d1b654e4ff6aedd356f510dcac09f83
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── f8ec666b4d1b654e4ff6aedd356f510dcac09f83
│           └── chunk-001.nq.gz
├── blob
│   ├── 048ecf1c402217d49603cc9265a534333a5a2298.nq.gz
│   ├── 2003b639c40025a4216b7b765e800b872a9052cd.nq.gz
│   ├── 265c7ab68515347755e59a2ded779353e14ecf81.nq.gz
│   ├── 26fd17fc0801972d6a89540d09be53ea3a702f27.nq.gz
│   ├── 2a9acf13daa95e85642ea255d3e3bd1ef8252804.nq.gz
│   ├── 305c988255000fb1b4c75ecf66295b954b21b5e2.nq.gz
│   ├── 37f5392d54cea2bda1c4bb97a5cd31f5ad93ad10.nq.gz
│   ├── 44da70f04a2b82ffa7471411e4315248a913d06d.nq.gz
│   ├── 4b5675da17b0d86550b7b27152ca280302bf6bfb.nq.gz
│   ├── 5ab46ac6f69cda9b3cc0d4fdc2172b206be83492.nq.gz
│   ├── 5ff09579e3842100aad840366b3a3031b05bef62.nq.gz
│   ├── 63e0d2b9567890ab9b8131407bc62eda50282fa3.nq.gz
│   ├── 6e2e0591b33b8ebdb87c7a8eabb0d50ee35ad177.nq.gz
│   ├── 726dd626b0ba6e1d947b702a91f075b0bfa52fa4.nq.gz
│   ├── 8148d6842cad88979cb90d0b462db1c33c502f21.nq.gz
│   ├── 819006bbd24e0ae789b9453b265e4184dd4d99f1.nq.gz
│   ├── 8495eb811643dd53d54ea9a31ae026cb8ed8800e.nq.gz
│   ├── 885f52d8de8220b4aa0430061054cd2230611656.nq.gz
│   ├── 894af4cc64e5551a30ce1f81290d28d9d4fbf9db.nq.gz
│   ├── 8ad29bb8a99921c695bdd8611df4fb372563174f.nq.gz
│   ├── 91f42bebda94a6f664e33af3dc4ede796428f13c.nq.gz
│   ├── 96f81bce745e779e85f578c769ff11707ba6eb0d.nq.gz
│   ├── a4e824c247f97b4f524b885a358c0d0008e4e161.nq.gz
│   ├── a7765f7ba6e1d7d9dbe28132cfa2cbbb486dd52c.nq.gz
│   ├── afbef58415e67f9c6b2cea98fb3633824bd5e9ec.nq.gz
│   ├── b29e18354aed040c1f39a128ebf210e96fa89b4c.nq.gz
│   ├── b7104ffc3541d1be46a2c94bb26eb4c870970426.nq.gz
│   ├── baa2566d45e3a2ec1857b7453c65244d97c4d40a.nq.gz
│   ├── c6268b6adea2a6192d4ea330b3af8a5b5043ced5.nq.gz
│   ├── cc0c128257cace9da1d84bb92bbcc4f3a7ed9257.nq.gz
│   ├── dfad587eff9e56dbdb0af95a63b4cf55a3af1409.nq.gz
│   ├── e4b7e589a0e2e96626a14cdbdc990731fe75ec40.nq.gz
│   └── eac3867b307a6d837cf5529d0b090cc8fa6b4e70.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── f8ec666b4d1b654e4ff6aedd356f510dcac09f83.nq.gz
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

[postmanlabs/httpbin](https://github.com/postmanlabs/httpbin)

---
*Parsed on 2026-10-18 by [repolex](https://repolex.ai)*
