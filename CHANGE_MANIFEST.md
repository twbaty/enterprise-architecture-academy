# Change manifest

## Consolidated

- Merged useful content from `README.md` and `README (2).md` into one root `README.md`.
- Moved the useful top-level `project/` concepts into the published `docs/project/` structure.
- Consolidated project philosophy, governance, style, and roadmap information without discarding the stronger content from either copy.

## Added

- `docs/project/project-philosophy.md`
- `docs/project/governance.md`
- `docs/project/style-guide.md`
- `docs/project/adr/index.md`
- ADR-0001 through ADR-0005
- a detailed versioned roadmap with exit criteria
- explicit preservation and migration principles

## Updated

- root `README.md`
- `docs/project/guiding-principles.md`
- `docs/project/roadmap.md`
- `.github/CODEOWNERS` to use `@twbaty`
- `mkdocs.yml` navigation
- `REPOSITORY_MANIFEST.txt`

## Removed

- duplicate `README (2).md` after merging its useful content
- misplaced top-level `project/` directory after migrating its useful content to `docs/project/`

## Not changed

- Existing Foundation, Practitioner, case-study, template, workflow, contribution, and license files were retained.
- The `.git` directory is not included in the returned ZIP. Copy the package contents into the existing local repository rather than replacing the repository folder itself.
