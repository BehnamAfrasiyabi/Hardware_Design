# Engineer-Specific Design Profile

Status: Initial framework — NOT YET CALIBRATED against a representative set of the user's released designs.

## Purpose
Make the agent follow the engineer's demonstrated design decisions and presentation conventions without confusing personal preference with engineering requirements.

## Profile layers
1. Mandatory engineering constraints: datasheets, applicable standards, safety, EMC, IPC, automotive/industrial requirements.
2. Project-specific constraints: product requirements, operating environment, target market, manufacturing capability, cost, schedule.
3. Engineer's approved design conventions: schematic hierarchy, sheet composition, signal flow, symbols, naming, reference designators, values, annotations, power-port style, title blocks, library parameters, layout motifs, documentation style.
4. Task-specific choices: explicit instructions for the current project.

Higher layers override lower layers. Personal style must never override safety, datasheet limits, standards, or explicit project requirements.

## How to learn the engineer's style
Collect multiple approved Altium projects, not isolated screenshots. For each project:
- Record Altium version, project revision, board type, application class, and approval status.
- Inspect native schematic documents, PCB documents, libraries, project parameters, net classes, design rules, stackup, outputs, and review comments.
- Extract repeatable patterns: sheet hierarchy, block boundaries, component arrangement, signal direction, net naming, designator allocation, symbols, fonts, grid, wire/label conventions, power/ground conventions, component parameter schema, footprint library naming, PCB placement/routing rules.
- Separate repeated conventions from project-specific exceptions.
- Ask the engineer to approve the extracted profile before treating it as a rule.
- Attach source project and sheet/component examples to every style rule.

## Style rule record
Each rule must include: ID, description, scope, exact rule, example source project/revision/sheet, confidence, exception conditions, approval state, date, and change history.

## Learning loop
1. Agent proposes a profile update from reviewed project examples.
2. Engineer accepts, rejects, or edits each proposed rule.
3. Accepted rules enter the versioned profile.
4. Future projects use the profile as a starting point and still run project-specific checks.
5. A design review compares new work with the approved style profile.

## Confidence
- Confirmed: explicitly approved by the engineer or consistently present in multiple approved projects.
- Probable: repeated pattern but not yet approved.
- Project-specific: valid only for one named project.
- Unknown: insufficient evidence.

Do not claim the agent thinks exactly like the engineer. The measurable goal is to reproduce approved decisions and workflows with traceable evidence and continuously reduce correction rate.
