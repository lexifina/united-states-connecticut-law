# How this repository was made (United States (Connecticut))

This file is written by the build on 2026-10-30, the day the source data was retrieved.

## Sources

| Source | Address | Retrieved | Licence |
| --- | --- | --- | --- |
| General Statutes of Connecticut (Connecticut General Assembly) | <https://www.cga.ct.gov/current/pub/titles.htm> | 2026-10-30 | Statute text is not copyrightable (Georgia v. Public.Resource.Org, 2020). Annotations omitted. |

Every word of law in this repository comes from these sources. Lexifina reads them and records each act's dated versions, and the laws that made each change, in one corpus file. This repository is built from that file.

## What is in it

| Act | Title | Versions | Span |
| --- | --- | ---: | --- |
| `title-33` | General Statutes of Connecticut, Title 33: Corporations | 4 | 2019-01-01 to 2025-01-01 |
| `title-47` | General Statutes of Connecticut, Title 47: Land and Land Records | 4 | 2019-01-01 to 2025-01-01 |
| `title-47a` | General Statutes of Connecticut, Title 47A: Landlord and Tenant | 4 | 2019-01-01 to 2025-01-01 |
| `title-53a` | General Statutes of Connecticut, Title 53A: Penal Code | 4 | 2019-01-01 to 2025-01-01 |

The build made 7 commits:

| Commits | Kind |
| ---: | --- |
| 4 | first version of an act |
| 3 | one law on its in-force day |
| 0 | changes no amendment note explains, credited to the publisher |

Other counts:
- 0 commits on the branch `future`: laws not yet in force on 2026-10-30.
- 0 commits dated 1 January 1970: in force before 1970, with the real day in their `In-force` trailer.
- 4 laws in the record.
- 19 tags.

## Dates

Each commit is dated at noon (America/New_York) on the day the change took effect. The other dates, enacted and published, are trailers.

When a law gives no date of its own, the default rule applies: Each edition is dated the January 1 to which the Legislative Commissioners' Office revised it. https://www.cga.ct.gov/current/pub/titles.htm

## How the history is built

`tools/build.py` turns the corpus into this history in one pass: one commit per law, on the day it took effect. The same corpus always gives the same commit hashes. `tools/check_repo.py` reads every version back from git and compares it with the corpus. `tools/on.py` shows the law as it stood on any date. The corpus format is described in `tools/SCHEMA.md`.

- Corpus: sha256 `e75cfd53c52e44b3ed59a1784c8ad966a1d4cda94bbcf7ed192eaf3dbd700cf9` (2939502 bytes).
- Builder blob hashes (`git hash-object`): `build.py` `a4faa25af85facb64b956b372f6b528aafdd7ec1`, `check.py` `3e59cb6f05eccb94a9ec14431a7f6781221e83ef`, `on.py` `644a6c0857fbcc72562032b58d57aa113fee0641`.
- Python 3.12.10; git version 2.46.0.windows.1.

## Checks

Not yet run for this build.

No second build of this corpus has been compared yet.

## Decisions made by hand

- Only the biennial revisions (2019, 2021, 2023, 2025) are used, dated January 1 of the revision year; the annual supplements and the public acts are not.
- Each change between editions is credited to the edition that first prints it; session laws are not matched to sections.
- Titles 33, 47, 47a and 53a only. The State Constitution is not included: no official reusable text was found on cga.ct.gov.
- Only the section heading and body are kept; source citations, history notes, annotations and cross-references are dropped.

## What AI did and did not do

The scripts that read the sources and build this repository were written by Claude Code running Claude Opus 5.5 (`claude-opus-5-5`) under Lexifina's direction.

No model wrote, translated or corrected legal text. No model runs at build time. Every word of law in this repository comes from the official sources above.

The commit messages are written by `build.py` from the source data.

Model use at data-build time:
- none
