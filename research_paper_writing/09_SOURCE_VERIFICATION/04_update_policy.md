# Update policy — keeping the library true

## Principles

1. **Facts have birthdays.** Every fact carries its verification date; stale facts are bugs.
2. **One fact, one place to re-check.** Each profile's Sources section is the authoritative
   pointer; updates happen against those URLs.
3. **No silent rewrites.** A correction that changes what a reader would *do* (cost, free/paid
   status, module count) deserves its own commit with a clear message.

## Commit message conventions (this library)

| Prefix | Use |
|:---|:---|
| `feat(rpw):` | New file or new capability in the library |
| `docs(rpw):` | Documentation-only changes to existing files |
| `fix(rpw):` | Correcting a fact that was wrong or drifted |
| `verify(rpw):` | Re-verification pass (no substantive change beyond dates/figures) |

Scope tags in parentheses: `rpw-courses`, `rpw-video`, `rpw-books`, `rpw-guides`,
`rpw-mentorship`, `rpw-tools`, `rpw-paths`, `rpw-verify`, or plain `rpw` for the hub.

## The quarterly maintenance pass (≈2 hours)

1. Open [`02_url_master_list.md`](02_url_master_list.md) top to bottom.
2. For each URL: does it still resolve? Do the header-table facts still hold?
3. Fix drift → commit `fix(rpw-…): correct <fact> in <file> — now <value> (re-checked <date>)`.
4. Update the profile's *last-verified* line even when nothing changed →
   `verify(rpw-…): re-verify <file> against live sources — no changes`.
5. Once a year: re-read [`03_known_limitations.md`](03_known_limitations.md) and prune retired
   resources; search for major new courses worth adding; extend the manifest.

## Adding a new resource (the checklist)

☐ It is real-world (a live URL that resolves) ☐ It survives the three-source test (platform
page + one third-party + fit for this library's mission) ☐ Its profile follows the standard
file anatomy (header table, coverage, why-recommended, ARES pairing, pair-it-with, sources)
☐ It is linked from the relevant folder README and the hub ☐ The commit says what and why

## Removal

Retire rather than delete when possible: mark the profile `> **Status: retired <date> — <reason>**`
at the top, move it out of the main tables, and note the replacement if one exists. History is
part of the library's provenance.
