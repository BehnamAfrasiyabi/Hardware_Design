# Standards Applicability and Compliance Strategy

Status: Draft. This is a selection framework, not a standards database or certification claim.

## Core rule
Never apply every standard to every project. Determine product category, intended market, end use, electrical risk, installation environment, customer contract, and regulatory obligations first. Record the exact edition and amendments. Obtain standards from authorized sources; do not copy copyrighted standards text into this repository.

## Standards families to assess

| Area | Candidate family/examples | Applicability decision |
|---|---|---|
| PCB design / workmanship | IPC-2221, IPC-2222, IPC-2152, IPC-7351, IPC-A-600, IPC-A-610, J-STD-001 | Select based on board type, design rules, assembly class, and contractually required acceptance level. Verify current edition and scope. |
| EMC emissions/immunity | CISPR 11/32/25, IEC 61000-4-x, FCC Part 15, EN harmonized standards | Select by product category, market, port type, and applicable regulatory route. |
| Automotive EMC | CISPR 25, ISO 11452 series, ISO 7637-2/-3, OEM-specific EMC specifications | Select based on vehicle subsystem, port, OEM, test plan, and vehicle voltage system. |
| Automotive environmental/electrical | ISO 16750 series, LV 124, OEM specifications | Determine mounting location, operating profile, supply transients, temperature, vibration, humidity, and mechanical loads. |
| Automotive component qualification | AEC-Q100/Q101/Q200 | Component qualification context; not a substitute for board/system qualification or application-specific validation. |
| Functional safety | ISO 26262, IEC 61508, IEC 60730, or sector-specific safety standards | Only when safety lifecycle and hazard analysis establish applicability. Do not claim compliance from a checklist. |
| Industrial | IEC 61000 series, IEC 60204-1, IEC 61508, IEC 61131-2, product-specific standards | Select according to equipment class, installation, ports, safety category, and jurisdiction. |
| Environmental/reliability | IEC 60068 series and applicable customer/OEM profiles | Derive test severities from product environment and requirements. |

## Required project standards record
- Product category and intended use
- Target countries/markets and installation environment
- Customer/OEM specifications
- Applicable standards, exact edition/amendments, clauses/tables, and source
- Applicability rationale and excluded standards with rationale
- Required design evidence and verification method
- Certification/test laboratory requirements
- Compliance owner and approval state

## IPC discipline
IPC documents are copyrighted and often require purchase/access. This repository may contain original checklists and summaries with references, but must not reproduce normative tables or substantial standards text. For clearance, creepage, conductor sizing, annular rings, solderability, acceptance class, and workmanship, use the exact applicable standard edition and document the clause/table used.

## Compliance language
Use "designed with reference to", "reviewed against selected clauses", or "tested to the specified method" only when evidence supports it. Reserve "compliant/certified" for the applicable formal process and documented evidence.
