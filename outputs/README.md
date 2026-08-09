<div align="center">

# Nomads_Reach

### Software engineer building the tools between game data and game systems.

I design editors, runtimes, and developer infrastructure that make complex worlds inspectable, moddable, and usable.

<p>
  <img src="https://img.shields.io/badge/systems_tooling-111827?style=flat-square" alt="Systems tooling" />
  <img src="https://img.shields.io/badge/game_infrastructure-111827?style=flat-square" alt="Game infrastructure" />
  <img src="https://img.shields.io/badge/engine_work-111827?style=flat-square" alt="Engine work" />
  <img src="https://img.shields.io/badge/open_source-111827?style=flat-square" alt="Open source" />
</p>

<p>
  <a href="https://github.com/NomadsReach">GitHub</a>
  ·
  <a href="https://fallenworld.nexus/docs/intro">Fallen World guide</a>
</p>

</div>

---

## About Me

I’m a software engineer and game designer with a master’s degree in software engineering. My work sits at the boundary between low-level systems, game runtime integration, reverse engineering, and tools that help other developers understand and change complex game data.

I’m particularly interested in the parts of software that are usually hidden behind a finished game: file formats, behavior graphs, rendering paths, plugin APIs, build systems, and the workflows that turn difficult technical systems into dependable tools.

My goal is simple: make powerful systems easier to inspect, extend, validate, and use.

## Featured Projects

<table>
<tr>
<td width="50%" valign="top">

### [Behavior Graph Studio](https://github.com/NomadsReach/BehaviorGraphStudio)

A standalone C# viewer and editor for Fallout 4 Havok behavior graphs.

It reads `.hkx` behavior, character, project, skeleton, and animation files directly, then exposes the graph as an editable model. The tool supports node and edge editing, graph variables and events, animation data inspection, validation of crash-prone graph states, and safe save-back with backups and verification.

`C#` · `.NET 8` · `Havok` · `Reverse engineering`

</td>
<td width="50%" valign="top">

### [PrismaUI for Fallout 4](https://github.com/NomadsReach/framework-F4-Conversion)

An F4SE conversion of the PrismaUI framework for building native-feeling web interfaces inside Fallout 4.

The framework embeds Ultralight and exposes C++ APIs for HTML, CSS, and JavaScript overlays, with view lifecycle management, input routing, focus handling, cursor control, and support for old-gen and next-gen Fallout 4 targets.

`C++` · `F4SE` · `Ultralight` · `D3D11` · `HTML/CSS/JS`

</td>
</tr>
<tr>
<td width="50%" valign="top">

### [Fallout Anomaly](https://github.com/NomadsReach/Fallout-Anomaly)

A maintained Fallout 4 modlist and distribution project focused on assembling a coherent, documented, and supportable modded game experience.

The repository carries the public collection and release metadata. The current user-facing documentation lives in the [Fallen World guide](https://fallenworld.nexus/docs/intro).

`Fallout 4` · `Mod infrastructure` · `Release operations`

</td>
<td width="50%" valign="top">

### Engineering through the whole stack

Across these projects, I work from binary formats and native runtime hooks up through editors, browser-backed UI, packaging, documentation, and contributor workflows.

The common thread is developer infrastructure for game systems: tools that make the underlying model visible and the resulting workflow repeatable.

</td>
</tr>
</table>

## Current Focus

<table>
<tr>
<td width="50%" valign="top">

### FO4RecordEditor

Building practical plugin and record-editing workflows for Fallout 4 data. The focus is on structured inspection, safe mutation, reference-aware tooling, and diagnostics that help catch problems before they reach the game.

</td>
<td width="50%" valign="top">

### Prisma UI

Continuing work on embedded web UI for game plugins: view lifecycle, input and focus behavior, native rendering paths, consumer APIs, and the build and deployment systems that make the framework usable by other mod authors.

</td>
</tr>
<tr>
<td width="50%" valign="top">

### GodotCK and engine work

Exploring engine-side tooling and editor workflows around GodotCK and related game systems, with an emphasis on runtime behavior, world data, and infrastructure that scales beyond a single prototype.

</td>
<td width="50%" valign="top">

### Fallen World

Developing the systems, tooling, and operational workflows behind a large modded game experience, from gameplay-facing features to packaging, compatibility, documentation, and maintenance.

</td>
</tr>
</table>

## Core Technologies

<p>
  <img src="https://img.shields.io/badge/C%2B%2B-00599C?style=flat-square&logo=c%2B%2B&logoColor=white" alt="C++" />
  <img src="https://img.shields.io/badge/C%23-239120?style=flat-square&logo=csharp&logoColor=white" alt="C Sharp" />
  <img src="https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white" alt="Rust" />
  <img src="https://img.shields.io/badge/.NET-512BD4?style=flat-square&logo=dotnet&logoColor=white" alt=".NET" />
  <img src="https://img.shields.io/badge/Godot-478CBF?style=flat-square&logo=godotengine&logoColor=white" alt="Godot" />
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white" alt="HTML5" />
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white" alt="CSS3" />
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=111827" alt="JavaScript" />
</p>

| Domain | Tools and technologies |
| --- | --- |
| Systems and native software | C++, C#, Rust, .NET, Windows and Linux tooling |
| Game and engine integration | Godot, F4SE, CommonLib, Fallout 4 runtime integration, native rendering paths |
| Data and reverse engineering | Binary formats, plugin records, Havok behavior graphs, reference-aware editors, validation tooling |
| UI and integration | HTML, CSS, JavaScript, Ultralight, embedded browser UI, native-to-web bridges |
| Engineering workflow | Build automation, release packaging, compatibility work, documentation, reproducible checks |

## Areas of Expertise

- Game tooling and editor development
- Native runtime integration and plugin APIs
- Reverse engineering of undocumented or partially documented formats
- Structured data editing with reference and compatibility constraints
- Embedded web UI and C++/JavaScript integration
- Engine-adjacent systems and game design infrastructure
- Cross-platform build, packaging, staging, and release workflows
- Technical documentation that explains constraints instead of hiding them

## Open Source Philosophy

I value open source that makes hard systems more understandable and more useful to the people who depend on them.

- **Inspectability over magic.** Tools should expose the model, the assumptions, and the failure modes.
- **Compatibility is a feature.** Existing users, data, runtimes, and community workflows matter.
- **Validation belongs in the workflow.** If a mistake can be detected before release or runtime, the tool should help detect it.
- **Documentation is part of the implementation.** A project is not finished when only the code works.
- **Respect the ecosystem.** Build on upstream work carefully, preserve license boundaries, and give contributors a clear path to participate.

## Contact

The best place to reach me is through GitHub and the relevant project repository:

- [NomadsReach on GitHub](https://github.com/NomadsReach)
- [Behavior Graph Studio](https://github.com/NomadsReach/BehaviorGraphStudio)
- [PrismaUI for Fallout 4](https://github.com/NomadsReach/framework-F4-Conversion)
- [Fallout Anomaly](https://github.com/NomadsReach/Fallout-Anomaly)
- [Fallen World guide](https://fallenworld.nexus/docs/intro)

<p align="center">
  <sub>Building tools for the systems behind the worlds.</sub>
</p>
