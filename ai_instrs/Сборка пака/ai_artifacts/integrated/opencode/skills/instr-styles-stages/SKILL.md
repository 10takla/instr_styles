---
name: "instr-styles-stages"
description: "Defines the structure, placement, and naming of stages and substages. Apply when dividing an instruction into stages."
---

**Related rules:**
- /instr-styles-style-context

An instruction consists of one or more stages.

## Separating stages

Treat stages as distinct when they differ in goal, task, or substance.

**Formats:**

- Stages of the same type:
    ```md
    <Stage>

    <Stage>
    ```
- Stages of different types:
    ```md
    <Stage>


    ---
    <Stage of another type>
    ```

## Substage

**Format:**

```md
<##> <Stage>

<###> <Substage>
```

## Stage

**Format:**

```md
<##> <Stage name>

<Content>
```

Where:

- `<Stage name>` — a concise noun phrase describing the process being performed or the result being produced, such as “Data collection,” “Results analysis,” or “Report generation.” Do not use names such as “Stage 1” when the stage can be named by its meaning.
- `<Content>` — stage content formed from the required elements within the framework of the selected model.
