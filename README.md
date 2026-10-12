# Roblox Roguelike

Roblox project based on [Frazer's Game Boilerplate](https://github.com/frrazer/roblox-game-boilerplate), imported from commit `d389bbd44a6f83b01cc2a58a2b0cabe1b7112cce`. The baseline is game-agnostic; roguelike-specific gameplay is not implemented yet.

## Setup

Install Aftman, then run from the project directory:

```powershell
./scripts/install.ps1
rojo serve default.project.json --address 127.0.0.1
```

Connect Roblox Studio's Rojo plugin to `localhost:34873`. Read [AGENTS.md](AGENTS.md) for GitHub-first development and disposable task worktrees, and [docs/Boilerplate.md](docs/Boilerplate.md) for the imported layout, implementation rules, packages, and Studio setup.

## Verification

```powershell
./scripts/check.ps1
```

This formats source, generates the sourcemap, runs Luau type/lint analysis, and builds `build/code.rbxlx`. The build is code-only; authored place content is saved and tested separately in Studio.

## Agent skills

Seven Roblox skills, including their references and assets, are included under `.hermes/skills`. Enable project discovery with `hermes skills trust`. Apply the existing Packet, Replica, ProfileStore, Input, Trove, lifecycle, and UIController architecture when using generic skill examples.

## License

The imported boilerplate is public domain under [the Unlicense](LICENSE). Vendored Replica and the imported game-development skills retain their accompanying Apache-2.0 licenses; Wally dependencies retain their own licenses.
