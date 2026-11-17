# Curated External Hardware Skills

This folder contains selected third-party skill documents retained with their original attribution and license. They are reference specialists, not automatically approved design rules. Read the integration notes before use.

## Included sources

### 1. hardware-agency-agents
- Source: https://github.com/Seahan1/hardware-agency-agents
- License: MIT (see local LICENSE)
- Imported: selected PCB, SI/PI, analog/mixed-signal, STM32, embedded, power, EMC, ESD, reliability, validation, and PCB review role documents.
- Intended use: specialist role prompts and review checklists. They require project-specific evidence and adaptation to the engineer's Altium conventions.

### 2. AI-PCB-layout
- Source: https://github.com/ChengminLi/AI-PCB-layout
- License: CC BY 4.0 (see local LICENSE)
- Imported: power PCB design skill.
- Intended use: staged power-layout workflow, physical current-loop reasoning, explicit evidence, and human approval gates. Preserve attribution when sharing adaptations.

### 3. eda-agent
- Source: https://github.com/salitronic/eda-agent
- License: Apache-2.0 (see `04_TOOLS/eda-agent/LICENSE`)
- Imported: its autonomous design skill.
- Intended use: Altium live-session automation adapter. The upstream project currently labels itself experimental; do not connect it to valuable design files without backups and controlled testing.

## Not copied as executable skills
- `aklofas/kicad-happy`: useful KiCad-only analysis skills for datasheets, BOM, SPICE, EMC, and board review. Not included as directly executable because the target EDA workflow is Altium. Source: https://github.com/aklofas/kicad-happy (MIT).
- `Seeed-Studio/kicad-mcp-server`: KiCad-specific schematic/PCB analysis and ERC/DRC MCP. Source: https://github.com/Seeed-Studio/kicad-mcp-server.
- `nevenfo/kicad-agentic-mcp`: KiCad 10 agentic execution with deterministic plans, evidence, rollback, and native validation. Source: https://github.com/nevenfo/kicad-agentic-mcp (AGPL-3.0; review obligations before reuse).
- `chopinfeng/awesome-hardware-skills`: discovery index for additional hardware agent projects. Source: https://github.com/chopinfeng/awesome-hardware-skills.

## Selection warning
Stars, recent activity, or a polished README do not establish engineering correctness. Every imported skill must pass source review, project validation, and compatibility checks before promotion into the native skill set.
