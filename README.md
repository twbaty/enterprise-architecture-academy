# Enterprise Architecture Academy

Enterprise Architecture Academy is a living, community-contributed curriculum for experienced technology professionals moving into Enterprise Architecture.

## Mission

Build a rigorous, practical, and maintainable Enterprise Architecture curriculum while preserving a single editorial vision.

## Goals

- Teach Enterprise Architecture, not merely TOGAF terminology.
- Prepare learners for the TOGAF Enterprise Architecture Foundation and Practitioner certification path.
- Develop practical architectural judgment through persistent scenarios, exercises, and decisions.
- Produce reusable instructor and learner material.
- Keep canonical source material in Markdown under version control.
- Generate the website and future PDF or DOCX releases from the same source.

> This is an independent educational project. It is not official training from The Open Group, is not endorsed by The Open Group, and does not contain recalled certification examination questions.

## Guiding principles

1. Teach the problem before the framework.
2. Architecture supports decisions.
3. Certification is a milestone, not the destination.
4. Examples must be realistic, persistent, and reusable.
5. Reality outranks the model.
6. Governance must enable delivery.
7. Anyone may contribute; the repository owner retains final editorial authority.
8. Markdown in this repository is the canonical source.

## Published documentation

The MkDocs site is built and published automatically through GitHub Actions after accepted changes are merged into `main`.

## Repository structure

- `docs/project/` — charter, philosophy, governance, decisions, standards, and roadmap
- `docs/foundation/` — Foundation curriculum and lessons
- `docs/practitioner/` — Practitioner curriculum and scenarios
- `docs/case-studies/` — recurring enterprise scenarios
- `docs/templates/` — reusable authoring templates
- `.github/` — contribution controls and automated workflows

## Contribution model

Anyone may propose improvements through an issue or pull request. The repository owner must approve accepted changes before they are merged and published.

See [CONTRIBUTING.md](CONTRIBUTING.md), [Project Governance](docs/project/governance.md), and [Editorial Governance](docs/project/editorial-governance.md).

## Local preview

```powershell
py -m venv .venv
.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
mkdocs serve
```

Open the local address shown by MkDocs, normally `http://127.0.0.1:8000`.
