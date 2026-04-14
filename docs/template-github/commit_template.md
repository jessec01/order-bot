# Commit Template (Conventional Commits)

Use this structural format to organize your `git commits`. You can copy these templates, replace the description translating from Spanish to **ENGLISH**, and integrate it.

## Base Structure

`<type>(<optional scope>): <description english>`

`<optional detailed body, if the commit is complex>`

### Commit Types:

- `feat:` -> New functionality (Feature)
- `fix:` -> Bug/error fix
- `docs:` -> Changes in documentation or comments
- `refactor:` -> Structural improvement of existing code without changing function
- `chore:` -> Maintenance or dependency adjustments

---

## Ready-to-copy templates (Translate your intention to English)

### 1. Template for a FIX (Bug Reports Fixed)

```text
fix(bot-logic): resolve issue with [insert what was failing in English]

- Fixed handling of [insertar qué se arregló]
- Prevented crash when [insertar condición del error]
- Resolves issue #[numero-del-issue]
```

_(Example of use: "fix(bot-logic): resolve issue with empty messages crashing bot")_

### 2. Template for a FEATURE (New Feature)

```text
feat(menu): implement [insert new feature in English]

- Added state code for [new feature]
- Integrated logic into index.js
- Fixes #[issue-number]
```

### 3. Template for a REFACTOR (Improvements/Cleanup)

```text
refactor(state-machine): improve efficiency of [insert module]

- Extracted complex functions to simplify readability
- Removed deprecated code blocks replacing variables
```

### 4. Template for DOCS (Documentation)

```text
docs(readme): add instructions for [insertar tema]

- Added setup guidelines for developers
- Included example environment variables
```
