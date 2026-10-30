# Connecticut: law history in git

The statute law of Connecticut as a git repository: one file per section, committed with the official publisher named as author. It follows the shared design of [lexifina/global-law](https://github.com/lexifina/global-law).

**What is in it now (a first build, not complete)**

| Folder | Act | Versions | History |
| --- | --- | ---: | --- |
| `title-33/` | Title 33: Corporations | 4 | Revisions of 2019, 2021, 2023, 2025 |
| `title-47/` | Title 47: Land and Land Records | 4 | Revisions of 2019, 2021, 2023, 2025 |
| `title-47a/` | Title 47a: Landlord and Tenant | 4 | Revisions of 2019, 2021, 2023, 2025 |
| `title-53a/` | Title 53a: Penal Code | 4 | Revisions of 2019, 2021, 2023, 2025 |

Nothing else of Connecticut's law is in it yet.

## Where the text comes from

[General Statutes of Connecticut](https://www.cga.ct.gov/current/pub/titles.htm), Connecticut General Assembly (Legislative Commissioners' Office). Only statute text is taken: section headings and bodies. Source notes, history notes, annotations and cross-references are left out. The State Constitution is not in this first build; no reusable official text of it was found on the General Assembly site.

## Dates

Each commit is dated 1 January of the revision year (2019, 2021, 2023, 2025), the date the Legislative Commissioners' Office revised the edition to.

## What it does not show

- The annual supplements and the Public Acts are not used, so a change is dated by the edition that first prints it, not by its effective date.
- Editions before 2019 are not online at the same path.
- Tables inside sections may be flattened to text.

## How it is checked

- Every unit is read back from git on its day and compared with the corpus (`tools/check_repo.py`; results in `REPRODUCE.md`).
- Each source file is identified by its sha256, in `data/versions.json`.

## What "author" means

The first edition collected (2019) is authored by the publisher (Connecticut Legislative Commissioners' Office) as the oldest version available; each later commit is authored by the edition (for example "General Statutes of Connecticut, 2021 revision") that first prints the change. The committer is always Lexifina.
