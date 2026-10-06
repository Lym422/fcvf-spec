# Freight Custody Verification Framework (FCVF)

An open framework for verifying carrier identity and load integrity at the physical transfer of truckload freight: pickup, intermediate stops, and delivery.

**Status:** Version 0.1, draft for public comment. Not yet adopted by any standards body, association, or agency.
**License:** This document is released under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). The reference implementation ([carrier-verify](https://pypi.org/project/carrier-verify/), seal-check, gate-verify) is released separately under Apache-2.0.
**DOI:** [10.5281/zenodo.23179115](https://doi.org/10.5281/zenodo.23179115) (version 0.1-draft, deposited October 6, 2026)

## What this is

Every truckload shipment changes hands at least twice. At almost every handoff, the releasing party checks paperwork against paperwork and lets the truck go. Nothing confirms that the tractor at the dock belongs to the carrier the load was given to, and nothing confirms that the seal is really there, is the right one, or is still there at the next stop. That gap is what deception-based cargo theft exploits.

FCVF writes down what a gate should actually do, in numbered, testable requirements, at three conformance levels:

- **Basic**: a written procedure, a phone, a browser, and the public FMCSA registry. No equipment.
- **Standard**: plus photographs of the cab and the door closure for every transfer, verification before release, second-channel confirmation of brokered carriers, red flags evaluated and recorded.
- **Full**: plus automated reading of the carrier marking resolved against the registry, automated seal detection (present, absent, uncertain, any seal type), automated comparison with the previous stop, and evidence records in the published structure.

It also defines the **evidence record** (Section 6), a common structure for what was checked, so that records can be shared and aggregated across organizations, and **verdict grading** (release, verify, hold) with the risk rules that drive it (Section 7).

## Contents of this repository

| Path | What it is |
|---|---|
| `spec/FCVF_Specification_v0.1_Draft.pdf` | The specification, current draft |
| `spec/FCVF_Specification_v0.1_Draft.docx` | Editable source of the same |
| `schema/evidence-record.schema.json` | Machine-readable form of the Section 6 evidence record |
| `CHANGELOG.md` | Every change by requirement identifier, with reason |
| `CITATION.cff` | How to cite this document |
| `.zenodo.json` | Deposit metadata |

## How to comment

Open an issue. The most useful comment is one that says *"at my facility this requirement would fail because ..."* followed by the reason. Please include the requirement identifier (for example `P-6` or `S-1`). Comments that are adopted are credited in the change log unless you ask otherwise.

Open questions on which comment is especially wanted for v0.1:

1. **Drop-and-hook** (Section 5.3). Who verifies the second tractor when a yard is unattended, and how is the seal check performed at the hook?
2. **G-4, verification before release.** Facilities that check seals after the drop because of gate throughput: what would make checking before release workable for you?
3. **P-7, driver identification in person.** How should this read for unattended gates and kiosks?

## Versioning

Versions are `major.minor`. A minor version adds requirements or notes, clarifies wording, or changes a conformance level tag; it never withdraws a requirement or changes its meaning. Requirement identifiers are stable; withdrawn requirements keep their number and are marked withdrawn. Proposed changes are posted as issues for at least 30 days before a new version is published.

## Relationship to other work

FCVF sits between documents that already exist and does not replace them: the FBI's April 2026 public service announcement on cyber-enabled cargo theft (it is, in effect, the implementation that announcement asks for), the U.S. DOT's 2025 cargo theft request for information, FMCSA's registration system and its March 2026 bulletin on USDOT number transfers, CBP's CTPAT seal procedures and ISO 17712, the TAPA FSR and TSR, and the TIA Framework to Combat Fraud. Section 9 of the specification maps each requirement to these.

## Author

Lingyu Meng. The requirements come from two years of building and deploying custody-verification systems in a national trucking network; the open implementations share no code, data, or imagery with those systems.
