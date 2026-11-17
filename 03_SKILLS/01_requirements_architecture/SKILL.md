# Requirements Analysis and Hardware Architecture
Status: Draft — expanded workflow; requires review against representative projects.

## Purpose
Turn an incomplete product idea into a testable, traceable hardware specification and an architecture whose risks and trade-offs are explicit. Do not start detailed schematic capture while critical interfaces, operating conditions, or safety constraints remain ambiguous.

## Required inputs
Product brief and use cases; target markets and deployment locations; operating/storage environment; power source and range; interfaces and external loads; mechanical envelope; production volume and cost target; service life; safety/security expectations; existing designs and approved style profile.

## Procedure
1. **Establish context.** Identify stakeholders, users, system boundary, external systems, use cases, misuse cases, operating modes, service conditions, and foreseeable faults. Separate confirmed facts from assumptions and questions.
2. **Create requirements.** Assign stable IDs (e.g. SYS-PWR-001). Write one requirement per statement using measurable language. Record rationale, source, priority, owner, verification method, acceptance limit, and status. Avoid unverifiable words such as fast, robust, low-noise, or automotive-grade unless quantified.
3. **Build an operating-condition matrix.** Include nominal/minimum/maximum supply, transients, load states, temperature, humidity, vibration/shock, EMC exposure, duty cycle, startup/shutdown, brownout, reverse connection, and fault conditions as applicable. Do not assume every category applies.
4. **Define interfaces.** For each connector and signal document direction, electrical levels, absolute limits, loading, timing, protocol, isolation, protection, pinout, return path, startup state, and behavior during faults. Identify ownership of interface requirements.
5. **Develop architecture.** Produce functional block diagram, power tree, clock/reset concept, data/control flow, partitioning, safety/security boundaries, and preliminary thermal, power, memory, bandwidth, and cost budgets.
6. **Compare alternatives.** Evaluate plausible architectures where the choice materially affects risk. Record criteria, evidence, trade-offs, rejected options, and decision owner in an Architecture Decision Record (ADR).
7. **Assess risks.** Maintain risk register with cause, effect, likelihood, severity, detectability where useful, mitigation, verification, owner, and residual risk. Highlight single-source parts, immature technologies, thermal bottlenecks, high-energy paths, and unclear compliance obligations.
8. **Plan verification and traceability.** Link each requirement to architecture blocks, design artifacts, and one or more verification methods: inspection, analysis, demonstration, or test. Define pass/fail before testing.
9. **Baseline.** Freeze a revisioned requirements/architecture baseline. Changes require impact analysis across circuit, PCB, firmware, mechanical, sourcing, compliance, cost, schedule, and verification.

## Required deliverables
- System requirements specification and requirements traceability matrix.
- Operating/environmental conditions table and interface-control document.
- Block diagram, power tree, clock/reset and data-flow diagrams.
- Preliminary budgets and architecture alternatives/ADR.
- Risk, assumption, dependency, and open-question registers.
- Verification strategy and baseline revision.

## Quality gate
No critical requirement is unmeasurable; all external interfaces have defined electrical behavior; assumptions and unresolved questions are visible; high-risk items have owners and mitigation; every high-priority requirement has a verification method. A reviewer must be able to trace product intent to an acceptance test.

## Agent constraints
Do not invent product requirements, environmental ratings, market approvals, or customer commitments. Mark unknowns explicitly and ask focused questions when an unknown changes architecture or safety. Never claim certification or compliance from an architecture review alone.
