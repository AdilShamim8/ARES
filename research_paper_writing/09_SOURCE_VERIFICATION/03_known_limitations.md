# Known limitations & re-check schedule

Honesty about what this library cannot promise, so users know where to re-verify.

## Volatile figures (will drift)

| Figure | Why it drifts | Re-check where |
|:---|:---|:---|
| Coursera/edX ratings & enrollment | Continuously updated by learners | The course page |
| YouTube views & subscriber counts | Continuous | The channel/playlist page |
| "Free to audit" availability | Platforms occasionally change audit policies | Course page (enroll button) |
| Nature Masterclasses individual pricing | Institutional sales model; prices by negotiation | nature.com/masterclasses + your library |
| Enago/Upskill per-course prices | Promotions vary | learn.enago.com / upskill.researcher.life |

## Figures we deliberately did not guess

- **Total lesson-hours** for the Wiley 14-module course (the independent breakdown lists modules
  and lessons but not hours; the platform page did not state hours at verification time).
- **Exact price of Nature Masterclasses** individual access (institutional sales).
- **Whether a specific Coursera course currently offers a free audit track** — the platform's
  403-to-bots behavior meant availability was corroborated via search snippets and third-party
  listings rather than the enroll button itself.

## Structural limitations

1. **The catalog is a snapshot.** New courses launch; some are retired (as Publons Academy was,
   in 2024). Re-verify quarterly; see the schedule below.
2. **Some platforms meter automated reads.** Coursera and nature.com blocked some direct
   fetches; those profiles lean on search-indexed snippets of the platform's own pages plus
   third-party corroboration — noted per-profile in its Sources section.
3. **YouTube channel recommendations are judgment calls.** The channel list combines one
   university-writing-center recommendation (Baylor GWC, 2023) with reach/quality signals
   visible at verification time; other excellent channels exist.
4. **Book "best for" labels are editorial.** The bibliographic facts (editions, publishers,
   authors) are verified; the *pairing advice* reflects this library's pedagogy.

## Re-check schedule (for maintainers)

| Cadence | What |
|:---|:---|
| Quarterly | Course ratings, prices, audit availability, playlist video counts |
| Semi-annually | Course existence (retirements/renames), book editions |
| On venue-template changes | All `templates/`-related pairing notes |

To re-verify a profile: open its **Sources** URLs, confirm each header-table fact, update the
**last-verified** date, and commit with a `verify(rpw):` message.
