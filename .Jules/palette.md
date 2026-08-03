# Palette UX Journal

This journal records critical UX and accessibility learnings from working on
the Abokaes/Abokaes GitHub Profile README user interface.

## 2026-07-30 - Accessible Interactive Emojis and Structured Navigation

**Learning:** When developing profile READMEs as visually appealing hubs,
including decorative or structural emojis can overwhelm screen reader users with
non-semantic text-to-speech feedback unless properly wrapped. Wrapping every
single emoji in `<span role="img" aria-label="...">` tags guarantees standard-
compliant spoken descriptions. Additionally, utilizing functional "Back to Top"
anchors combined with horizontal layout structures avoids scroll fatigue and
improves keyboard scanability. Disabling MD033 is necessary to allow these raw
accessible inline HTML patterns to pass modern linter pipelines.

**Action:** Consistently annotate emojis with role and aria-label attributes in
Markdown layouts. Place an HTML target id inside the top H1 heading to support
smooth keyboard navigation shortcuts without violating MD041, and selectively
disable MD033 when verifying.

## 2026-08-01 - Reference Links for Tech Stack Badges and Circular Prevention

**Learning:** Long URL parameters on shield.io badges in a profile README can
easily cause Markdown files to violate strict 80-character line limits. Moving
badge source definitions to reference-style link blocks at the bottom of the
file keeps layout markup concise, readable, and perfectly compliant with
structural linter limits. Furthermore, eliminating circular navigation targets
(like links back to the user's profile index) and replacing them with direct,
actionable links to external pages (e.g., repository feedback/issue trackers)
removes cognitive loops for assistive technology users.

**Action:** Move all long badge definitions and target links to reference-style
link definitions at the bottom of the Markdown document. Ensure no links cycle
back to the profile page itself, substituting them with external contact or
feedback mechanisms instead.
