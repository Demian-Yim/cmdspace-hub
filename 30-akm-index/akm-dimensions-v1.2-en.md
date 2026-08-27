# AKM Dimensions v1.2 — Descriptive Dimensions Specification

> **Scoring does not change.** The 25 criteria × level 0-4 anchors × 0-100 total (maturity, M) remain exactly as in v1.1. What v1.2 adds is an *interpretive coordinate system* for that score — three descriptive dimensions (S·A·O) that show whether a given 70 is "a simple system's 70" or "a complex system's 70", plus a theory-grounded grammar for visualizing the aggregated multi-dimensional profiles.

## 1. Why

In measurement terms this is a **construct contamination** problem. The AKM total measures one construct — maturity (quality of operation) — but readers inevitably blend in a second one: scale. An M3 on a single 300-note vault and an M3 on a 12-vault, 10,000-note ecosystem are the same number and different achievements.

We rejected the difficulty-multiplier design (diving/gymnastics style, score = execution × difficulty) for two reasons: ① complexity is not a virtue — weighting it invites participants to inflate accidental complexity (a Goodhart path); ② no single multiplier exists — complexity cuts opposite ways per criterion (recall gets harder at scale, evidence gets easier, weekly cadence is scale-free). Instead we adopt **norming**: as CMMI keeps maturity levels scale-invariant while appraisals state organizational scope, the score stays pure maturity and verifiable descriptive dimensions are reported alongside it.

## 2. The three dimensions

To qualify as a dimension: ① conceptually independent of maturity ② measurable as counts (not self-description) ③ interpretive value — knowing it changes how the same score reads.

### S — Scale (system scale & complexity index)

*How much system is being operated.* Seven measured fields, each 0-3 on log-scaled thresholds; S-index is their mean.

| Field | 0 | 1 | 2 | 3 |
|-------|---|---|---|---|
| notes — knowledge documents | <300 | 300-1,499 | 1,500-5,999 | ≥6,000 |
| stores — vaults/repositories | 1 | 2 | 3-5 | ≥6 |
| runtimes — connected agent runtimes | 1 | 2 | 3-4 | ≥5 |
| automations — standing scheduled jobs | 0 | 1-2 | 3-5 | ≥6 |
| skills — custom skills & commands | <5 | 5-19 | 20-49 | ≥50 |
| humans — governance participants | 1 | 2 | 3-5 | ≥6 |
| yearsActive — years in operation | <1 | 1-1.9 | 2-3.9 | ≥4 |

**Bands**: S-index <0.75 → **S** · <1.5 → **M** · <2.25 → **L** · ≥2.25 → **XL**

Anti-gaming: every field is a spot-checkable count, and S does not enter the score — inflating it only buys you the *less* flattering reading ("that big a system, and this score").

### A — Autonomy (self-operation ratio)

*How much of the recurring operation runs without a human.* A standard 8-item operations checklist keeps systems comparable — each item scored none 0 / manual 0.5 / automated 1, **A = Σ/8** (reported as %):

1. Backup · 2. Search index & embedding refresh · 3. Measurement & benchmarks · 4. Retrospective generation · 5. Hygiene checks (drift/links/lint) · 6. Secret & security scanning · 7. Knowledge promotion/ingestion pipeline · 8. Memory & context grooming

"Automated" = initiated by a scheduler/hook and completed without human intervention. A human *consuming* the result keeps it automated — consumption is what the L pillar scores.

A is not maturity: level 4 is achievable manually (the anchors require records and feedback loops, not cron), and an automated system can be immature (jobs that run but feed nothing back). That independence is what makes the interaction analysis in §4 meaningful.

### O — Output Coupling

*Does the system reach external outputs?* The count of artifacts delivered to third parties through this system in the last 90 days — published posts, lectures, consulting deliverables, releases, reports.

**Bands**: O0 = 0 · O1 = 1-2 · O2 = 3-9 · O3 = 10+

O is heavily occupation-dependent, so it is profile information, never a ranking.

## 3. Profile notation

Standard notation: **`M 77.25 (M3) · S-XL · A 88% · O2`** — one score becomes a four-coordinate profile. In the report schema (1.2) this is an optional `dimensions` block; reports without it remain valid (backward compatible).

## 4. Aggregate visualization grammar

### 4.1 The 2×2 matrix (S × M)

A portfolio quadrant (BCG lineage). Horizontal: S-index (boundary 1.5); vertical: M total (boundary 60 = entering M3).

| | Simple (S<1.5) | Complex (S≥1.5) |
|---|---|---|
| **Mature (M≥60)** | 🚤 Speedboat — complete at small scale | 🚢 Fleet — complete at large scale |
| **Immature (M<60)** | ⚓ Casting off — healthy early state | ⚠️ Overloaded — scale outran operation |

Quadrants are not a ranking — Speedboat and Fleet are both excellent, for different purposes. The only alert quadrant is Overloaded.

### 4.2 The bubble chart (S × A, size = O, color = M band)

Four dimensions on one plane; also the raw scatter beneath the surface analysis.

### 4.3 Polynomial regression + response surface methodology (Edwards & Parry, 1993)

The standard congruence-analysis technique from organizational research:

M = b₀ + b₁S + b₂A + b₃S² + b₄(S×A) + b₅A² + e

- **Core hypothesis — scale-autonomy congruence**: when scale outruns autonomy (S↑ A↓), maintenance debt erodes maturity. In RSM terms: the surface curves downward along the incongruence line (a₄ = b₃−b₄+b₅ < 0).
- **The four surface tests**: congruence-line slope a₁=b₁+b₂ · congruence-line curvature a₂=b₃+b₄+b₅ · incongruence-line slope a₃=b₁−b₂ · incongruence-line curvature a₄=b₃−b₄+b₅
- **The 3-way interaction**: stratify by years-in-operation as moderator — small multiples of surfaces per tenure band are the visual equivalent of the S×A×tenure interaction. Hypothesis: the incongruence penalty is steepest for young complex systems.
- **Rendering**: 3D surface plus contour plot (contours travel better on the web).

### 4.4 Statistical honesty gate

Until data fills in, the surface is a *grammar*, not a *result*:

| Phase | Condition | What is shown |
|-------|-----------|---------------|
| 1 (now) | dimension N < 30 | Measured scatter, quadrants, profile chips only. Any surface carries an "illustrative" watermark |
| 2 | N ≥ 30 | Quadratic fit + contours (descriptive statistics) |
| 3 | N ≥ 100 | Coefficient tests + a₁-a₄ surface tests + confidence regions; drop non-significant higher-order terms (per Edwards) |

Dimension data accrues from v1.2 submissions onward. Prior submitters can resubmit just the `dimensions` block for retroactive inclusion.

## References

- Edwards, J. R., & Parry, M. E. (1993). On the use of polynomial regression equations as an alternative to difference scores in organizational research. *Academy of Management Journal*, 36(6), 1577-1613.
- Edwards, J. R. (2002). Alternatives to difference scores: Polynomial regression analysis and response surface methodology. In F. Drasgow & N. Schmitt (Eds.), *Measuring and analyzing behavior in organizations* (pp. 350-400). Jossey-Bass.
- Box, G. E. P., & Wilson, K. B. (1951). On the experimental attainment of optimum conditions. *Journal of the Royal Statistical Society B*, 13(1), 1-45. (Origin of RSM)
- CMMI Institute. *CMMI for Development* — scale-invariant maturity levels with scoped appraisals.
