# Resume data

Raw numbers behind figures quoted in `../resume.json`.

- `clarity-weekly-commits.csv`: weekly commit counts at Clarity Pediatrics, weeks of 2024-10-13 to 2026-10-11.
- `clarity-weekly-additions.csv`: weekly lines added, same period.

## Derived figures

Before = weeks of 2025-01-05 to 2026-01-25 (56 weeks). After = weeks of 2026-02-01 onward (37 weeks, through 2026-10-11). The shift starts the week of 2026-02-01; January 2026 looks like 2025.

| Metric | Before | After | Change |
|---|---|---|---|
| Commits per week (mean) | 3.8 | 9.9 | 2.6x |
| Lines added per week (median) | ~350 | ~3,200 | ~9x |

Use the median for lines added. The week of 2025-02-09 has 74,008 additions (likely generated or vendored code) and skews the mean. Commits is the safer claim; lines added rewards verbose AI output.

Interview counts come from the Obsidian note "Interviews up to this point" (18 recorded for 2026 as of 2026-10-16).
