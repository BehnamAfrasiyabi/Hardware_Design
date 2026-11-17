# Firmware and Embedded Software
Status: Draft

1. Define MCU/SoC, silicon revision, toolchain, boot mode, memory map, clock tree, power states, and interfaces.
2. Read datasheet, reference manual, errata, and official SDK/toolchain documentation.
3. Define drivers and interfaces with explicit pin, timing, electrical, and concurrency assumptions.
4. Design initialization/sequencing, watchdog, brownout, reset recovery, error handling, and safe states.
5. Implement modular code with conventions, static analysis, and reviewable changes.
6. Address secure boot, signed updates, debug locking, key storage, input validation, and threat model where applicable.
7. Build reproducibly; record compiler, SDK, flags, dependencies, and configuration.
8. Test unit behavior, interfaces, timing, interrupts/DMA, power modes, fault injection, and recovery.
9. Maintain hardware/firmware compatibility matrix and release notes.

Outputs: architecture, pin/peripheral map, build instructions, source changes, test results, limitations, security notes, compatibility.
Acceptance: reproducible build; no undocumented pin assumptions; fault behavior defined; test types clearly distinguished.
