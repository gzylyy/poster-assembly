# Poster Assembly

**English** · [简体中文](README.zh-CN.md)

A practical skill for planning posters, producing independent visual assets, and handing them off for editable layout. Created and maintained by **Fishking**.

The workflow keeps composition decisions, visual materials, typography, and output checks separate so a local correction does not require rebuilding the whole poster.

<p>
  <img src="examples/folded-light/layout.svg" width="240" alt="Text-free layout reference with reserved space for typography">
  <img src="examples/folded-light/poster.svg" width="240" alt="Folded Light vector demonstration with separate artwork and editable type">
</p>

**Example:** [brief → layout → separate assets → assembled poster](examples/folded-light/README.md). The artwork is an original, reproducible SVG demonstration; it is not presented as an AI-generated result or a model quality benchmark.

## What it helps with

- Single posters and series that need separately editable assets, detail views, or manual composition.
- Checking real copy length before expensive visual production.
- Preserving product identity while varying backgrounds or visual styles.
- Planning source pixels, cropping, print dimensions, and channel-specific exports.
- Diagnosing mismatched perspective, lighting, contact shadows, and cutout edges.
- Providing material prompts, placement parameters, revision notes, and delivery inventories.

For an ordinary standalone illustration or an upscaling-only request, use the relevant image tool directly rather than this full workflow.

## Requirements and scope

Use an agent host that supports `SKILL.md` instructions. The host needs suitable image generation or editing tools for steps that create or modify visuals. Final assembly is normally performed by the user in a design application with editable typography and layers.

The repository contains instructions, templates, and an SVG example. It does not bundle an image model, connector account, or image-generation credits. Available output sizes, transparency, cost, and editing capabilities depend on the tools in the session.

## Install in Codex

Download and extract the [repository ZIP](https://github.com/gzylyy/poster-assembly/archive/refs/heads/main.zip), then copy **`skills/poster-assembly`** into a supported skills directory. A separate GitHub Release is not required for this installation. For a user-level installation, the resulting entry point is:

```text
~/.agents/skills/poster-assembly/SKILL.md
```

On Windows, `~` is your user profile directory. Keep the four reference documents, `agents/openai.yaml`, and `LICENSE` with `SKILL.md`; copying only the main file breaks its references.

For a project-local installation, place the same folder at `.agents/skills/poster-assembly` in the project. Choose one installation scope to avoid duplicate entries. Restart the host if the new skill does not appear. See the [official skill documentation](https://learn.chatgpt.com/docs/build-skills) for current discovery locations and host differences.

This repository also includes a portable [plugin manifest](plugin.json) for hosts that support that format. Hosting the files on GitHub does not itself create a marketplace listing; direct folder installation is the documented setup here.

## Try it

Start with a planning-only request:

```text
Use $poster-assembly and respond in English.
Plan one 2:3 screen poster for a fictional paper-art exhibition.
Target export: 1200 × 1800 px. Palette: deep blue, warm paper, orange.
Provide an information hierarchy, material list, and layout proposal.
Do not generate images yet. Ask only for missing critical details.
```

For a Chinese request, see [中文快速开始](README.zh-CN.md#快速开始). In hosts with a skill picker, select the installed skill through that host's interface.

## Workflow

| Stage | Output |
|---|---|
| 0. Clarify | Reused brief, key gaps, target use, and existing authorizations |
| 1. Plan | Information hierarchy, real-copy capacity, layout, and material list |
| 2. Review | A simple composition reference, approved before high-resolution production |
| 3. Produce | Independent assets, detail checks, actual file dimensions, and limitations |
| 4. Assemble | Coordinates, cropping, masking, lighting, and layer guidance |
| 5. Finish | Editable text, output-specific checks, and a delivery inventory |

Reuse an existing approved layout where it applies. Continue within an existing tool and budget authorization; request further decisions when the actual scope changes or the user asks for step-by-step approval.

## Language policy

The GitHub introduction is available in English and Simplified Chinese. The authoritative skill body and detailed references are currently **Chinese**, with bilingual discovery metadata and an English display name. The English README is not a full translation of the skill.

Ask the agent to respond in your preferred language. Start with the planning-only prompt above to check your host's behavior. We maintain one instruction set to avoid contradictory rules between translations; see [language and translation policy](docs/LANGUAGE.md).

## Repository contents

```text
plugin.json
README.md / README.zh-CN.md
LICENSE
skills/poster-assembly/
  SKILL.md
  agents/openai.yaml
  references/
  LICENSE
examples/folded-light/
  README.md / brief.md
  layout.svg
  assets/background.svg / assets/hero.svg
  poster.svg
docs/LANGUAGE.md / PUBLISHING.md
```

## Quality checks and contributions

The skill has been checked for its manifest, local references, numeric examples, and scenario-level behavior. These checks do not certify every image model, printer, or editor. The example's SVG files are self-contained; the final composition preserves text and artwork as separate groups.

For reports or improvements, describe the brief, host, expected behavior, actual behavior, and the relevant stage. Do not include private client material. See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

[MIT](LICENSE) · Copyright © 2026 Fishking. Keep the license with redistributed copies, including the standalone skill folder.
