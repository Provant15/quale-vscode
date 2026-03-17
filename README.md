# Quale Language Support for VS Code

Syntax highlighting and code snippets for the [Quale](https://quale.dev) neuroevolution language.

Quale is a domain-specific language for evolving neural networks using NEAT (NeuroEvolution of Augmenting Topologies). Define agent bodies, worlds, fitness criteria, and evolution parameters in `.quale` files, then let the engine evolve brains that solve your problem.

## Features

- Syntax highlighting for all `.quale` constructs
- Three-tier comment system (`--`, `--!`, `--!!`)
- Code snippets for rapid scaffolding
- Auto-closing brackets and string pairs
- Code folding on brace blocks
- Auto-indentation

## Comment System

Quale uses a semantic comment system:

```quale
-- Regular comment (discarded by parser)
--! NOTE: this needs calibration    (note - preserved in AST)
--!! FIXME: hardcoded value         (critical - blocks --strict mode)
```

| Syntax | Purpose | Visibility |
|--------|---------|------------|
| `--` | Author notes, scratchpad | Parser discards |
| `--!` | Notes, TODOs | Shown in `quale check` |
| `--!!` | Critical issues | Fails `quale check --strict` |

## Snippets

| Prefix | Description |
|--------|-------------|
| `body` | Agent body with sensors and actuators |
| `sensor-internal` | Internal state sensor |
| `sensor-directional` | Directional sensor (4 nodes) |
| `sensor-property` | Item property sensor |
| `sensor-social` | Social/peer sensor |
| `actuator-directional` | Directional actuator (4 nodes) |
| `actuator-trigger` | Trigger actuator |
| `item` | Item with properties and effects |
| `world` | World grid configuration |
| `fitness` | Fitness objectives |
| `evolve` | Evolution experiment |
| `evolve-full` | Evolution with all optional blocks |
| `mutation` | Mutation rate block |
| `speciation` | Speciation block |
| `convergence` | Convergence block |
| `checkpoint` | Checkpoint block |

## Installation

Search for "Quale" in the VS Code Extensions panel, or install from the command line:

```bash
code --install-extension Provant.quale-lang
```

## Links

- [Quale Documentation](https://quale.dev/docs/)
- [Quale Engine](https://github.com/Provant15/quale)
- [Report Issues](https://github.com/Provant15/quale-vscode/issues)
