---
name: "implementation-with-verification"
description: "Separates implementation instructions from verification. Use for implementation tasks that require result verification."
disable-model-invocation: true
---

**Related rules:**
- /instr-styles:style-context
- /instr-styles:stages
- /instr-styles:content-sections

Separate the stage context from implementation and result verification.

**Required structural parts:**

- “Implementation Instructions” contains the actions addressed to the agent that are necessary to produce the stage result.
- “Verification” contains actions that confirm the stage result matches the specified goal or expected state.

**Format:**

```md
<Preface>

<###> Implementation Instructions

<Sections>

<###> Verification

[Actions that confirm the stage result matches the goal or expected state specified in the stage content. Verify the stage result, not whether the agent followed the implementation instructions.]
```
