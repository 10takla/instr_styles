---
name: "instr-styles-execution"
description: "Presents task execution as a sequence of actions. Use for step-by-step instructions addressed to an agent."
---

**Related rules:**
- /instr-styles-style-context
- /instr-styles-stages
- /instr-styles-content-sections

Express task execution as a sequence of actions addressed to the agent.

Prefer the following sections and preserve their relative order when they are used:

```md
<Section "Inputs">

<Section "Instructions">

<Section "Requirements">

<Section "Outputs">
```
