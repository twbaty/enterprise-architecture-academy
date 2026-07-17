# Content and style guide

## Voice

Write in a professional, direct, instructional voice. Explain concepts completely without inflating simple points.

Avoid promotional language, artificial enthusiasm, and unsupported claims.

## Headings

Use sentence case for headings.

```markdown
## Architecture as decision support
```

Do not capitalize every major word unless it is an official title.

## Terminology

Use official TOGAF terminology when discussing formal TOGAF concepts. Distinguish formal framework usage from common industry usage when they differ.

Use **Enterprise Architecture** when naming the discipline or program. Lowercase may be used in ordinary descriptive phrases when capitalization would imply a formal name.

Define specialized terms before relying on them.

## Lesson structure

Each complete lesson should contain, where applicable:

1. purpose;
2. authoritative alignment;
3. prerequisites;
4. learning objectives;
5. instructional narrative;
6. persistent scenario application;
7. exercises;
8. debrief or model answer;
9. knowledge check;
10. common misconceptions;
11. references;
12. revision notes.

## Examples and scenarios

Prefer realistic fictional examples. Never include confidential employer, customer, patient, security, or operational information.

Use the Northstar Regional Health scenario when continuity improves learning. Use government and commercial variants when sector comparison adds value.

## Sources and citations

Prefer official and primary sources. Paraphrase rather than reproducing substantial source text.

Citations must identify enough information for a reader to locate the source. Certification-related claims must be checked against current official Open Group material before release.

## Examination integrity

Do not include recalled, reconstructed, solicited, or confidential examination questions. Practice questions must be original and derived from published objectives and concepts.

## Markdown

- Use fenced code blocks with a language identifier where applicable.
- Use tables only when comparison benefits from tabular structure.
- Use admonitions for warnings, notes, examples, and status information.
- Keep links descriptive; avoid link text such as “click here.”
- Prefer Mermaid for diagrams that can be represented clearly in text.

## File naming

Use lowercase kebab-case:

```text
architecture-decision-support.md
```

ADRs retain their numbered uppercase prefix:

```text
ADR-0001-markdown-canonical-source.md
```

## Status language

Use explicit status labels:

- proposed;
- accepted;
- superseded;
- deprecated;
- draft;
- review-ready;
- published.
