# Altium Schematic Design and Review
Status: Draft — expanded workflow; Altium version and engineer style profile must be project-confirmed.

## Purpose
Create a readable, electrically correct, maintainable Altium schematic that follows approved project conventions and is traceable to verified component data.

## Required inputs
Requirements and architecture baseline; circuit calculations; exact component MPNs; verified symbols/footprints; Altium Designer version; project templates/libraries; approved Engineer Style Profile; sheet/hierarchy conventions.

## Procedure
1. Inspect the project before editing: project files, document hierarchy, libraries, variants, parameters, compiler settings, design rules, existing conventions, and Altium version. Preserve a clean backup or work on a copy/branch.
2. Load the approved Engineer Style Profile. If no profile exists, infer only provisional conventions from multiple approved examples; label them provisional and do not claim they are the engineer's established style.
3. Plan sheets around functional boundaries and signal flow. Define sheet names, hierarchy, ports, power domains, and cross-sheet connectivity before drawing.
4. Verify every symbol against the exact component datasheet: designator, pin number, pin name, electrical type, hidden pins, no-connect pins, power pins, exposed pad, and package mapping. Record source and library revision.
5. Apply consistent designators, value/MPN parameters, net labels, power ports, sheet entries, connector naming, units, grid, fonts, wire junctions, and annotation policy from the style profile. Maintain readability; never sacrifice correctness for visual imitation.
6. Show functional grouping and signal direction clearly. Separate analog, digital, power, high-voltage, RF, and isolation domains where appropriate. Make power entry, protection, filtering, test access, programming/debug, boot/reset, and critical interfaces easy to review.
7. Add component parameters required for BOM and procurement: manufacturer, exact MPN, description, value, tolerance/rating where relevant, lifecycle/source metadata according to project policy.
8. Cross-check power pins, decoupling, pull-ups/pull-downs, strap states, unused pins, connectors, net names, and pin swaps. Confirm no hidden power pin or global net creates unintended connectivity.
9. Compile and run ERC using the actual Altium project and configured rules. Review every error and warning; fix real issues and document justified exceptions with rationale and owner.
10. Independently inspect critical nets and pin mapping against datasheets. Where available, compare generated netlist against intended connectivity and prior approved design.
11. Save, reopen, and confirm the project compiles without missing libraries or broken references. Record tool version, actions actually performed, and files changed.

## Deliverables
Native project/schematic files; sheet hierarchy map; component/library provenance; pin-map checklist; BOM parameter check; ERC report and exception register; change summary; unresolved issues.

## Quality gate
No unverified pin mapping, unintended floating/shorted net, unexplained ERC finding, broken library link, or missing critical component parameter. Schematic is readable at normal review scale and matches approved conventions where evidence exists.

## Agent constraints
Do not claim ERC, compile, or netlist checks ran unless the tool executed them. Do not overwrite the only source copy. Do not silently alter connectivity or component MPNs. If Altium automation is experimental, use a disposable copy and read-only inspection first; preserve logs and rollback path.
