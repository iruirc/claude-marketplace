# iruirc marketplace

Two Claude Code plugins:

- **[spine-toolkit](https://github.com/iruirc/spine-toolkit)** — a task lifecycle orchestrator that
  knows no programming language. Install it alone and you get the process.
- **[swift-platform](https://github.com/iruirc/swift-platform)** — Swift and Apple knowledge, nine
  agents, and the manifest that tells `spine-toolkit` who to dispatch to. Declares `spine-toolkit`
  a dependency, so installing it installs both.

```
/plugin marketplace add iruirc/claude-marketplace
/plugin install swift-platform     # for a Swift project — pulls spine-toolkit with it
/plugin install spine-toolkit      # for any other stack, paired with a platform plugin of your own
```

Writing a platform plugin for another stack is a documented contract:
[`conventions/platform-contract.md`](https://github.com/iruirc/spine-toolkit/blob/main/conventions/platform-contract.md).
