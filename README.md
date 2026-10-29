# AstraX Launcher

**AstraX Launcher** is an independently developed, native Linux desktop game launcher. The application is currently in **private development**; this public repository provides information about the project, its Minecraft Java Edition features, and its Microsoft authentication integration.

> **Project status:** Development / testing. This is an information-only repository. The private AstraX Launcher source code is not published here.

## Minecraft Java Edition

AstraX Launcher contains a first-party Minecraft Java Edition module that manages game installations and starts Minecraft directly, without running PolyMC, Prism Launcher, or the official Minecraft Launcher.

Implemented features:

- Install and launch official **Minecraft Java Edition** releases using Mojang metadata and game assets.
- Manage **multiple isolated game instances**, with separate worlds, settings, mods and accounts.
- Configure per-instance Java runtime and memory.
- Install and launch **Fabric** and **Quilt** mod loaders.
- Search and manage compatible mods through **Modrinth**, including compatible .mrpack imports.
- Manage profiles, account selection, instance duplication and game logs.
- Microsoft account sign-in via the **OAuth 2.0 Device Authorization Grant** flow.

**Forge / NeoForge:** not yet implemented.

## Microsoft authentication and Minecraft ownership

We are requesting approval for **AstraX Launcher's own Microsoft Entra application registration** to authenticate legitimate Minecraft Java Edition owners.

Our native sign-in flow requests the scopes XboxLive.signin and offline_access. Players authenticate using Microsoft's official sign-in website; the application then requests Xbox Live, XSTS and Minecraft Services credentials and checks for a valid Minecraft Java Edition profile.

- The launcher **does not ask users for their Microsoft account passwords**.
- Account display names and Minecraft player identifiers can be stored locally.
- Authentication tokens are **currently retained only in the launcher's worker process memory** and must be obtained again after it restarts.
- A temporary, clearly labeled third-party OAuth compatibility test exists during development. We are seeking **our own approved Client ID** so that AstraX can use its own application identity instead.
- **Premium multiplayer access is subject to valid Minecraft ownership and successful Microsoft/Minecraft Services authentication.**

## Platform and project status

| Area | Status |
| --- | --- |
| Native Linux launcher | Under active development |
| Official Minecraft Java install/launch | Implemented and tested |
| Multiple isolated instances | Implemented |
| Fabric / Quilt | Implemented and launch-tested |
| Modrinth mod management | Implemented |
| Microsoft device-code sign-in | Implemented and tested with a Minecraft account |
| Own Microsoft Client ID approved for Minecraft Services | **Approval being requested** |
| Forge / NeoForge | Planned |

## Source code, contact and review

This repository is a public information page for a **privately developed project**. Reviewers who need additional technical information can contact the maintainer using the repository's GitHub Issues page.

AstraX Launcher is an **independent** application and is **not affiliated with, endorsed by, or sponsored by Microsoft, Mojang Studios, Minecraft, PolyMC, or Prism Launcher**. Minecraft is a trademark of Mojang Studios / Microsoft.
