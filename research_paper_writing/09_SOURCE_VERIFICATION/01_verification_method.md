# How this library was verified

## The rule

> No claim about an external resource enters this library without having been read from the
> live web during verification. Memory is not a source.

## The procedure (executed 5 November 2026)

1. **Platform-page reads.** For every course: the hosting platform's own page (Coursera course
   pages, edX, nature.com, researcheracademy.elsevier.com, wileyresearcheracademy.com,
   tephinet.org, ocw.mit.edu, risingscholars.net, springernature.com) was fetched and parsed —
   instructor, module/unit counts, ratings, review counts, enrollment, and price model were
   transcribed from what the page itself states.
2. **Search-engine corroboration.** Each resource was independently searched (z-ai web search)
   and at least one *third-party* source (Class Central, MoocList, university LibGuides, publisher
   announcements, press coverage) was read to confirm provider, availability, and scope.
3. **Where platforms blocked scraping** (Coursera pages sometimes return 403 to automated
   fetchers; Nature Masterclasses redirects through an IDP), the numbers were taken from the
   search-result snippets of the platform page itself plus corroborating third-party pages —
   and the profile says which.
4. **Video-platform reads.** The YouTube playlist page was rendered in a headless browser and
   its title, channel, video count, per-video titles/lengths/views, and total views were read
   from the rendered page text.
5. **Unverifiable = marked.** Anything that could not be confirmed (e.g., exact lesson-hours
   for some free guides; the current individual price of institutionally-sold products) is
   recorded in [`03_known_limitations.md`](03_known_limitations.md) rather than guessed.

## What "verified 5 Nov 2026" means on each file

Every profile's header table carries a **last-verified date**, and its **Sources** section
lists the exact URLs consulted. If a rating or price is quoted, it was on the page that day.
Prices and ratings drift; the sources section tells you where to re-check.

## Authorship tools

- Headless-browser automation (agent-browser) for the playlist page
- Web search + page fetches for everything else
- All generation scripts persisted in the repository's history (and the contributor's local
  `scripts/` directory) so the library can be regenerated and re-audited

*Compiled 5 November 2026 by the ARES maintainers.*
