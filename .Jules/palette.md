# Palette UX Journal

A journal to record critical UX and accessibility learnings from optimizing
interfaces and user experiences.

## 2026-07-02 - Avoiding Placeholders in Profile READMEs

**Learning:** In GitHub Profile READMEs, uncommenting template placeholders like
`[Project Name]` or `...` can lead to an 'unfinished' UI look if the user
doesn't immediately fill them in. A better UX approach is to provide generic
but professional text that serves as a functional starting point.

**Action:** Always replace bracketed placeholders with professional, complete
sentences or remove them entirely when populating templates for users.

## 2026-08-09 - Avoiding Redundant Circular Profile Links via Quick Actions

**Learning:** In GitHub Profile READMEs, linking back to the profile page
itself (e.g., `https://github.com/username`) creates an annoying circular
redirect that frustrates users. A better UX pattern is to provide explicit,
high-engagement external paths (like `/stargazers`, `?tab=repositories`, or
`/issues`) via an interactive "Quick Actions" panel, keeping user exploration
purposeful and highly interactive.

**Action:** Replace self-referencing links with useful repository action
routes or clear contact channels, and wrap list items cleanly under the 80-
character line length limit.
