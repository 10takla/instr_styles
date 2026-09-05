## Style Application Principles

- Apply the described styles as soft rules for organizing instructions.
- Account for style with an approximate weight of 20–30% relative to direct task requirements and already accepted decisions.
- Give unconditional priority to user edits when they diverge from style; minimize style influence in such cases.
- Treat all structural elements of styles as optional. Include only those elements necessary to convey the meaning of the specific task.
- Interpret format descriptions declaratively: reproduce the intended meaning and structure, avoiding blind literal copying of templates.
- Distinguish between explanatory text and ` ```md ` blocks: explanatory text formulates rules and format semantics, while code blocks demonstrate markup or examples.

## Template Notation

When interpreting templates and format schemes, follow these rules:

- **Variables and Substitution:**
  - `var` — name of a variable or template parameter;
  - `<var>` — interpolation (substitution) of the computed variable value into the template.
- **Quantifiers:**
  - `...` — metasymbol for repeating the preceding element one or more times;
  - Never output the auxiliary symbol `...` literally into resulting documents.
- **Headings:**
  - `<##>` — Markdown heading of the required nesting level (`#`, `##`, `###`, etc.) depending on placement context.
- **Template Composition:**
  - `[](#anchor)` or `[](<path>)` — invocation, reference, or inclusion of the specified template structure;
  - `, where: var = <value>` — passing an argument to a parameter of the included template.

## Instruction Format Workflow

1. Determine the composition and hierarchy of task stages according to @draft(stages).
2. Choose the appropriate stage content model (simple or structured) according to @draft(content-models).
3. Format sections of each stage and transferred data types according to @draft(content-sections).
4. Verify the final document for absence of auxiliary notation metasymbols and adherence to user requirement priority.
