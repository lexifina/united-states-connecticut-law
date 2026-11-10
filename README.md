# Connecticut: law history in git

Part of [lexifina/global-law](https://github.com/lexifina/global-law), one git history for every country's law: this is the law of Connecticut, United States, which global-law reads at `united-states/connecticut/acts/`.

The statute law of Connecticut as a git repository: one file per section, committed with the official publisher named as author. It follows the shared design of [lexifina/global-law](https://github.com/lexifina/global-law).

**What is in it now**

Every title of the General Statutes with a section in force: 72 titles (Titles 4c, 13, 17, 19, 36, 38, 39, 45 and 46 were wholly transferred or repealed and are left out).

| Folders | Versions | History |
| --- | --- | --- |
| `title-33/`, `title-47/`, `title-47a/`, `title-53a/` | revisions of 2019, 2021, 2023, 2025; 2026 supplement | from January 1, 2019 |
| every other `title-*/` | revision of 2025; 2026 supplement | from January 1, 2025 |

Sections a later public act rewrites from a stated day ("On and after July 1, 2026, this section ... is to read as follows") change on that day, up to the build day.

## Where the text comes from

[General Statutes of Connecticut](https://www.cga.ct.gov/current/pub/titles.htm), Connecticut General Assembly (Legislative Commissioners' Office). Only statute text is taken: section headings and bodies. Source notes, history notes, annotations and cross-references are left out. The State Constitution is not in this first build; no reusable official text of it was found on the General Assembly site.

## Dates

Each revision is dated 1 January of its year (2019, 2021, 2023, 2025), the date the Legislative Commissioners' Office revised it to. The 2026 supplement, which reprints the sections changed since the 2025 revision, is dated 1 January 2026, the date it is revised to. A text an edition prints as in force "on and after" a later day is dated that day.

## What it does not show

- The Public Acts themselves are not used, so a change is dated by the edition that first prints it (or by the day the edition says it takes effect), not by each act's own effective date.
- Notes that rewrite only a subsection, or several sections at once, on a later day are not applied; neither are the few whose new heading differs from the printed one. The section keeps the edition's text, which points to the note.
- Editions before 2019 are not online at the same path; for most titles, the 2019-2023 revisions are not yet added.
- Tables inside sections may be flattened to text.

## How it is checked

- Every unit is read back from git on its day and compared with the corpus (`tools/check_repo.py`; results in `REPRODUCE.md`).
- Each source file is identified by its sha256, in `data/versions.json`.

## What "author" means

The first edition collected (2019) is authored by the publisher (Connecticut Legislative Commissioners' Office) as the oldest version available; each later commit is authored by the edition (for example "General Statutes of Connecticut, 2021 revision" or the 2026 supplement) that first prints the change. The committer is always Lexifina.
