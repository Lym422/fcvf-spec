# Publishing checklist for v0.1

Status: v0.1-draft deposited manually on Zenodo on October 6, 2026 (DOI 10.5281/zenodo.23179115). Remaining steps: push this repository to GitHub, enable the repository in Zenodo's GitHub settings so future releases archive automatically, and open the three issues for the open questions. Make a new Zenodo version only when the text changes (draft 3), not for the DOI insertion alone.

## Original checklist

1. Create the GitHub repository `fcvf-spec` (public). Push these files. The repository links already point to github.com/Lym422/fcvf-spec.
2. Fill the date in CITATION.cff. Add an ORCID if you have one (free at orcid.org; it takes five minutes and makes the record easier to find).
3. On zenodo.org, sign in with GitHub, enable the `fcvf-spec` repository under GitHub integration. Zenodo reads `.zenodo.json` automatically on each release.
4. On GitHub, create a release tagged `v0.1-draft` with the PDF attached. Zenodo archives it and issues a DOI within a few minutes.
5. Copy the DOI into: CITATION.cff, README.md, the title page of the specification (rebuild the PDF), and the Section 5.4 progress item in the NIW statement.
6. Record the date. That date is the first new line in the petition's progress section.
7. Open three GitHub issues, one for each open question in the README, so commenters have a place to reply.
