<p align="center">
  <img src="./assets/readme/tr-ai-daw-hero.svg" width="100%" alt="Tr AI-Daw — an open-source digital audio workstation">
</p>

<p align="center">
  <a href="./README.md"><b>Türkçe</b></a> ·
  <a href="./README_EN.md"><b>English</b></a> ·
  <a href="https://github.com/heshengtao/ai-daw/blob/main/README_zh.md"><b>简体中文</b></a>
</p>

# Tr AI-Daw

**Tr AI-Daw is a full, extensible digital audio workstation project—not a translation-only fork.** This repository develops the product end to end: music arrangement, the audio engine, mixing, plugin hosting, desktop and browser experiences, local AI workflows, and MCP tools for working with AI agents. Turkish is a first-class product goal, not the project's entire scope.

The project builds on the open-source codebase of [heshengtao/ai-daw](https://github.com/heshengtao/ai-daw). Tr AI-Daw is an independent community project, not officially affiliated with or endorsed by upstream; upstream copyright and license notices are preserved.

## What the DAW includes

- **Compose and edit:** arrange MIDI and audio clips on a multitrack timeline; edit notes in the piano roll; automate parameters and export standard formats.
- **Audio and mixing:** real-time playback, timing, DSP/rendering, mixer channels, sends, buses, built-in effects and synthesis.
- **Plugin ecosystem:** host VST3 and CLAP plugins; manage plugins and SoundFont libraries.
- **AI and agent workflows:** let an agent read and edit the running session over MCP; use local audio analysis and music tools without uploading projects.
- **One project, multiple clients:** use the Tauri desktop app or browser interface to work with the same project and history.

<p align="center">
  <img src="./assets/screenshots/01-arrange.png" width="100%" alt="Tr AI-Daw multitrack arrangement view">
</p>

## Development scope

The open development tracks include audio-engine reliability and performance, creative workflows and accessibility, plugin compatibility, local AI/MCP tools, cross-platform packaging, testing, documentation, and Turkish/English UX. These are areas for community collaboration, not dated release promises.

- Product roadmap: [GitHub Project](https://github.com/users/TrKeyboarder/projects/2) and [ROADMAP.md](./ROADMAP.md)
- Bug reports and feature requests: [Issues](https://github.com/TrKeyboarder/tr-ai-daw/issues)
- Design and community discussion: [Discussions](https://github.com/TrKeyboarder/tr-ai-daw/discussions)
- Contributor guide: [CONTRIBUTING.md](./CONTRIBUTING.md)

## Build and run

Prerequisites: stable Rust, Node.js 22+, pnpm 10, and the [Tauri system prerequisites](https://v2.tauri.app/start/prerequisites/).

```bash
git clone https://github.com/TrKeyboarder/tr-ai-daw.git
cd tr-ai-daw
pnpm install --frozen-lockfile
pnpm tauri dev
```

For an optimized, generic Linux x86_64 Debian package:

```bash
CARGO_BUILD_JOBS=1 \
CARGO_PROFILE_RELEASE_LTO=thin \
CARGO_PROFILE_RELEASE_CODEGEN_UNITS=1 \
AIDAW_TARGET=x86_64-unknown-linux-gnu \
pnpm tauri build --target x86_64-unknown-linux-gnu --bundles deb
```

The package is not published as a GitHub Release yet. Follow [Releases](https://github.com/TrKeyboarder/tr-ai-daw/releases) for future builds.

## Architecture

| Path | Role |
| --- | --- |
| `src/` | Vue 3 desktop and browser UI |
| `src-tauri/` | Tauri desktop shell and packaging |
| `crates/daemon/` | Project commands, audio/plugin coordination, MCP and HTTP |
| `crates/engine/` | Audio timing, DSP and rendering |
| `crates/ipc/` | Shared command and event schema |

## License

Application code is Apache-2.0; see [LICENSE](./LICENSE) and [NOTICE](./NOTICE). Downloaded model weights may have separate terms; see [MODELS.md](./MODELS.md).
