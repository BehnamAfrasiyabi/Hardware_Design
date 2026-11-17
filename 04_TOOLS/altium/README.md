# Altium Designer Automation and AI Integration

## Official automation surfaces
- Altium Designer Scripting: https://www.altium.com/documentation/altium-designer/scripting
- Scripting setup: https://www.altium.com/documentation/altium-designer/scripting/overview-setup
- Running scripts: https://www.altium.com/documentation/altium-designer/scripting/running-scripts
- Writing scripts: https://www.altium.com/documentation/altium-designer/scripting/writing-scripts
- Altium Designer SDK: https://www.altium.com/documentation/altium-developer-center/altium-designer/sdk
- Altium Developer Center: https://www.altium.com/documentation/altium-developer-center

Altium's scripting framework supports DelphiScript and object interfaces for automating design documents. The current Altium Designer SDK is described by Altium as closed beta; confirm access and version compatibility before planning a new extension.

## Candidate MCP integration: eda-agent
See `../eda-agent/README.md` and `../eda-agent/autodesign/SKILL.md`. It provides a live Altium session bridge, but upstream explicitly warns that the project is experimental and some tools may crash the scripting engine.

## Recommended adoption order
1. Read-only project inspection and report extraction.
2. Schematic and PCB structured data extraction; compare against Altium-native compile/netlist.
3. Read-only design audits and BOM/library checks.
4. Write operations in disposable projects with checkpoints.
5. Controlled editing with explicit approval and native ERC/DRC.
6. Production-project use only after a documented validation campaign.

## Version policy
Never edit or convert a user's Altium project with a different or older version without approval. Record Altium build, bridge revision, Python version, MCP client, and enabled permissions in each test report.
