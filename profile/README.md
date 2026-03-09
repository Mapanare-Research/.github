<div align="center">

<br>

# Mapanare Research

**The first AI-native programming language.**

*Agents. Signals. Streams. Tensors. First-class, not frameworks.*

<br>

[![Website](https://img.shields.io/badge/mapanare.dev-000?style=for-the-badge&logo=google-chrome&logoColor=white)](https://mapanare.dev)
[![License](https://img.shields.io/badge/MIT-green?style=for-the-badge&label=license)](https://github.com/Mapanare-Research/Mapanare/blob/main/LICENSE)
[![CI](https://img.shields.io/github/actions/workflow/status/Mapanare-Research/Mapanare/ci.yml?style=for-the-badge&label=build)](https://github.com/Mapanare-Research/Mapanare/actions)

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

---

## Performance

LLVM native backend vs Python:

| Benchmark | Speedup |
|-----------|---------|
| Fibonacci (n=35) | **26x faster** |
| Stream Pipeline (1M items) | **63x faster** |
| Matrix Multiply (100x100) | **23x faster** |

Mapanare programs are also the **shortest in lines of code** compared to Python, Go, and Rust across every benchmark.

---

## Get Started

```bash
# Linux / macOS
curl -fsSL https://raw.githubusercontent.com/Mapanare-Research/Mapanare/main/install.sh | bash

# Windows (PowerShell)
irm https://raw.githubusercontent.com/Mapanare-Research/Mapanare/main/install.ps1 | iex

# Or via pip
pip install mapanare
```

---

## Roadmap

| Phase | Status |
|-------|--------|
| Foundation | Done |
| Transpiler | Done |
| Runtime | Done |
| LLVM Backend | Done |
| Tensors | Done |
| Self-Hosting | In Progress |
| Ecosystem | Planned |

---

<div align="center">

**Built with care by [Juan Denis](https://juandenis.com)**

[Manifesto](https://github.com/Mapanare-Research/Mapanare/blob/main/docs/manifesto.md) · [Spec](https://github.com/Mapanare-Research/Mapanare/blob/main/docs/SPEC.md) · [Roadmap](https://github.com/Mapanare-Research/Mapanare/blob/main/docs/ROADMAP.md) · [Contributing](https://github.com/Mapanare-Research/Mapanare/blob/main/CONTRIBUTING.md)

</div>
