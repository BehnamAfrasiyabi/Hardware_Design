# Firmware and Embedded Software
Status: Draft — expanded hardware/firmware co-design workflow.

## Purpose
Develop firmware that is electrically compatible with the target hardware, recoverable under faults, secure where required, reproducibly buildable, and verifiable against system requirements.

## Required inputs
MCU/SoC exact part and silicon revision; schematic/PCB revision; pin map; datasheet, reference manual, errata; boot and memory architecture; toolchain/SDK; interface requirements; threat model and safety constraints where applicable.

## Procedure
1. Establish exact silicon, package, revision, board revision, clock sources, power domains, boot straps, memory map, debug/programming path, and toolchain versions. Read datasheet, reference manual, errata, and official SDK documentation.
2. Build a hardware/software interface-control table: pin, alternate function, electrical level, direction, reset state, pull, drive, timing, peripheral, connector, and schematic reference. Identify conflicts and reserved pins.
3. Define initialization order and dependencies: power-good, clocks, pin mux, external memories, peripherals, sensors, communication links, watchdog, and application start. Include brownout, reset, boot failure, and partial-power cases.
4. Define module boundaries, driver contracts, error codes, timeouts, concurrency model, ISR/DMA ownership, buffer lifetime, and resource budgets (RAM, flash, stack, CPU, bandwidth, energy).
5. Implement defensive drivers and state machines. Validate external inputs, handle bus errors/timeouts, avoid unbounded waits, and define safe outputs during faults. Keep hardware-specific assumptions explicit.
6. Address security proportionately to product threat model: secure boot, signed firmware, anti-rollback, key provisioning/storage, debug access, update recovery, transport protection, and vulnerability handling. Never embed production secrets in source or logs.
7. Build reproducibly. Record compiler/linker versions, SDK, flags, dependencies, generated files, configuration, linker map, binary hash, and build environment. Pin dependency versions where practical.
8. Test unit logic, drivers with mocks/HIL, peripheral timing, interrupt/DMA contention, communication faults, reset/brownout recovery, watchdog, low-power states, boot/update rollback, and security controls as applicable.
9. Use static analysis, warnings-as-errors where feasible, code review, memory/concurrency review, and hardware-in-loop testing. Separate host simulation from target-board evidence.
10. Maintain compatibility matrix across firmware version, PCB revision, component variants, bootloader, and calibration data. Document upgrade/downgrade behavior and field recovery.
11. Release source, binary, map file, build instructions, configuration, test reports, SBOM/dependency inventory where appropriate, security notes, and release notes.

## Deliverables
Hardware/software interface map; firmware architecture; source and build configuration; reproducible build record; binary and hashes; test evidence; security review; compatibility matrix; release notes.

## Quality gate
No undocumented pin assumptions or unresolved peripheral conflicts. Reset/boot/fault behavior is defined. Builds are reproducible. Critical interfaces and recovery paths are tested on target hardware when required. Security claims are backed by implementation and test evidence.

## Agent constraints
Never claim target execution or hardware testing from a host build. Do not expose credentials, keys, device identifiers, or production secrets. Do not change pin assignments, boot configuration, fuse/option bytes, or deployed update behavior without impact analysis and explicit approval.
