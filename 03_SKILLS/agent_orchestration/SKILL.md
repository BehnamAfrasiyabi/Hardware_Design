# Skill: Hardware Design Agent Orchestration

Status: Draft

## Goal
Coordinate specialist skills to perform the engineer's repeatable hardware workflow, while preserving decision traceability and human approval at risk gates.

## Roles
- Lead Hardware Architect: requirements, architecture, trade-offs, integration.
- Component Research Engineer: manufacturer evidence, exact MPN, footprint, sourcing.
- Circuit Design Engineer: topology, calculations, worst-case, simulation.
- Schematic Engineer: sheet architecture, symbols, connectivity, style profile.
- PCB Engineer: stackup, placement, routing, SI/PI, thermal, EMC.
- EMC/Safety/Automotive Specialist: applicability, risk analysis, test plan.
- DFM/DFA Engineer: fabrication, assembly, inspection, rework.
- Embedded Engineer: MCU, pinmux, firmware, boot/security, hardware bring-up.
- Independent Reviewer: adversarial review, requirements traceability, verification evidence.

## Workflow
1. Intake and classify project: consumer, industrial, automotive, medical, safety-related, RF, power, high-speed, or mixed.
2. Load project requirements, standards applicability record, engineer profile, and tool inventory.
3. Build a requirements-to-evidence traceability matrix.
4. Select one primary specialist and relevant supporting specialists per stage.
5. Each specialist returns structured findings and evidence; no specialist can self-approve a safety-critical output.
6. Lead architect resolves conflicts and records decisions.
7. Execute design in small stages with explicit review gates.
8. Run independent review using source files and raw evidence, not only the first agent's conclusions.
9. Close findings and preserve a versioned decision log.

## Mandatory gates
- Requirements and standards applicability
- Architecture and power/interface budgets
- Component selection
- Circuit calculations and schematic connectivity
- PCB constraints and physical implementation
- Verification and EMC/safety risk review
- DFM/DFA and manufacturing release
- Firmware/hardware integration

## Independence
The reviewer must be given the actual project files and requirements. It must not rely solely on summaries from the designing agent. Reviewers report evidence, severity, location, impact, and corrective action.

## Human approval
No irreversible release, fabrication order, safety-related design acceptance, or compliance claim without explicit authorized human approval.
