---
name: "instr-styles-content-sections"
description: ""
---

**Related rules:**
- /instr-styles-style-context

## Section Format and Data Types

Format instruction sections as a bold heading followed by a colon:
```md
**<Section Name>:** <Content>
```

### Basic Content Types

- **`Descr` (description):** a plain text block or a single line without list markers.
- **`List` (list):** a bulleted list of items (`- <item>`).
- **`Puncts` (points):** a single point in `Descr` format or a group of points in `List` format.

## Standard Sections

### 1. Inputs
Contains initial arguments, parameters, and information necessary to perform the task.
**Format:**
```md
**Inputs:**
- `argument` — argument description
```

### 2. Outputs
Contains specific target artifacts, created files, or result saving paths (unlike the output format, fixes an actual artifact in the file system).
**Format:**
```md
**Outputs:**
- `path/to/file` — artifact description
```

### 3. "Input/Output" Composition
Use for stages with explicit transformation of input data into a result:
```md
**Inputs:**
- `<argument> — <description>`

<Instructions | Algorithm | Requirements>

**Outputs:**
- `<artifact> — <description>`
```

### 4. Instructions
Contains direct directives and instructions to the agent for action. Content type — `Puncts`.
**Format:**
```md
**Instructions:**
- <Action directive>
- <Action directive>
```

### 5. Algorithm
Contains a step-by-step sequence of actions for task execution. Content type — `Puncts`.
**Format:**
```md
**Algorithm:**
- <Step 1>
- <Step 2>
```

### 6. Task
Concisely formulates a specific action or stage goal. Content type — `Descr`.
**Format:**
```md
**Task:** <task text>
```

### 7. Requirements
Specifies technical constraints, rules, and execution criteria. Content type — `List`.
**Format:**
```md
**Requirements:**
- <Requirement 1>
- <Requirement 2>
```

### 8. Output Format
Describes the structure and format of the expected agent response (message, JSON, etc.). Content type — `List`.
**Format:**
```md
**Output Format:**
- <Description of response structure>
```

## Section Formatting Workflow

1. Determine the sections necessary for the stage (all sections are optional, include only those needed for the context).
2. When input parameters and saved files are present, use the "Input/Output" template.
3. To describe steps, choose "Instructions" (a set of direct directives), "Algorithm" (a sequence of actions), or a concise "Task".
4. Add "Requirements" and "Output Format" sections if special constraints or expectations regarding response format exist.
5. Follow the `**<Name>:**` syntax and corresponding data type (`Descr`, `List`, or `Puncts`).
