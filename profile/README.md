<div align="center">

<br>

# Mapanare Research

**The first AI-native programming language.**

*Agents. Signals. Streams. Tensors. First-class, not frameworks.*

<br>

[![Website](https://img.shields.io/badge/mapanare.dev-000?style=for-the-badge&logo=google-chrome&logoColor=white)](https://mapanare.dev)
[![Discord](https://img.shields.io/badge/Discord-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/5hpGBm3WXf)
[![License](https://img.shields.io/badge/MIT-green?style=for-the-badge&label=license)](https://github.com/Mapanare-Research/Mapanare/blob/main/LICENSE)
[![CI](https://img.shields.io/github/actions/workflow/status/Mapanare-Research/Mapanare/ci.yml?style=for-the-badge&label=build)](https://github.com/Mapanare-Research/Mapanare/actions)
[![v0.2.0](https://img.shields.io/badge/version-0.2.0-blue?style=for-the-badge)](https://github.com/Mapanare-Research/Mapanare/releases)

</div>

---

<div align="center">

*Python was the last language built for humans.*
*Mapanare is the first built for AI.*

</div>

---

## What is Mapanare?

Mapanare is a programming language where agents, signals, streams, and tensors are **compiler primitives** — not library constructs bolted on after the fact.

It compiles to **Python** (for ecosystem access) and **native binaries via LLVM** (for bare-metal performance), with a self-hosted compiler in progress.

```mn
agent Classifier {
    input text: String
    output label: String

    fn handle(text: String) -> String {
        return "positive"
    }
}

fn main() {
    let cls = spawn Classifier()
    cls.text <- "hello world"
    print(sync cls.label)
}
```

No `asyncio`. No event loops. No frameworks. Just agents as language primitives.

---

## Projects

| Repository | Description |
|-----------|-------------|
| [**Mapanare**](https://github.com/Mapanare-Research/Mapanare) | The compiler, runtime, standard library, LLVM backend, and VS Code extension |
| [**skills**](https://github.com/Mapanare-Research/skills) | Mapanare skill for AI coding agents — Claude Code, Cursor, Windsurf |
| [**tree-sitter-mapanare**](https://github.com/Mapanare-Research/tree-sitter-mapanare) | Tree-sitter grammar — syntax highlighting for Neovim, Helix, Zed, GitHub |

---

## AI Agent Skill

Give your AI coding agent full fluency in Mapanare. One command — your agent writes idiomatic `.mn` code instantly.

```bash
npx skills add Mapanare-Research/skills
```

Works with **Claude Code**, **Cursor**, **Windsurf**, and any [skills-compatible](https://skills.sh) agent.

| Just ask your agent... | It generates... |
|------------------------|----------------|
| *"Create a sensor monitoring agent"* | Agent with typed channels, signals, anomaly detection |
| *"Build a sentiment analysis pipeline"* | Multi-stage pipe: `Fetcher \|> Extractor \|> Classifier` |
| *"Track metrics with reactive state"* | `signal()`, `computed {}`, `batch {}` with auto-propagation |
| *"Matrix multiply with shape safety"* | `Tensor<Float>[M, N]` with `@` — shapes checked at compile time |
| *"Stream-process logs in real time"* | Pipeline with `filter`, `throttle`, `for_each` |

---

## Performance

LLVM native backend vs Python:

| Benchmark | Speedup |
|-----------|---------|
| Fibonacci (n=35) | **26x faster** |
| Stream Pipeline (1M items) | **63x faster** |
| Matrix Multiply (100x100) | **23x faster** |

Mapanare programs are also the **shortest in lines of code** compared to Python, Go, and Rust across every benchmark. See [full benchmarks](https://mapanare.dev/benchmarks).

---

## Get Started

```bash
# Linux / macOS
curl -fsSL https://mapanare.dev/install | bash

# Windows (PowerShell)
irm https://mapanare.dev/install.ps1 | iex

# Or via pip
pip install mapanare
```

Read the [Getting Started guide](https://mapanare.dev/docs/getting-started) or browse the [full documentation](https://mapanare.dev/docs).

---

## Roadmap

| Phase | Name | Status |
|-------|------|--------|
| 1 | Foundation | **Done** |
| 2 | Transpiler | **Done** |
| 3 | Runtime | **Done** |
| 4 | LLVM Backend | **Done** |
| 5 | Tensors | **Done** |
| 6 | Self-Hosting | **In Progress** |
| 7 | Ecosystem & AI Skills | **In Progress** |

*Currently building v0.3.0 — self-hosted compiler and expanded ecosystem.*

---

<div align="center">

Built by [Juan Denis](https://juandenis.com) with an assist from [Claude](https://claude.ai).

[Docs](https://mapanare.dev/docs) · [Benchmarks](https://mapanare.dev/benchmarks) · [Manifesto](https://mapanare.dev/docs/manifesto) · [Discord](https://discord.gg/5hpGBm3WXf) · [Twitter](https://x.com/mapanare) · [Contributing](https://github.com/Mapanare-Research/Mapanare/blob/main/CONTRIBUTING.md)

</div>
