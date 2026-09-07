---
name: "style-context"
description: "Defines shared rules for styles and content models. Apply when creating or revising instructions."
---

Use styles as soft rules for organizing instruction content.

Interpret technical format descriptions declaratively: recover the meaning they express instead of limiting yourself to literal reproduction of templates. Clearly distinguish explanatory text from the contents of `md` code blocks: explanatory text describes a format, while a block shows the format itself or an example of it.

## Applying styles

- When choosing a structure, treat the style as a soft preference with an approximate weight of 20–30% relative to the task requirements and the decision already made.
- When a user-edited version conflicts with the style, prioritize the user-edited version and apply the style only minimally.
- Follow the common structure of an instruction, a stage, and a content model.
- Apply the rules for stages, content, and styles consistently.

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
