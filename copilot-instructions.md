---
description: "General documentation preferences for agents updating markdown documentation files."
applyTo: "**/*.md"
---

# Documentation Guidelines

- Write command examples as single-line commands. Convert existing multi-line commands to single-line when editing.
  - Exception: Commands that are syntactically impossible to express on a single line, specifically heredocs and other constructs where a newline is part of the syntax (not just a readability choice).
- All markdown tables in markdown documentation files must be aligned for readability.
  - Use pipes and spaces so columns line up visually.
- Example of a documentation aligned table:

| Name  | Port |
|-------|------|
| http  | 80   |
| https | 443  |
