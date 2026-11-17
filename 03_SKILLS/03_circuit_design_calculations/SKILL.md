# Circuit Design and Engineering Calculations
Status: Draft — expanded workflow; requires review against representative projects.

## Purpose
Develop a defensible circuit topology and prove its operating margins before schematic/PCB release.

## Required inputs
Requirements baseline; interface-control document; selected or candidate components; operating-condition matrix; architecture and approved design conventions.

## Procedure
1. Define each circuit block's function, operating modes, input/output range, startup/shutdown sequence, normal states, fault states, and interaction with adjacent blocks.
2. Draw current paths and signal paths for nominal and abnormal conditions. Identify return paths, energy storage, switching nodes, high-impedance nodes, sensitive analog nodes, and isolation boundaries.
3. Select topology and explain alternatives. Base device models and equations on datasheets, manufacturer application notes, textbooks, or recognized engineering references. Record source and assumptions.
4. Calculate nominal and worst-case behavior. Include component tolerances, temperature coefficients, supply variation, load variation, aging where material, model spread, startup, transient and fault conditions. Use min/max limits rather than typical values for guaranteed margins.
5. Check electrical stress: voltage/current/power, SOA, pulse energy, reverse conditions, inrush, short circuit, clamp energy, gate/base drive, and protection coordination. Distinguish recommended operating limits from absolute maximum ratings.
6. Check analog performance: gain/error budget, offset, bias currents, noise, bandwidth, stability/phase margin, input/output headroom, ADC acquisition, anti-aliasing, reference drive, and grounding as applicable.
7. Check digital/timing performance: logic thresholds, rise/fall times, setup/hold, clock tolerance/jitter, reset timing, bus loading, termination, boot configuration, and asynchronous crossings as applicable.
8. Check power and thermal behavior: efficiency, dissipation, junction temperature estimate, copper/thermal path assumptions, derating, sequencing, brownout, and power-good/reset behavior.
9. Review protection and EMC at circuit level: ESD/surge/transient paths, common-mode/differential-mode filtering, input filtering, shielding/ground reference strategy, and connector entry. Select protection devices using actual waveform, source impedance, clamp behavior, and energy—not voltage label alone.
10. Independently recalculate critical values using a second method, spreadsheet, script, or peer review. Validate equations, units, significant figures, and boundary conditions.
11. Define simulation and bench evidence needed to resolve uncertainty. Record model limitations and what simulation cannot prove.
12. Maintain calculation IDs and link each result to schematic references, requirement IDs, and verification tests.

## Calculation record
Purpose; topology; equation and source; symbols/units; input values and provenance; assumptions; nominal result; worst-case/corner result; margin; component stress; uncertainty; independent check; design consequence; verification method.

## Quality gate
All critical ratings have explicit margin; units and assumptions are reviewable; startup and fault behavior are considered; sensitive/fast loops and return paths are identified; critical results have independent checks; each unresolved uncertainty has an owner and verification action.

## Agent constraints
Never present a typical-value estimate as guaranteed. Do not invent missing component characteristics. Flag calculations that require field solver, SPICE, thermal simulation, safety analysis, or laboratory measurement. Do not mark a circuit safe or compliant solely from hand calculations.
