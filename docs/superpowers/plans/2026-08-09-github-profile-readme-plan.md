# GitHub Profile README Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Create a paste-ready `README.md` for the `NomadsReach` GitHub profile that presents a serious software engineer working across game tooling, developer infrastructure, and game design.

**Architecture:** One self-contained Markdown document in the task outputs directory. Use GitHub-flavored Markdown plus small, explicitly closed HTML tables for compact project and technology layouts. Keep factual project links limited to verified public destinations and describe unlinked current-focus work without implying it is public.

**Tech Stack:** GitHub-flavored Markdown, limited HTML tables, shields.io technology badges only where useful, GitHub repository links.

## Global Constraints

- Never use em dashes.
- Do not use generic greetings, visitor counters, snake graphs, memes, flashy animations, or vanity stats.
- Make the software-engineering and game-design identity clear in the first screenful.
- Mention the master’s degree in software engineering exactly as user-provided, without inventing an institution or graduation date.
- Link only verified public destinations: the NomadsReach profile, BehaviorGraphStudio, framework-F4-Conversion, Fallout-Anomaly, and the Fallout Anomaly guide.
- Represent FO4RecordEditor, Prisma UI, GodotCK/engine work, and Fallen World as active engineering areas when no verified public repository link is available.
- Keep the document fast to load, readable in GitHub dark mode, and maintainable as project links change.

---

### Task 1: Draft the profile README

**Files:**
- Create: `outputs/README.md`

**Interfaces:**
- Consumes: The approved design spec at `docs/superpowers/specs/2026-08-09-github-profile-readme-design.md` and the verified public project facts in that spec.
- Produces: A complete profile README ready to paste into `NomadsReach/NomadsReach`.

- [ ] **Step 1: Write the hero and identity block**

Create a concise opening with:

```markdown
# Nomads_Reach

Software engineer building the tools between game data and game systems.

I design editors, runtimes, and developer infrastructure that make complex worlds inspectable, moddable, and usable.
```

Follow it with a compact signal row for systems tooling, game infrastructure, engine work, and open source. Do not add a generic greeting or a personal photo because GitHub already renders the account avatar in the profile sidebar.

- [ ] **Step 2: Write About Me and current focus**

State that the author is a software engineer and game designer with a master’s degree in software engineering. Describe the working areas in plain English: reverse engineering, game systems, tooling, runtime integration, and maintainable developer workflows.

Include a current-focus list with these exact project areas:

1. FO4RecordEditor and plugin/data tooling.
2. Prisma UI and embedded web interfaces for Fallout 4.
3. GodotCK and related engine work.
4. Fallen World systems, tooling, and mod infrastructure.

Phrase these as current engineering areas, not as public repositories.

- [ ] **Step 3: Write the featured project cards**

Use a two-column HTML table or equivalent compact layout with three linked projects:

```html
<table>
<tr>
<td width="50%" valign="top">

### [Behavior Graph Studio](https://github.com/NomadsReach/BehaviorGraphStudio)

...

</td>
<td width="50%" valign="top">

### [PrismaUI for Fallout 4](https://github.com/NomadsReach/framework-F4-Conversion)

...

</td>
</tr>
</table>
```

Describe Behavior Graph Studio as a C# standalone viewer/editor for Fallout 4 Havok behavior files, including graph editing, validation, animation data inspection, and safe `.hkx` saves. Describe PrismaUI as a C++/F4SE conversion embedding Ultralight so mod authors can build HTML/CSS/JavaScript overlays with input and focus handling. Add Fallout Anomaly as a separate project card linked to both its repository and `https://fallenworld.nexus/guide`, describing it as a maintained modlist/distribution project.

- [ ] **Step 4: Add technologies and expertise**

Group technologies into short rows instead of a large badge wall:

- Systems: C++, C#, Rust, .NET, native Windows/Linux tooling.
- Game and engine: Godot, F4SE/CommonLib, Fallout 4 runtime integration, game data formats.
- UI and integration: HTML, CSS, JavaScript, Ultralight, embedded browser UI, C++/JavaScript bridges.
- Engineering practice: reverse engineering, binary/data tooling, validation, release packaging, CI/build automation, documentation.

Use no icon or badge whose technology is not supported by the reviewed project facts or user-provided work areas.

- [ ] **Step 5: Add philosophy and contact**

Write a concise open source philosophy around inspectability, compatibility, documentation, reproducible validation, and responsible upstream/community collaboration. End with links to the GitHub profile, the public project repositories, and the Fallout Anomaly guide. Do not add an unverified email or social link.

### Task 2: Validate the README

**Files:**
- Test: `outputs/README.md`

**Interfaces:**
- Consumes: `outputs/README.md`.
- Produces: A verified, paste-ready Markdown artifact with no broken project links or malformed HTML.

- [ ] **Step 1: Check forbidden patterns and placeholders**

Run:

```bash
rg -n 'Hi there|visitor|snake|meme|github-readme-stats|github-readme-streak|TODO|TBD|FIXME|—|PLACEHOLDER|example\.com' outputs/README.md
```

Expected: no matches.

- [ ] **Step 2: Check required content**

Run:

```bash
for term in 'FO4RecordEditor' 'Prisma UI' 'GodotCK' 'Fallen World' 'Behavior Graph Studio' 'Fallout Anomaly' 'master' 'software engineer' 'game design'; do rg -q "$term" outputs/README.md || exit 1; done
```

Expected: exit code `0`.

- [ ] **Step 3: Check all linked destinations**

Run:

```bash
for url in \
  'https://github.com/NomadsReach' \
  'https://github.com/NomadsReach/BehaviorGraphStudio' \
  'https://github.com/NomadsReach/framework-F4-Conversion' \
  'https://github.com/NomadsReach/Fallout-Anomaly' \
  'https://fallenworld.nexus/guide'; do
  curl -L --fail --silent --show-error --head "$url" >/dev/null || exit 1
done
```

Expected: exit code `0` for every URL.

- [ ] **Step 4: Inspect the final artifact**

Run:

```bash
sed -n '1,320p' outputs/README.md
```

Confirm that the first screenful contains the mission statement, software-engineer identity, game-design context, and a clear project signal. Confirm every HTML table has matching opening and closing tags and that no section reads like a generic template.

- [ ] **Step 5: Commit the deliverable**

```bash
git add outputs/README.md
git commit -m "feat(profile): add engineering README"
```

The commit body should state that the README presents verified public project work and clearly labels unlinked current-focus areas.
