---
description: "General documentation preferences for agents updating markdown documentation files."
applyTo: "**/*.md"
---

# Documentation Guidelines

- All new entries must follow the structure defined in `entry_template.md`. If `entry_template.md` is not accessible, stop and notify the user rather than proceeding with an assumed structure.
- Do not add sections that are not in `entry_template.md`.
- Keep descriptions and explanations concise and technical. Do not add commentary, context, or background to documentation entries that wasn't requested. Explanatory labels in templates or guidelines are exempt from this rule.
- Commands in code blocks must be copy-pasteable. Do not annotate commands inline.
- Write command examples as single-line commands. Convert existing multi-line commands to single-line when editing.
  - Exception: Commands that are syntactically impossible to express on a single line, specifically heredocs and other constructs where a newline is part of the syntax (not just a readability choice).
- All markdown tables in markdown documentation files must be aligned for readability.
  - Use pipes and spaces so columns line up visually.
- Example of a documentation aligned table:

| Name  | Port |
|-------|------|
| http  | 80   |
| https | 443  |
