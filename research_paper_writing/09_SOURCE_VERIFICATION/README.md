# 09 · Source verification — the library's audit trail

This folder is what makes the library trustworthy rather than merely useful: every number in the
110 files traces back to a URL read on a specific date, and the method, the URLs, the limits,
and the upkeep rules are all written down.

| # | File | What it holds |
|:---|:---|:---|
| 01 | [Verification method](01_verification_method.md) | The exact procedure used on 5 Nov 2026 — platform reads, third-party corroboration, and how blocked fetches were handled |
| 02 | [URL master list](02_url_master_list.md) | Every URL consulted, grouped by resource type — the re-checking checklist |
| 03 | [Known limitations](03_known_limitations.md) | What drifts, what was not verifiable, and the re-check schedule |
| 04 | [Update policy](04_update_policy.md) | Quarterly maintenance pass, commit conventions, and the new-resource checklist |

## The one-sentence version

> No claim about an external resource enters this library without having been read from the
> live web during verification — and every profile tells you where to re-check it yourself.

*Compiled 5 November 2026.*
