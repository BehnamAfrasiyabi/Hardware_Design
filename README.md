# Hardware Design AI Engineering Knowledge

A vendor-neutral, modular engineering knowledge base and specialist skill library for electronics product development. The long-term goal is to make an AI agent reproduce the engineer's approved workflow and design conventions while preserving engineering evidence and human control.

## Lifecycle scope
1. Requirements analysis and hardware architecture
2. Component research and selection
3. Circuit design and calculations
4. Altium schematic design
5. PCB design
6. Simulation and verification
7. Manufacturing preparation
8. Firmware and embedded software

## Core architecture
- `SKILL.md`: portable agent entry point.
- `AI_INSTRUCTIONS.md`: universal instructions for different AI systems.
- `01_CORE/`: engineering rules, evidence, personalization, standards applicability, and quality gates.
- `02_KNOWLEDGE_BASE/`: reusable domain knowledge.
- `03_SKILLS/`: native lifecycle, orchestration, automotive/industrial, and curated external specialist skills.
- `04_TOOLS/`: Altium automation, EDA integrations, simulation, and automation.
- `05_TEMPLATES/`: requirements, component selection, design review, engineer style profile, and standards applicability.
- `06_VALIDATION/`: checklists and test procedures.
- `07_REFERENCES/`: authoritative source index.

## Agent workflow
1. Classify the product and target markets.
2. Load project requirements, standards applicability, and the approved engineer style profile.
3. Select a lead architect, task specialists, and an independent reviewer.
4. Research exact parts from primary sources and show calculations.
5. Design in Altium using the approved schematic/PCB conventions and project constraints.
6. Validate through native EDA checks, simulation, independent review, and physical tests as required.
7. Record decisions, findings, evidence, and approval gates.

## Learning the engineer's style
The agent must learn from multiple approved native Altium projects. It should extract sheet hierarchy, block layout, symbols, naming, designators, net labels, power conventions, title blocks, libraries, PCB placement/routing, and documentation patterns. The engineer must approve extracted rules before they become normative. See `01_CORE/engineering_personalization.md`.

## Standards
Standards are selected per product category, target market, customer/OEM, installation, and risk. IPC, IEC, CISPR, ISO, AEC-Q, OEM and regulatory documents must be checked at the exact applicable edition. The repository stores original checklists and references, not copyrighted normative standards text. See `01_CORE/standards_applicability.md`.

## External specialist skills and tools
Selected third-party documents are stored with their license and attribution under `03_SKILLS/EXTERNAL/`. Altium live-session automation is documented under `04_TOOLS/eda-agent/`. External material is not automatically validated for this repository.

## Evidence labels
- VERIFIED: supported by authoritative evidence, measurement, or completed verification.
- CALCULATED: derived using stated inputs and method.
- ASSUMED: adopted but not confirmed.
- ESTIMATED: approximate judgment with uncertainty.
- UNKNOWN: not established; never silently guess.

AI output is not engineering approval. Critical designs require qualified review, simulation where appropriate, and physical validation.

## Maturity
See `VERSION.md` and `CHANGELOG.md`. Imported skills and new native skills remain Draft until technically reviewed and validated on representative projects.
