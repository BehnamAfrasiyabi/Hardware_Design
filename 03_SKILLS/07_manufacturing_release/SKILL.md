# Manufacturing Preparation and Release
Status: Draft — expanded controlled-release workflow.

## Purpose
Produce a complete, internally consistent, revision-controlled package that a fabricator and assembler can build without relying on undocumented assumptions.

## Required inputs
Approved Altium project baseline; approved BOM and alternates; fabricator/assembler capability data; board stackup; assembly variants; test/calibration requirements; change and approval records.

## Procedure
1. Confirm release authority and freeze the exact source revision. Record project commit/revision, CAD version, libraries, variants, and release date. Work from a clean release copy.
2. Generate fabrication outputs: Gerber X2 or agreed native data, NC drill, board outline, stackup, impedance/coupon requirements, fabrication drawing, notes, and controlled layer mapping.
3. Generate assembly outputs: BOM with exact MPNs and approved alternates, pick-and-place/centroid, assembly drawings, polarity/orientation, paste layers, stencil notes, variants, and special process notes.
4. Generate test and programming data: programming images/configuration, calibration instructions, production test procedure, fixture/interface requirements, acceptance limits, and traceability fields.
5. Perform DFM/DFA review against the selected supplier's actual capabilities: minimum trace/space, drill and annular ring, copper balance, solder mask, paste, panelization, fiducials, tooling, edge plating, controlled impedance, surface finish, and assembly tolerances.
6. Reconcile BOM with schematic and PCB: every fitted designator has a BOM entry; DNP items are explicit; MPN/package/value/footprint match; alternates are approved and mapped; lifecycle/procurement concerns are visible.
7. Inspect generated plots and 3D/assembly outputs independently. Check board outline, drill registration, layer polarity, solder mask openings, silkscreen, polarity, connector orientation, and revision consistency.
8. Verify outputs were generated from the frozen source, not a stale intermediate. Reopen source and output package where possible; compare hashes/manifests and inspect critical layers.
9. Create a release manifest with file names, revision, generation tool/version, timestamps, checksums, approvals, deviations, and known limitations.
10. Archive source snapshot, release package, reports, supplier correspondence, and approval record. Any subsequent change creates a new revision and requires impact analysis/re-release.

## Deliverables
Fabrication package; assembly package; BOM and approved alternate list; drawings; programming/calibration/test package; DFM/DFA disposition; release manifest and checksums; approval/change records.

## Quality gate
All files map to one approved source revision. BOM and designators reconcile. Supplier capabilities are confirmed. No critical DFM/DFA issue remains unresolved. Output plots and manifest are checked. Required approvals are recorded.

## Agent constraints
Do not place fabrication/assembly orders, publish production files, or declare production release without explicit authorization. Never invent supplier acceptance or qualification. Do not silently substitute parts or change revision after release freeze.
