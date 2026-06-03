---
name: feedback_verify_imports_used
description: Always verify that imported assets/components are actually referenced in the template, not just imported in the frontmatter
metadata:
  type: feedback
---

When creating or editing Astro (or any component) files, always verify that every import in the frontmatter is actually used in the template markup below it. I once imported `joshBakerKickVariation` in Tracks.astro but forgot to add the `<Image>` tag in the template.

**Why:** Easy to miss — imports don't throw errors if unused, so the bug is silent.

**How to apply:** Before finishing a file, do a quick scan: every import should appear at least once in the template.
