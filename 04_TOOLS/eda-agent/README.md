# Altium AI Tool Adapter: eda-agent

Upstream: https://github.com/salitronic/eda-agent
License: Apache-2.0. The upstream license is retained here.

## Purpose
Provide a practical bridge between an AI assistant and a running Altium Designer session. Upstream documents live schematic, PCB, library, project, audit, BOM, netlist, and manufacturing workflows through MCP.

## Important status
The upstream README explicitly labels the project experimental and warns that some tools may crash the Altium DelphiScript engine. This repository does not certify its safety or reliability.

## Controlled evaluation protocol
1. Use a disposable copy of a project, never the sole source of a production design.
2. Record Altium version, agent version/commit, Windows/Python environment, MCP client, and enabled tool permissions.
3. Start with read-only inspection: project summary, sheets, components, nets, BOM, design rules, and reports.
4. Compare extracted connectivity and component data with Altium's own compiled project/netlist.
5. Test writes only on a throwaway project; make a checkpoint and inspect every change in Altium.
6. Run native ERC/DRC and independent connectivity audits after edits.
7. Test save/reopen and recovery from interrupted operations.
8. Maintain a compatibility matrix and known-issues list.

## Permission policy
Default to read-only. Enable write operations only for an explicitly scoped task, after backup/checkpoint, with human approval before high-impact mutations. Never allow unattended deletion, library replacement, project conversion, release export, or fabrication ordering.

## Why this matters
The MCP server supplies tool access, not engineering judgment. The native Hardware Design skills, engineer-specific style profile, project requirements, and standards applicability record govern what the agent should design.
