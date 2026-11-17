# PCB Design and Layout
Status: Draft — expanded workflow; stackup and constraints are project-specific.

## Purpose
Translate a verified schematic into a manufacturable, testable PCB while meeting electrical, mechanical, thermal, EMC, SI/PI, safety, and assembly constraints applicable to the product.

## Required inputs
Approved schematic/netlist; board outline and mechanical data; connector and mounting constraints; component footprints; current and timing budgets; target fabricator/assembler capabilities; operating environment; applicable standards; approved layout style profile.

## Procedure
1. Validate schematic/netlist revision, footprints, pin-1/polarity, 3D models, variants, and mechanical envelope. Resolve library issues before placement.
2. Obtain fabricator stackup options and material data. Define layer count, copper weights, dielectric thickness, reference planes, controlled impedance, and tolerances with the fabricator. Never assume a generic stackup or impedance.
3. Establish constraints before routing: net classes, clearances, creepage, current capacity, differential impedance, length/skew, via types, return path, thermal, antenna/RF, and assembly rules. Record the source and applicability of each critical constraint.
4. Place by function and physical current/signal flow. Prioritize connectors and mechanical features, power conversion loops, decoupling, clocks, memory/high-speed interfaces, analog front ends, RF, isolation, thermal sources, test/programming access, and serviceability.
5. Route critical power loops compactly; minimize high di/dt loop area and maintain intended return paths. Place decoupling close to relevant pins with a low-inductance connection. Avoid splits/voids under critical signals unless an engineered return transition exists.
6. Route high-speed and sensitive signals using interface-specific topology and validated constraints. Consider impedance, reference plane continuity, via stubs/transitions, coupling, crosstalk, skew, termination, connector launch, and package escape. Length matching and impedance values must come from the actual interface, timing budget, stackup, and device guidance—not generic rules.
7. Partition noisy switching/power circuits from sensitive analog/RF circuits based on current paths and return-current behavior. Do not split ground planes by habit; define grounding from circuit topology and EMC/SI/PI analysis.
8. Size copper and thermal paths using current, temperature rise, copper thickness, geometry, airflow, enclosure, and applicable design criteria. Check component derating and thermal coupling.
9. Review EMC/ESD/transient entry paths, chassis/signal-ground strategy, filter placement, shield termination, isolation, creepage/clearance, and cable/connector interfaces where applicable.
10. Review fabrication and assembly: annular rings, drill aspect ratio, solder mask slivers, paste apertures, component spacing, courtyard, fiducials, tooling, panelization, edge clearance, silkscreen readability, and rework access.
11. Run DRC with the intended rule set. Resolve violations or create explicit, justified, reviewed exceptions. Inspect 2D, 3D, layer plots, critical current paths, return paths, and mechanical fit.
12. Review testability: probe access, test points, programming/debug, boundary scan where used, fixture access, and production test strategy. Record design review findings and disposition.

## Deliverables
Stackup and impedance record; constraint/rule set; placement/routing rationale; thermal/SI/PI/EMC review as applicable; DRC report and exceptions; 2D/3D/mechanical review; testability and DFM notes; source revision.

## Quality gate
No unexplained DRC violation, unreviewed mechanical conflict, unknown stackup assumption, critical signal without a defined return path, or unverified creepage/clearance where safety applies. Fabricator constraints and impedance targets are confirmed, not guessed.

## Agent constraints
Never claim SI/PI, thermal, EMC, or DRC validation without the corresponding analysis/tool evidence. Do not universalize project-specific layer stackups, impedances, clearances, or length rules. Preserve source and provide diff/rollback before automated edits.
