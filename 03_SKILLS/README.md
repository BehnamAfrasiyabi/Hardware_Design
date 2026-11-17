# Engineering Skills

Native skills define the repository's intended engineering workflow. External skills are retained under `EXTERNAL/` with attribution and must be reviewed for compatibility before use.

## Native lifecycle workflow

| Stage | Skill | Main controlled output |
|---|---|---|
| 1. Requirements and architecture | `01_requirements_architecture/SKILL.md` | Testable requirements, interfaces, architecture, risk register, verification plan |
| 2. Component research and selection | `02_component_selection/SKILL.md` | Exact MPN, source evidence, comparison, footprint provenance, lifecycle and sourcing risk |
| 3. Circuit design and calculations | `03_circuit_design_calculations/SKILL.md` | Topology, nominal/worst-case calculations, stress and margin evidence |
| 4. Altium schematic | `04_altium_schematic/SKILL.md` | Native schematic, library/pin checks, ERC disposition, connectivity evidence |
| 5. PCB design | `05_pcb_design/SKILL.md` | Stackup, constraints, placement/routing rationale, DRC and physical review |
| 6. Simulation and verification | `06_simulation_verification/SKILL.md` | Reproducible simulation/test records and requirement status |
| 7. Manufacturing release | `07_manufacturing_release/SKILL.md` | Controlled fabrication/assembly package, BOM reconciliation, release manifest |
| 8. Firmware and embedded software | `08_embedded_firmware/SKILL.md` | HW/SW interface map, reproducible build, test and security evidence |

## Cross-cutting skills
- Agent orchestration: `agent_orchestration/SKILL.md`
- Automotive hardware: `automotive_hardware/SKILL.md`
- Industrial hardware: `industrial_hardware/SKILL.md`

## Specialist roles
Select only specialists relevant to the design: analog/mixed-signal, MCU, power, SI/PI, high-speed, PCB/DFM/DFA, EMC/ESD, reliability, validation, and independent design review.

## Required engineering gates
1. Requirements and architecture baseline before detailed implementation.
2. Exact component identity and primary-source evidence before library/BOM approval.
3. Calculation and independent review of critical electrical/thermal margins.
4. Schematic connectivity and ERC disposition before PCB release.
5. Stackup, mechanical constraints, and interface-specific routing constraints before detailed routing.
6. DRC, independent design review, and requirement-linked verification before manufacturing release.
7. Revision-controlled manufacturing package and explicit release authorization.
8. Firmware/hardware compatibility and recovery behavior before firmware release.

## Evidence and status policy
- `Draft`: workflow documented but not independently reviewed on representative projects.
- `Reviewed`: technical review completed and review findings recorded.
- `Validated`: exercised on representative projects with evidence and known limitations documented.
- Imported third-party documents retain their upstream status and are not automatically validated for this repository.

The eight lifecycle documents have been expanded, but remain Draft until they are reviewed and validated against the engineer's real Altium projects and working practices. A detailed checklist is not proof that a tool was run or a design passed.

## Project tailoring
Standards, clearances, impedance, length matching, environmental limits, qualification and safety requirements must be selected for the specific product, market, customer and revision. Never treat project-specific values as universal defaults.
