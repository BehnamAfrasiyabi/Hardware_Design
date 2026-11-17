# Simulation and Verification
Status: Draft — expanded evidence and test workflow.

## Purpose
Use analysis, simulation, inspection, and physical testing to demonstrate that design requirements are met, while clearly stating evidence strength and limitations.

## Required inputs
Requirements traceability matrix; design revision; calculation records; component models and source; test access; target conditions; available tools/instruments; safety constraints.

## Procedure
1. Start with a verification question linked to requirement IDs. Choose method: inspection, analysis, simulation, demonstration, or physical test. Explain why the method is suitable.
2. Define pass/fail before execution: stimulus, operating conditions, limits, tolerance, duration, sample count, measurement points, and treatment of uncertainty.
3. For simulation record tool/version, solver, model name/version/source, model validity range, netlist/design revision, parameters, initial conditions, boundary conditions, parasitics, temperature, load, and corner selection.
4. Verify model suitability. Identify idealized or missing effects (package parasitics, layout coupling, magnetic saturation, thermal coupling, nonlinear protection, source impedance, firmware timing). Do not extrapolate beyond validated model range without qualification.
5. Run nominal and meaningful worst-case/corner cases. Sweep parameters that materially affect the result. Preserve input files, configuration, logs, raw data, plots, and scripts.
6. Compare results with hand calculations, datasheet limits, and requirement acceptance criteria. Explain discrepancies rather than selecting the favorable result.
7. For bench tests document DUT revision/serial, fixture, wiring, instruments, calibration status, probe loading, bandwidth, sample rate, uncertainty, ambient conditions, firmware, setup photos, and safety precautions.
8. Execute tests with appropriate current/voltage/thermal limits and stop conditions. Record raw observations, failures, anomalies, deviations, and retest conditions.
9. Perform root-cause analysis for failures. Link corrective action to schematic/PCB/firmware revision and add regression tests.
10. Review evidence independently. Separate passed, failed, blocked, not-run, and inconclusive items. A planned test is not a passed test; simulation is not a physical test.
11. Update traceability and release evidence after every design change that affects verified requirements.

## Evidence classification
- **Calculated:** analytical result with assumptions and source.
- **Simulated:** result from a documented model and tool setup.
- **Inspected:** visual or rule-based inspection with recorded scope.
- **Bench-tested:** measured physical behavior with setup and instrument details.
- **Qualified/certified:** only when the relevant formal process and authorized evidence exist.

## Deliverables
Verification plan and matrix; simulation/test procedures; tool/model/configuration records; raw results and reports; deviations; root-cause/corrective-action records; updated requirement status.

## Quality gate
Every result is reproducible and tied to a revision. Acceptance limits were defined before execution. Calibration and uncertainty are considered where material. Evidence type and limitations are explicit. No requirement is marked passed without adequate evidence.

## Agent constraints
Never fabricate logs, measurements, screenshots, instrument calibration, or test outcomes. Never report a test as passed if it was not executed. Protect people and equipment: high voltage, high current, RF, batteries, and thermal tests require suitable fixtures, limits, and competent supervision.
