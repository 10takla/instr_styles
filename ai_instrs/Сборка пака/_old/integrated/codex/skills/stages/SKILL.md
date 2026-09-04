---
name: "stages"
description: ""
---

**Related rules:**
- $instr-styles:style-context

## Stage Organization

### Stage Separation

- **Homogeneous stages:** separate sequential stages of the same type or semantic group with empty lines:
  ```md
  <##> <Stage 1>

  <##> <Stage 2>
  ```
- **Heterogeneous stages:** separate stages of different types or fundamentally distinct activities with a horizontal rule `---`:
  ```md
  <##> <Stage of one type>

  ---
  <##> <Stage of another type>
  ```

### Substage Formatting

- Form a substage by lowering the heading level relative to the parent stage:
  ```md
  <##> <Stage>

  <###> <Substage>
  ```

### Stage Structure

- Format each stage with a Markdown heading followed by a content block:
  ```md
  <##> <Stage Name>

  <Content>
  ```
- Formulate the stage name concisely and reflect the essence of the task being solved.
- Form `<Content>` in accordance with models from $instr-styles:content-models and sections from $instr-styles:content-sections.

## Stage Formation Workflow

1. Break the overall workflow into sequential logical steps.
2. Group stages by activity type: leave blank lines between homogeneous stages, and place a horizontal rule `---` before transitioning to another activity type.
3. If decomposition is needed, extract substages with lower-level headings (<###>).
4. Fill the body of each stage according to $instr-styles:content-models and $instr-styles:content-sections.
