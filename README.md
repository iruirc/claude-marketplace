# iruirc marketplace

[![release](https://img.shields.io/github/v/tag/iruirc/claude-marketplace?sort=semver&label=release&color=0969da)](https://github.com/iruirc/claude-marketplace)
[![license](https://img.shields.io/github/license/iruirc/claude-marketplace?color=555)](LICENSE)
[![spine-toolkit](https://img.shields.io/github/v/tag/iruirc/spine-toolkit?sort=semver&label=spine-toolkit&color=0969da)](https://github.com/iruirc/spine-toolkit)
[![spine-platform-swift](https://img.shields.io/github/v/tag/iruirc/spine-platform-swift?sort=semver&label=spine-platform-swift&color=0969da)](https://github.com/iruirc/spine-platform-swift)
[![spine-platform-kotlin](https://img.shields.io/github/v/tag/iruirc/spine-platform-kotlin?sort=semver&label=spine-platform-kotlin&color=0969da)](https://github.com/iruirc/spine-platform-kotlin)
[![spine-driver-mobile](https://img.shields.io/github/v/tag/iruirc/spine-driver-mobile?sort=semver&label=spine-driver-mobile&color=0969da)](https://github.com/iruirc/spine-driver-mobile)
[![spine-driver-agent-device](https://img.shields.io/github/v/tag/iruirc/spine-driver-agent-device?sort=semver&label=spine-driver-agent-device&color=0969da)](https://github.com/iruirc/spine-driver-agent-device)

Five Claude Code plugins in three categories — the orchestrator, the platforms that teach it a stack,
and the drivers that let it drive a running app. The Swift and Kotlin platform plugins also expose
their standalone knowledge skills to Codex:

- **[spine-toolkit](https://github.com/iruirc/spine-toolkit)** — a task lifecycle orchestrator that
  knows no programming language. Install it alone and you get the process.
- **[spine-platform-swift](https://github.com/iruirc/spine-platform-swift)** — Swift and Apple knowledge, nine
  agents, and the manifest that tells `spine-toolkit` who to dispatch to. Declares `spine-toolkit`
  a dependency, so installing it installs both.
- **[spine-platform-kotlin](https://github.com/iruirc/spine-platform-kotlin)** — Kotlin knowledge for Android,
  Compose Desktop, JVM servers and KMP: sixteen agents fanned out by target, twenty-nine skills,
  and the manifest that tells `spine-toolkit` who to dispatch to. Declares `spine-toolkit` a
  dependency, so installing it installs both.
- **[spine-driver-mobile](https://github.com/iruirc/spine-driver-mobile)** — declares what the
  `mcp-devices` MCP server can drive on each surface, so Validation drives the app instead of
  handing every UI check to a human. An adapter: it does not ship or install the server.
- **[spine-driver-agent-device](https://github.com/iruirc/spine-driver-agent-device)** — the same
  for `callstack/agent-device`. Pick whichever server you already run; a project names one in its
  `## Validation` block.

## Claude Code

```text
/plugin marketplace add iruirc/claude-marketplace
/plugin install spine-platform-swift   # for a Swift project — pulls spine-toolkit with it
/plugin install spine-platform-kotlin  # for a Kotlin project — pulls spine-toolkit with it
/plugin install spine-toolkit          # for any other stack, paired with a platform plugin of your own
/plugin install spine-driver-mobile    # optional — lets Validation drive a simulator or device
```

## Codex

Add this repository as a Git-backed marketplace, then install either or both platform plugins:

```bash
codex plugin marketplace add iruirc/claude-marketplace
codex plugin add spine-platform-swift@iruirc
codex plugin add spine-platform-kotlin@iruirc
```

Refresh the marketplace and its installed plugins with:

```bash
codex plugin marketplace upgrade iruirc
```

Start a new Codex session after installation or upgrade. Codex gets the standalone platform skills;
the `spine-toolkit` orchestration, agents, commands and driver adapters remain Claude Code components.

Writing a platform plugin for another stack is a documented contract:
[`conventions/platform-contract.md`](https://github.com/iruirc/spine-toolkit/blob/main/conventions/platform-contract.md).
So is writing a driver for an MCP server you do not own:
[`conventions/driver-contract.md`](https://github.com/iruirc/spine-toolkit/blob/main/conventions/driver-contract.md).
