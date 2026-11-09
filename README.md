# CompleteConfig (Unofficial 1.21.1 Fabric Port)

An unofficial Minecraft 1.21.1 compatibility port of [CompleteConfig](https://github.com/Lortseam/completeconfig), a configuration library for Fabric mods. This port preserves the upstream library APIs and existing configuration features so mods that depend on CompleteConfig can target Minecraft 1.21.1.

## What CompleteConfig provides

- Multiple configuration files per mod, with comments retained when configs are saved.
- Dynamic configuration creation and listeners for reacting to configuration changes.
- Optional configuration screens through the Cloth Config and YetAnotherConfigLib (YACL) adapters.
- Client and server support for dependent mods.

This is a library, not a standalone gameplay mod. It does not add items, blocks, or gameplay behavior by itself.

## Upstream status and port scope

The upstream project is deprecated and its README says it will not receive an official Minecraft 1.21 update. The upstream author recommends YACL for new projects. This port updates the Minecraft, Fabric Loader, Gradle, Loom, and optional configuration-screen dependency targets while retaining the upstream API. The Fabric API version is updated for the included development test mod. This port is intended for existing mods that depend on CompleteConfig; it does not introduce a new library design.

Based on upstream commit `c42877e71f86eff1ae06006e76eaf3d560547ec8`.

## Compatibility

- Minecraft 1.21.1
- Fabric Loader 0.16.14 or newer
- Java 21 or newer
- Optional screen adapters: Cloth Config or YACL

The release JAR bundles the base library and both optional screen adapters. Each adapter still needs its corresponding library installed to open its screen.

The mod ID remains `completeconfig` to preserve compatibility with existing dependent mods. Install this port only in a Minecraft 1.21.1 Fabric instance and do not install it alongside another CompleteConfig copy.

## Credits and source

- Original project and library design: [Lortseam / CompleteConfig](https://github.com/Lortseam/completeconfig)
- Port source: [JustHari01/CompleteConfig-1.21.1-Fabric-Port](https://github.com/JustHari01/CompleteConfig-1.21.1-Fabric-Port)
- Original license: Apache-2.0. The upstream copyright and license notices are retained in `LICENSE` and `NOTICE`.

Report bugs in the 1.21.1 compatibility build to the port repository. Report issues with upstream versions to the original project.

## Build

Use Java 21 and run `gradlew.bat remapJar`. The release artifact is written to `build/libs/`.

This compatibility build and its release description were prepared with AI assistance.
