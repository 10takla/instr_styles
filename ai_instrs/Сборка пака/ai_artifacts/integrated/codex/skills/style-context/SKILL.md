---
name: "style-context"
description: "Defines shared rules for styles, notation, and content models. Apply when creating or revising instructions."
---

Use styles as soft rules for organizing instruction content.

Interpret technical format descriptions declaratively: recover the meaning they express instead of limiting yourself to literal reproduction of templates. Clearly distinguish explanatory text from the contents of `md` code blocks: explanatory text describes a format, while a block shows the format itself or an example of it.

## Applying styles

- When choosing a structure, treat the style as a soft preference with an approximate weight of 20–30% relative to the task requirements and the decision already made.
- When a user-edited version conflicts with the style, prioritize the user-edited version and apply the style only minimally.
- Follow the common structure of an instruction, a stage, and a content model.
- Apply the rules for notation, stages, content, and styles consistently.

## Notation

### Interpolation

- Interpret `<expression>` as the interpolation of the value, structure, or content defined by the expression.
- Determine how to interpolate an expression from its content and the format context.
- Do not output angle brackets literally.
- Treat `var` as the name of a variable or parameter.
- Interpret `` `<var>` `` as the interpolation of the value of `var`; do not include the backticks in the result.

Examples:

- `<###>` — insert a Markdown heading at the required nesting level: `#`, `##`, `###`, and so on.
- `<Section "Inputs">` — insert a section with the specified name.

### Descriptive text

- Interpret `[description]` as a placeholder for free-form text generated according to the description.
- Do not output square brackets literally.

### Quantifiers and repetition

- Interpret `...` as one or more repetitions of the preceding element.
- Do not output `...` literally in the resulting document.

### Passing parameters

Interpret `, where: var = <value>` as passing a value to the `var` parameter of the interpolated structure.

## Stage content

Form stage content from content elements within the framework of the selected model. Treat the sections required for the specific instruction and unsectioned text as content elements.

### Optional elements

Treat content elements as optional unless they are explicitly required or necessary to preserve the purpose of the model. Treat a format as a description of the position and relationships of an optional element, not as a requirement to use that element. Do not create empty elements in place of omitted ones.

### Text

Treat content without its own heading and not formatted as a section as text.

### Preface

Use a preface to convey the context, goal, meaning, or expected result of a stage without prompting the agent to take action.

### Content models

Treat each model as an independent way to organize stage content. Treat models as alternative structures rather than consecutive parts of one structure. Apply the model explicitly selected by the operator. Do not combine models or choose between them automatically without an explicit requirement.
