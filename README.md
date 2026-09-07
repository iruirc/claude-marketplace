# iruirc marketplace

[![release](https://img.shields.io/github/v/tag/iruirc/claude-marketplace?sort=semver&label=release&color=0969da)](https://github.com/iruirc/claude-marketplace)
[![license](https://img.shields.io/github/license/iruirc/claude-marketplace?color=555)](LICENSE)
[![spine-toolkit](https://img.shields.io/github/v/tag/iruirc/spine-toolkit?sort=semver&label=spine-toolkit&color=0969da)](https://github.com/iruirc/spine-toolkit)
[![swift-platform](https://img.shields.io/github/v/tag/iruirc/swift-platform?sort=semver&label=swift-platform&color=0969da)](https://github.com/iruirc/swift-platform)
[![kotlin-platform](https://img.shields.io/github/v/tag/iruirc/kotlin-platform?sort=semver&label=kotlin-platform&color=0969da)](https://github.com/iruirc/kotlin-platform)

Three Claude Code plugins:

- **[spine-toolkit](https://github.com/iruirc/spine-toolkit)** — a task lifecycle orchestrator that
  knows no programming language. Install it alone and you get the process.
- **[swift-platform](https://github.com/iruirc/swift-platform)** — Swift and Apple knowledge, nine
  agents, and the manifest that tells `spine-toolkit` who to dispatch to. Declares `spine-toolkit`
  a dependency, so installing it installs both.
- **[kotlin-platform](https://github.com/iruirc/kotlin-platform)** — Kotlin knowledge for Android,
  Compose Desktop, JVM servers and KMP: sixteen agents fanned out by target, twenty-nine skills,
  and the manifest that tells `spine-toolkit` who to dispatch to. Declares `spine-toolkit` a
  dependency, so installing it installs both.

```
/plugin marketplace add iruirc/claude-marketplace
/plugin install swift-platform     # for a Swift project — pulls spine-toolkit with it
/plugin install kotlin-platform    # for a Kotlin project — pulls spine-toolkit with it
/plugin install spine-toolkit      # for any other stack, paired with a platform plugin of your own
```

Writing a platform plugin for another stack is a documented contract:
[`conventions/platform-contract.md`](https://github.com/iruirc/spine-toolkit/blob/main/conventions/platform-contract.md).
