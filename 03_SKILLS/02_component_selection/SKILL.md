# Component Research and Selection
Status: Draft — expanded workflow; requires review against representative projects.

## Purpose
Select exact, orderable components using authoritative evidence, worst-case suitability, lifecycle risk, manufacturability, and project sourcing constraints.

## Required inputs
Approved requirements and interface limits; schematic function; operating/environmental conditions; package and assembly constraints; target lifecycle/volume/cost; approved vendors and sourcing policy; library conventions.

## Procedure
1. Translate each circuit function into a component specification: electrical range, precision, bandwidth, noise, transient behavior, thermal limits, package, pinout, reliability, qualification, lifecycle, and cost.
2. Search manufacturer product pages, datasheets, errata, reference designs, application notes, and package/land-pattern documents. Distributor listings are useful for orderability, not as sole authority for electrical claims.
3. Verify the exact full manufacturer part number (MPN) including suffixes, package, temperature grade, tape/reel, voltage option, memory density, speed grade, and qualification. Never transfer evidence from a similar family member without confirming applicability.
4. Build a comparison matrix using the parameters that decide the design. Include min/typ/max and test conditions, not just typical values. Explain why each candidate passes or fails.
5. Check absolute maximum ratings separately from recommended operating conditions. Evaluate startup, shutdown, sequencing, transients, load steps, fault states, temperature corners, tolerance stack-up, aging, and derating where relevant.
6. Check ecosystem compatibility: logic thresholds, drive strength, pull-ups, clocking, reset, boot straps, package pin mapping, thermal pad, required passives, firmware support, programming/debug, and reference-layout constraints.
7. Verify package drawing and land pattern. Record dimensions, pitch, pad geometry, exposed pad/via needs, polarity/pin-1 marker, courtyard and assembly constraints. Do not create a footprint from a distributor thumbnail.
8. Assess lifecycle and procurement. Record lifecycle status, authorized source, stock/lead-time observation date, MOQ, alternates, country/region constraints, and single-source exposure. Stock is volatile and must be timestamped.
9. Apply project sourcing policy. For this repository's default workflow, check LCSC first; if an exact suitable listing is unavailable, check Mouser, then DigiKey. This is a sourcing preference, not permission to choose an electrically inferior substitute.
10. Select primary and fallback parts. Define whether alternates are pin-to-pin, footprint-compatible, firmware-compatible, or require redesign. Record qualification and approval status.
11. Create or update library entries only after pinout, symbol, footprint, 3D model, parameters, and source provenance are verified. Run library checks before use.

## Required evidence record
MPN; manufacturer; function; datasheet revision/date and page/table; operating and absolute limits; package drawing; land-pattern source; critical calculated margins; lifecycle; dated distributor links/order codes; approved alternate mapping; known errata; unresolved risks; reviewer.

## Quality gate
No selected part relies solely on an AI answer, search snippet, or distributor summary. Exact MPN and suffix match every cited source. Critical limits are checked at relevant corners. Footprint and pin numbering are verified. Availability claims include an observation date. No alternate is called drop-in unless every relevant pin, electrical, thermal, mechanical, and firmware dependency is checked.

## Agent constraints
Never fabricate MPNs, stock, prices, datasheet pages, qualification status, or footprints. If a primary source cannot be accessed, mark the item unverified. Do not silently replace an approved component; provide impact analysis and request approval.
