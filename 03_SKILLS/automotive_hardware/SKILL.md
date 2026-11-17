# Automotive Electronics Hardware Engineering
Status: Draft — project-specific tailoring and qualified review required.

## Scope
Design and review electronic control units and automotive subsystems. This skill is an applicability and engineering workflow; it does not establish ISO 26262 compliance, OEM approval, or vehicle qualification.

## Intake
Identify vehicle domain and ECU function; 12 V/24 V/48 V or other electrical system; battery and load-dump/transient environment; location in vehicle; connector/harness; grounding and shielding; thermal/vibration/moisture/chemical exposure; lifetime; diagnostic and fault-tolerant behavior; target OEM; production volume; and target markets.

## Standards and qualification selection
Assess applicability of:
- ISO 26262 for functional safety when hazard analysis and item classification establish relevance.
- ISO 16750 series for environmental and electrical loads according to mounting location and subsystem.
- ISO 7637 series for conducted electrical transients on vehicle supply/signal lines.
- CISPR 25 and ISO 11452 series for automotive EMC emissions/immunity as specified by the OEM/product requirements.
- AEC-Q100/Q101/Q200 for relevant semiconductor/passive component qualification context.
- OEM-specific electrical, EMC, environmental, validation, and manufacturing specifications.

Confirm exact editions, amendments, test levels, setup, acceptance criteria, and applicability with the customer/OEM and authorized standards sources. Do not use remembered limits or generic automotive defaults.

## Engineering workflow
1. Establish system boundary, vehicle interfaces, safety goals and failure behavior where applicable.
2. Build supply/transient, load, grounding, harness, and environmental budgets.
3. Select protection architecture for reverse battery, overvoltage, jump start, load dump, cranking, ESD, EFT/surge where relevant, and short/open fault cases.
4. Review power input, reverse polarity, transient suppressors, filtering, hot-plug, ground offsets, and thermal dissipation against sourced requirements.
5. Review communication physical layers (CAN/LIN/Ethernet/USB/etc.), common-mode range, termination, ESD, wake/sleep, bus fault behavior, and harness coupling.
6. Review EMC current paths, enclosure/shield/connector interfaces, filter placement, common-mode and differential-mode paths, and return paths.
7. Apply derating, component qualification, lifecycle, traceability, and production test requirements.
8. Define verification matrix with test setup, severity, operating mode, monitoring, acceptance, and failure recovery.
9. Record safety analysis artifacts and independence requirements where functional safety applies.

## Required outputs
Automotive standards applicability record, interface-control document, power/transient budget, protection analysis, EMC design review, component qualification matrix, environmental profile, verification matrix, and open OEM questions.

## Stop conditions
Do not claim ISO 26262, CISPR 25, ISO 7637, ISO 16750, AEC-Q, or OEM compliance without the applicable requirements, edition, test evidence, and authorized review.
