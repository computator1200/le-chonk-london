# Le Chonk in London: Mistral Vibe Hackathon (21 Nov 2026)

Direction, strategy and full decision evidence for the one-day in-person Mistral
hackathon at Fora - Chancery House, London, Sat 21 Nov 2026 (arrive 08:30; hack 10:00-18:00; pitches 19:00-21:00 GMT).
Team build: **ChonkVid**, an epidemic simulation of self-spreading prompts through
a live population of Mistral agents, with measured R0 and a computed vaccine result.

Start here: **DECISION-BRIEF.md** (self-contained; includes the questions a cold
reader should attack).

## Status

Post-event, updated Sun 22 Nov 2026. The team built ChonkVid and pitched it at Fora
Chancery House on 21 Nov, a five-person entry aimed at Track_01, Bonus_02 and
Special_03.

**Result: did not place, and did not make the finalists.** No prize, no credits.

What was actually built and measured on the day, taken from the team run rather than
from projections:

| Claim | Number |
|---|---|
| Live run | 40 agents on Ministral 8B, 39 infected |
| Detector control arm | 0/30 false positives |
| One-hop spread | 28/30, p 0.93, CI 0.79-0.98 |
| Hardening the whole fleet | 30/30 stopped |
| Hardening 20% of the fleet | epidemic survived, R 1.7 against a 40-60% herd threshold |
| Attack rate | 0.96, against 0.76 random and 0.60 targeted |
| Vaccine on an unseen payload | 0.67 to 0.23 |
| Voxtral voice channel | 20/20 through speech, 0/20 after the vaccine |

This repository is now a record of the attempt rather than a submission: the
pre-event strategy, the execution centre, and the evidence behind those numbers. The
submitted build lives in the team repo, Maya2314/Oh-Lawd-He-Comin.

### Honest retrospective

- **The demo lagged the build.** At submission the Cloudflare worker was still
  serving the pre-diagnostic build while the VPS on port 8793 had the fixed version,
  so anyone following the QR link could have seen an older app than the one measured.
- **Most of the preparation went into choosing the idea**, through a 100-seed funnel
  and a collision audit over 980 competitor analogues. The judging rewarded the pitch
  and a working demo, so that work bought confidence rather than points.
- **We pitched the measured result together with its limits**: targeted hardening beat
  random in only 5 of 8 seeds, and the herd threshold was never reached. Honest, and
  harder to land in five minutes than one clean claim.

## Contents

| Path | What it is |
|---|---|
| DECISION-BRIEF.md | The whole picture in one self-contained file, plus what to challenge |
| HACKATHON.md | The build brief: event facts, one-day plan, stack, demo script, risks |
| IDEA-STRATEGY.md | Nine scored candidates, the advanced-layer stress test, why eight were killed |
| FINAL-VALIDATION.md | The 10/10 winner-pattern validation with the past-winner table |
| FUNNEL-FINAL-VERDICT.md | The blind 100-seed funnel: clusters, gates, collision corpus, pairwise verdict |
| PASS1-SANITIZED-BRIEF.md | The sanitized brief the four isolated ideators received |
| ENGINE-RUN-RECONCILIATION.md | Why the HackForge engine's own pick was rejected on its own red team's findings |
| chonkvid/ | The app (own git repo, git-ignored here so it can go public alone). See its README |
| command-centre/ | 10-file execution centre for the build day (01–04, 06, 07, 09–11, 13) |
| evidence/hackforge-run/ | Raw engine outputs: final recommendation, collision, feasibility |
| evidence/briefs/ | The engine brief as submitted |
| evidence/collision-corpus/ | 980 scraped live competitor analogues (JSON) behind the collision audit |
| evidence/event-research.md | The original event research brief (verified 20 Nov 2026) |

## The one-line summary

Fleets get red-teamed one prompt at a time in a spreadsheet; ChonkVid runs your
whole fleet as a live epidemic and returns the measured spread probability and R0,
evidence that targeted hardening beats random hardening at the same dose, and a
merge-ready vaccine patch in one command.

Provenance: strategy produced 20 Nov 2026 in an OpenCode session using live
research (organiser pages, judge recaps, winner write-ups), the local HackForge
engine, and four isolated ideation panels. Push this repo private until after
the event; flip public afterwards if wanted (other attendees could read it today).
