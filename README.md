# Claude Code 2.1.88 Source Recovery

<p align="center">
  <img src="https://img.shields.io/badge/Version-2.1.88-blue.svg" alt="Version">
  <img src="https://img.shields.io/badge/Status-Recovered-green.svg" alt="Status">
  <img src="https://img.shields.io/badge/Language-TypeScript-blue.svg" alt="Language">
  <img src="https://img.shields.io/badge/UI-Ink%20%2F%20React-orange.svg" alt="UI">
</p>

---

> [!IMPORTANT]
> **This is a source code recovery and reconstruction project for `@anthropic-ai/claude-code` version 2.1.88.**
> This version was published to npm with source maps that allowed the original source to be reconstructed. This project uses the `sources` and `sourcesContent` fields to restore readable source directories, for the purpose of studying Claude Code's CLI architecture, command system, and MCP implementation.
> 
> After recovery from cli.js.map, there are approximately 700,000 lines of code.
> <img width="794" height="387" alt="image" src="https://github.com/user-attachments/assets/ab30578b-d6d2-440c-abde-ddf09e5d42de" />


## Quick Install (Mirror)

Background: On 2026.03.31, Claude Code uploaded a `cli.js.map` file containing the full source code to npm.

<img width="1497" height="242" alt="image" src="https://github.com/user-attachments/assets/b1a01c8d-f14c-46d5-b6cb-4f5b4f90c9ab" />

Since version 2.1.88 has been removed from the [official npm registry](https://www.npmjs.com/package/@anthropic-ai/claude-code/v/2.1.88?activeTab=code), running `npm install @anthropic-ai/claude-code@2.1.88` directly will fail. You can install it via the Tencent cloud mirror cache:

```shell
npm install -g https://mirrors.cloud.tencent.com/npm/@anthropic-ai/claude-code/-/claude-code-2.1.88.tgz
```

<img width="626" height="370" alt="image" src="https://github.com/user-attachments/assets/bcc1d094-f19d-4bd7-b53b-898399c6d117" />

> Act fast — there's no telling when the Tencent cloud mirror cache will also be taken down.

---

## Project Structure Overview

The project is centered around `src/`, closely mirroring the original code organization:

- **`src/entrypoints/`** - CLI entry points and initialization logic
- **`src/commands/`** - The command system (`login`, `mcp`, `review`, `tasks`, etc.)
- **`src/components/`** - Terminal UI components built with **React + Ink**
- **`src/services/`** - Core business logic (policies, sync, remote capabilities, etc.)
- **`src/hooks/`** - Interactive terminal state management
- **`src/utils/`** - Utility functions for auth, file operations, process management, etc.
- **`src/ink/`** - Custom terminal rendering infrastructure

---

## Source Code Highlights

From the recovered code, we can explore the following core design patterns:

- **Command loading mechanism**: Supports a hybrid loading system for built-in commands, dynamic skills, plugins, and MCP commands.
- **Terminal UI art**: How React components are used to build complex interactive interfaces in the terminal.
- **Deep MCP integration**: The concrete implementation and usage of Model Context Protocol within the CLI.
- **Feature Flags**: Feature trimming and build-time control logic found throughout the source code.

---

## Disclaimer

- **Unofficial project**: This repository is not an official Anthropic repository and does not represent Anthropic's position.
- **Copyright notice**: Copyright, trademarks, and related rights to the original code belong to the original rights holder (Anthropic).
- **Research purposes only**: This project is intended solely for archival, structural analysis, and source code study, and should not be treated as an official open-source project.
- **Legal risk**: If you intend to redistribute or use this commercially, please assess the relevant licensing and legal risks on your own.

---

## Next Steps (TODO)

If you want to get it running, try the following steps:
1. Add a `package.json` and configure dependencies.
2. Set up the build toolchain.
3. Handle `bun:bundle` macros and feature flags.
4. Verify that core commands run correctly.

---

## Acknowledgments

Thanks to the **Source Map** that wasn't removed before publishing — it allowed this elegant engineering structure to be reconstructed.

---

## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=ponponon/claude_code_src&type=Date)](https://star-history.com/#ponponon/claude_code_src&Date)
