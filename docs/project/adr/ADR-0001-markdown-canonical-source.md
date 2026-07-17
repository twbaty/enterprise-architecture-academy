# ADR-0001: Markdown is the canonical source

**Status:** Accepted

## Context

Maintaining Word documents, PDFs, and website pages independently causes divergence and makes it unclear which version is authoritative.

## Decision

Markdown stored in the Git repository is the authoritative source for project documentation and curriculum content.

PDF, DOCX, website, and presentation formats are generated or released outputs.

## Consequences

- Changes can be reviewed line by line.
- Version history remains visible.
- Multiple output formats can be generated consistently.
- Existing DOCX material must be migrated or explicitly archived.
