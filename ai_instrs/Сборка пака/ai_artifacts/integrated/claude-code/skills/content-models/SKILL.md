---
name: "content-models"
description: ""
disable-model-invocation: true
---

**Related rules:**
- /instr-styles:style-context

## Content Models

Use one of two stage content organization models depending on verification and structure requirements.

### Simple Model

Apply to compact stages or tasks without a separate independent acceptance procedure for results.

**Format:**
```md
[Preface — reflection of the goal, intent, or concept of the stage]

<Sections>
```

- In the preface, concisely convey the intent or goal of the stage.
- In the `<Sections>` block, place inputs, algorithm, instructions, or outputs according to /instr-styles:content-sections.

### Structured Model

Apply to stages with independent verification and a clear separation between execution and verification.

**Format:**
```md
[Preface — context, goal, intent, or expected stage result without prompting the agent to act]

### Implementation Instructions

<Sections>

### Verification

[Actions confirming compliance of the stage result with the goal or expected state from the preface. Verify the stage result, not the fact of instruction execution by the agent.]
```

- **Preface:** describes context, intent, and expected target state. Do not use imperative directives in the preface.
- **Implementation Instructions:** contains concrete steps, rules, and action sections formatted according to /instr-styles:content-sections.
- **Verification:** contains actions and acceptance criteria for the final result relative to the goal from the preface.

## Model Selection and Application Workflow

1. Assess the stage nature: if strict artifact validation and independent verification are required, choose the structured model; for other cases, use the simple model.
2. Formulate the preface: capture the goal or expected state without imperative commands.
3. Format the execution part: apply sections from /instr-styles:content-sections. In the structured model, place them under the `### Implementation Instructions` heading.
4. For the structured model, add the `### Verification` block and describe the criteria for verifying the stage result.
