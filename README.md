# Enterprise Architecture Academy

A living, community-contributed body of curriculum and study material for Enterprise Architecture and the TOGAF Enterprise Architecture certification path.

This repository documents the material, exercises, references, and methods used to study Enterprise Architecture. It is designed for experienced technology professionals moving into architecture.

> This is an independent educational project. It is not official training from The Open Group, is not endorsed by The Open Group, and does not contain recalled certification examination questions.

## Published documentation

The MkDocs site is published automatically through GitHub Actions after an approved pull request is merged into `main`.

## Contribution model

Anyone may propose improvements through an issue or pull request. The repository owner retains editorial authority and must approve changes before they are merged.

See [CONTRIBUTING.md](CONTRIBUTING.md) and [Editorial Governance](docs/project/editorial-governance.md).

## Local preview

```powershell
py -m venv .venv
.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
mkdocs serve
```

Open the local address shown by MkDocs, normally `http://127.0.0.1:8000`.
