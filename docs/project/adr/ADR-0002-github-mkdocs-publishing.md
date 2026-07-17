# ADR-0002: GitHub and MkDocs form the publishing platform

**Status:** Accepted

## Context

The project requires version control, public access, contribution workflows, automated validation, and wiki-like navigation.

## Decision

GitHub stores and governs the source. MkDocs Material renders the public documentation site. GitHub Actions validates and publishes accepted changes.

## Consequences

- Pull requests become the standard change mechanism.
- The public site reflects the accepted `main` branch.
- Navigation is controlled through `mkdocs.yml`.
- Contributors can work using ordinary Git and Markdown tools.
