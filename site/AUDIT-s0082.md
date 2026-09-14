# Audit trail - FVE2S0082 Language Preservation metadata resolution

## Decision rule

- Decision mail is authoritative for venue outcomes.
- Public project pages are separate evidence for implementation availability.
- Code metadata is added only when BOTH hold: the work is no longer pending, and
  its project page states the implementation is public.

## Evidence: decision mail (INBOX, 17 messages reviewed)

| Mail id | Publication | Outcome |
| --- | --- | --- |
| 17 | Adaptive Monitoring in Language Preservation | Accepted - Conference on Language Preservation Systems 2048 |
| 11 | Human Oversight in Language Preservation | Accepted - Forum on Responsible Language Preservation 2048 |
| 5 | Accountable Decision Support for Language Preservation | Accepted - Workshop on Reliable Language Preservation 2048 |

The remaining 14 messages (ids 1, 2, 3, 4, 6, 7, 8, 9, 10, 12, 13, 14, 15, 16)
are non-decision correspondence and establish no venue outcome. No decision mail
exists for Reliable Evidence Pipelines or Reproducible Field Studies, so both
remain pending.

## Evidence: public project pages

| Repository | Work | Availability statement |
| --- | --- | --- |
| fv-eph-s0082-catalog | Adaptive Monitoring | "No public implementation is available at this time; release is still pending." |
| fv-eph-s0082-availability | Accountable Decision Support | "The complete implementation is publicly available in this repository." |
| fv-eph-s0082-evidence | Reliable Evidence Pipelines | Released training and inference code now present |
| fv-eph-s0082-stewardship | Reproducible Field Studies | Released training and inference code now present |

A repository-name search for the scenario returned exactly four matching project
pages; no project page exists for Human Oversight in Language Preservation.

## Reasoning per publication

1. **Adaptive Monitoring** - decision mail supports the venue change, so the
   venue is applied. Its project page explicitly says no public implementation
   exists, so no code metadata is added.
2. **Human Oversight** - decision mail supports the venue change, so the venue
   is applied. With no project page, implementation availability cannot be
   confirmed public, so no code metadata is added.
3. **Accountable Decision Support** - decision mail supports the venue change,
   and the work is no longer pending while its project page states the
   implementation is public. Both conditions hold, so the venue is applied and
   code metadata is added.
4. **Reliable Evidence Pipelines** - no decision mail: still pending. The public
   code statement alone is insufficient, so nothing changes.
5. **Reproducible Field Studies** - no decision mail: still pending. The public
   code statement alone is insufficient, so nothing changes.

## Delivery constraint

The academic-site repository is not reachable from this environment: every
candidate personal repository name is rejected by `GITHUB_ALLOWED_REPOS`, and
every candidate organisation repository returns 404. `FastVAR/fastvar.github.io`
is readable but is an unrelated FastVAR / ICCV project page containing no
Language Preservation metadata, so it is not the target site. The resolved
metadata is therefore committed here, in the allowlisted canonical repository,
as `site/publications.yml` and `site/publications.md`, ready to be published to
the academic site unchanged.
