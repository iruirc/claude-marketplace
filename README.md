# iruirc marketplace

[![release](https://img.shields.io/github/v/tag/iruirc/claude-marketplace?sort=semver&label=release&color=0969da)](https://github.com/iruirc/claude-marketplace)
[![license](https://img.shields.io/github/license/iruirc/claude-marketplace?color=555)](LICENSE)
[![spine-toolkit](https://img.shields.io/github/v/tag/iruirc/spine-toolkit?sort=semver&label=spine-toolkit&color=0969da)](https://github.com/iruirc/spine-toolkit)
[![spine-platform-swift](https://img.shields.io/github/v/tag/iruirc/spine-platform-swift?sort=semver&label=spine-platform-swift&color=0969da)](https://github.com/iruirc/spine-platform-swift)
[![spine-platform-kotlin](https://img.shields.io/github/v/tag/iruirc/spine-platform-kotlin?sort=semver&label=spine-platform-kotlin&color=0969da)](https://github.com/iruirc/spine-platform-kotlin)

Three Claude Code plugins:

- **[spine-toolkit](https://github.com/iruirc/spine-toolkit)** — a task lifecycle orchestrator that
  knows no programming language. Install it alone and you get the process.
- **[spine-platform-swift](https://github.com/iruirc/spine-platform-swift)** — Swift and Apple knowledge, nine
  agents, and the manifest that tells `spine-toolkit` who to dispatch to. Declares `spine-toolkit`
  a dependency, so installing it installs both.
- **[spine-platform-kotlin](https://github.com/iruirc/spine-platform-kotlin)** — Kotlin knowledge for Android,
  Compose Desktop, JVM servers and KMP: sixteen agents fanned out by target, twenty-nine skills,
  and the manifest that tells `spine-toolkit` who to dispatch to. Declares `spine-toolkit` a
  dependency, so installing it installs both.

```
/plugin marketplace add iruirc/claude-marketplace
/plugin install spine-platform-swift     # for a Swift project — pulls spine-toolkit with it
/plugin install spine-platform-kotlin    # for a Kotlin project — pulls spine-toolkit with it
/plugin install spine-toolkit      # for any other stack, paired with a platform plugin of your own
```

Writing a platform plugin for another stack is a documented contract:
[`conventions/platform-contract.md`](https://github.com/iruirc/spine-toolkit/blob/main/conventions/platform-contract.md).
