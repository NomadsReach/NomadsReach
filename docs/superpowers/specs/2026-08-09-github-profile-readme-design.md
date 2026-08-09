# NomadsReach GitHub Profile README Design

## Objective

Create a paste-ready profile README for `NomadsReach` that presents the account as the public landing page of a software engineer working across developer infrastructure, game tooling, game design, and engine-adjacent systems.

## Audience and positioning

The primary audience is experienced engineers, open-source contributors, game-tool developers, and potential collaborators. The profile should communicate technical depth without sounding like a résumé dump or a generic developer template.

The core positioning is:

> Software engineer building the tools between game data and game systems: editors, runtimes, and infrastructure that make complex worlds inspectable, moddable, and usable.

The profile should also state that the author has a master’s degree in software engineering and works in both software engineering and game design.

## Content structure

1. Hero section with the mission statement and a compact identity line.
2. About Me section describing software engineering, game design, systems work, reverse engineering, and developer tooling.
3. Featured Projects section with linked public projects:
   - Behavior Graph Studio: C# desktop editor and viewer for Fallout 4 Havok behavior graphs, including graph editing, validation, animation data inspection, and safe `.hkx` saves.
   - PrismaUI for Fallout 4: C++/F4SE conversion of the PrismaUI framework, embedding Ultralight to provide HTML/CSS/JavaScript interfaces inside Fallout 4.
   - Fallout Anomaly: public modlist and distribution project, linked to its current guide rather than duplicating the guide content.
4. Current Focus section that names FO4RecordEditor, Prisma UI, GodotCK and related engine work, and Fallen World systems. These items may be described without links when no public repository is available under the connected account.
5. Core Technologies section grouped by systems, application/tooling, game/engine, and web/UI technologies.
6. Areas of Expertise section focused on reverse engineering, game tooling, runtime integration, data-heavy editors, modding infrastructure, and cross-platform build/deployment work.
7. Open Source Philosophy section with concise principles: make difficult systems inspectable, document constraints, preserve compatibility, automate repeatable validation, and respect upstream/community licenses.
8. Contact section with the GitHub profile and any stable project or community links available. Do not invent an email address, social account, or community server link.

## Visual and technical direction

- Use GitHub-flavored Markdown with lightweight HTML only where it improves layout.
- Use a restrained GitHub-native visual hierarchy inspired by the supplied examples: one strong opening block, short paragraphs, compact project cards, technology icon rows, and consistent section dividers.
- Use technology badges or icons only in grouped rows that communicate real engineering domains. Avoid badge walls and decorative stacks.
- Add a small, hand-authored engineering signal row near the hero, such as `systems tooling`, `game infrastructure`, `engine work`, and `open source`. Do not use generated vanity metrics.
- Do not use animated GIFs, visitor counters, snake graphs, memes, generic greetings, or decorative noise.
- Do not add GitHub stats unless they communicate something more useful than the project descriptions. Current public profile metrics do not justify a stats block.
- Do not add external screenshots or banners unless a stable, public asset exists. The README must remain fast to load and easy to maintain.
- Keep all factual project claims aligned with the current public READMEs and repository metadata.
- Never imply that private or unlisted work is publicly available. Unlinked current-focus items should be phrased as active engineering areas, not public repositories.

## Public source facts used

- GitHub account: `NomadsReach`, display name `Nomads_Reach`.
- Public repositories visible on the profile: `BehaviorGraphStudio`, `framework-F4-Conversion`, `Fallout-Anomaly`, `opt-out-lists`, and `mod-lists`.
- `BehaviorGraphStudio` README describes a standalone C# viewer/editor for Fallout 4 `.hkx` behavior, character, project, skeleton, and animation files, with graph editing, validation, and safe saving.
- `framework-F4-Conversion` README describes `PrismaUI_F4` as an F4SE plugin using Ultralight to render HTML/CSS/JavaScript overlays in Fallout 4, with C++ APIs, input routing, focus management, and old-gen/next-gen support.
- `Fallout-Anomaly` points readers to the current guide at `https://fallenworld.nexus/guide`.
- Recent public activity includes Behavior Graph Studio editing and animation work, PrismaUI Fallout 4 VR/runtime work, and ongoing Fallout Anomaly releases and metadata updates.

## Acceptance criteria

- The output is a complete `README.md` that can be pasted into the `NomadsReach/NomadsReach` profile repository.
- Every linked repository or external page resolves to the intended destination.
- The README makes the software-engineering and game-design identity clear within the first screenful.
- Featured project descriptions are specific enough to distinguish the work from generic game development.
- FO4RecordEditor, Prisma UI, GodotCK/engine work, and Fallen World are represented without fabricated public links.
- The page reads as a serious open-source engineering portfolio and remains maintainable as projects change.
- Markdown and HTML syntax are structurally valid, with no unclosed layout tags or placeholder contact links.
