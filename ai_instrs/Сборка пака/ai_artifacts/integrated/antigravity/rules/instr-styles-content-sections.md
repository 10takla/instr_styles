---
name: "instr-styles-content-sections"
description: "Defines content types, section kinds, and input/output compositions. Apply when formatting instruction sections."
trigger: "model_decision"
---

**Related rules:**
- [instr-styles:style-context](rule;instr-styles:style-context)

## Content types

**Inputs:**

- `var` — the content of one element.

### `Text`

**Format:**

```md
`<var>`
```

### `List`

**Format:**

```md
- `<var>`
...
```

Use only an unordered bulleted list.

### `TextOrList`

Use either one `Text` block or a `List`.

## Sections

Form a section from a name and content. Determine its purpose and permitted content type from the section kind.

**Formats:**

```md
**<sectionName>:** <Text>
```

or

```md
**<sectionName>:**
<List>
```

Form section content according to the specified types.

### Section kinds

- **“Inputs”** — `List`, where each item has the format `` `<input name>` — <input description> ``. List values, files, links, and additional context that the calling instruction or operator explicitly passes on every invocation. Do not include the instruction content’s internal arguments. Interpret and, when needed, transform a passed value according to the argument description.
- **“Task”** — `Text`. Briefly describe the required action or transformation.
- **“Instructions”** — `TextOrList`. Describe a sequence of actions addressed to the agent for performing the task in the current context. Order the actions by dependency: each subsequent action assumes that the necessary preceding actions have been completed or that the state they require is available.
- **“Algorithm”** — `List`. Describe a sequence of logical operations independent of a particular executor that transforms the input state into the result. Order the items by the execution order of the operations.
- **“Requirements”** — `List`. List the mandatory properties of the actions being performed or their result.
- **“Output format”** — `TextOrList`. Define the structure and presentation of the agent's response.
- **“Result”** — `TextOrList`. Describe the expected state after completing the task or stage.
- **“Outputs”** — `List`. List the specific values, files, or artifacts to create, provide, or save, including where to save them.

## Input/output composition

**Inputs:**

- `otherSections` — other sections.

**Format:**

```md
<Section "Inputs">

`<otherSections>`

<Section "Outputs">
```

Examples:

- For a composition with instructions, pass the “Instructions” section to `otherSections`.
- For a composition with an algorithm, pass the “Algorithm” section to `otherSections`.
