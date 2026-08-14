# Palette UX Journal

A journal to record critical UX and accessibility learnings from optimizing
interfaces and user experiences.

## 2026-08-09 - Accessibility and Readability Standards in Profile READMEs

**Learning:** Profile READMEs are highly visual entryways. Unwrapped emojis can
confuse screen readers, and unstructured tech badge listings decrease horizontal
scannability. Wrapping emojis in semantic tags, laying tech badges out
horizontally under strict 80-character line limit, and providing clear "Back to
Top" navigation controls significantly improves usability and accessibility.

**Action:** Wrap all emojis with `<span role="img" aria-label="...">`, align
badges horizontally using short referenced links, limit line lengths to 80
characters, and place top-scrolling anchors on the main heading.

## 2026-08-09 - Keyboard-Accessible Disclosure Patterns using Native HTML

**Learning:** When displaying non-essential detailed profile sections (such as
workspace configurations or philosophies), overloading a single page can cause
visual fatigue. Utilizing native `<details>` and `<summary>` disclosure widgets
provides interactive collapsible controls. These are fully keyboard-navigable
(tab and space/enter to toggle) and accessible to screen readers out-of-the-box
without custom CSS or Javascript.

**Action:** Employ native HTML `<details>` and `<summary>` elements to create
accessible, interactive accordions that structure page content while
maintaining strong readability.

## 2026-08-09 - Power User Keyboard Shortcut Styling and Discovery

**Learning:** Adding contextual keyboard shortcut tips using standard, semantic
`<kbd>` HTML elements significantly enhances UX for power users of modern web
platforms like GitHub. This improves discovery of platform-native keyboard
shortcuts, encourages efficient platform navigation, and renders beautifully and
accessibly across modern screen readers and markdown renderers.

**Action:** Integrate keyboard shortcut callouts utilizing standard `<kbd>` HTML
tags within user profiles, ensuring instructions are short and aligned with
platform-native interactions.
