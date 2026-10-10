# Repolex Knowledge Graph of aio-libs/aiorwlock

RDF knowledge graph data for [aio-libs/aiorwlock](https://github.com/aio-libs/aiorwlock), parsed by [repolex](https://repolex.ai).

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
rlex download aio-libs/aiorwlock
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 420dd9dcc0b379aade93d88cbdc774ff52cdb040
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 420dd9dcc0b379aade93d88cbdc774ff52cdb040
│           └── chunk-001.nq.gz
├── blob
│   ├── 1cc322445906f041720e3fe69d9025b7c7e1a5e2.nq.gz
│   ├── 1ceacd84c8cdf25987d2b402d71b4366d1bbb086.nq.gz
│   ├── 248dab1b6d07b34428b08ffcaee5a86b73e8bd6d.nq.gz
│   ├── 2ce48a2b6ed128092f56c3791a689b9d80f0eb02.nq.gz
│   ├── 36979982708b367032730848375b2a457cf360b8.nq.gz
│   ├── 42021b084d14dc718d4e75ae53d2a1f2c74599d9.nq.gz
│   ├── 51be53e81cfae01162331fbdb23a90d2d8a17f56.nq.gz
│   ├── 625cbee4f442fd772bf6294e5b594baaca203195.nq.gz
│   ├── 78303322e6014885ebae42cc4edb6e123a5c9303.nq.gz
│   ├── 85b21c0db3c95b7dac7954b0a76b9e0e677ac264.nq.gz
│   ├── 8ebd9feee72de861dc219f65a2bd368815bc0ccb.nq.gz
│   ├── 9ac312a989d08169ea6673cd34050c893f2c33f6.nq.gz
│   ├── 9c392a8adfac96cbf4bbc3c1b9d6abde219ff2a3.nq.gz
│   ├── ae0994328a8dceb88962df432083303627243f2b.nq.gz
│   ├── aeb1900ddd51f1d012da9cd3a6a4403aaa6c6b30.nq.gz
│   ├── b9fb8a6e0f4a5ce99899eb97d872c6b90f4bb678.nq.gz
│   ├── bb94e1f0f8bf378c664fb2d61cad413b56279c2b.nq.gz
│   ├── bcc776eec67b17d1222c35a3ed217a874b4d7301.nq.gz
│   ├── bf4bb29447c0fd4ba79d2495d1be1981c728d974.nq.gz
│   ├── cd498f3459160883d5b17e549408c9465d0f9a8b.nq.gz
│   ├── f61a942b79523f1bb8b0d7803dec63f2bff46a7f.nq.gz
│   ├── faa08ed348a711e6fa0c8f1230ee0dd3051e2b45.nq.gz
│   └── fdffa2a0fd7bfbca016990e698d6ea642934bb55.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 420dd9dcc0b379aade93d88cbdc774ff52cdb040.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 31 files
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

[aio-libs/aiorwlock](https://github.com/aio-libs/aiorwlock)

---
*Parsed on 2026-10-10 by [repolex](https://repolex.ai)*
