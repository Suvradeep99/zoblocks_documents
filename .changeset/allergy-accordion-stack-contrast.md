---
"@zoblocks/react": patch
---

Fixed three WCAG AA color-contrast failures the a11y audit flagged. `AllergyChip`'s refuted/entered-in-error verification affix and its past-reaction text were rendered inside the inactive state's 0.75-opacity dimming on top of an already-muted color, dropping under 4.5:1 — both now use the full-strength text color for that state so the opacity alone carries the "quieter" signal. `ChartAccordion`'s count/time badge used the same low-contrast token on a tinted background as a prior `care-timeline` fix and is now switched to the same safer one. `RecentPatientStack`'s avatar initials, drawn in the full-strength accent over a 16%-opacity tint of that hue, cleared 4.5:1 for only one of its eight accents in light theme; initials now use a darkened variant of the accent in light theme only, verified to hold 4.5:1+ across all eight (dark and high-contrast already passed undarkened).
