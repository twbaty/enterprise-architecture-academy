# Project governance

## Governance model

Enterprise Architecture Academy uses open contribution with controlled acceptance.

Anyone may propose a change. The repository owner retains final editorial authority and controls what is merged into the published branch.

## Roles

### Repository owner

The repository owner:

- sets project direction;
- approves or rejects proposed content;
- controls curriculum scope and sequence;
- resolves editorial conflicts;
- approves releases;
- may delegate review without delegating final authority.

### Contributors

Contributors may:

- open issues;
- propose corrections or additions;
- submit pull requests;
- participate in review discussions;
- provide technical or instructional review.

Contribution does not guarantee acceptance or publication.

### Reviewers

Reviewers evaluate factual accuracy, instructional quality, source use, terminology, confidentiality, copyright, and curriculum fit. Reviewer approval informs the owner but does not replace owner approval.

## Branch and publication policy

- `main` is the published source branch.
- Work is performed on topic or feature branches.
- All substantive changes reach `main` through pull requests.
- A successful strict MkDocs build is required before merge.
- Code Owner approval is required before merge.
- Merging to `main` triggers site publication.

A separate integration branch may be introduced later if release volume justifies it. It is not required for the current project stage.

## Acceptance criteria

A contribution may be accepted when it:

- supports the program charter and roadmap;
- improves accuracy, clarity, usefulness, or coverage;
- uses authoritative sources appropriately;
- follows the project style and content templates;
- preserves examination integrity;
- contains no confidential or personally identifiable information;
- does not reproduce protected material beyond permitted quotation or citation;
- passes automated validation.

A technically correct contribution may still be rejected when it duplicates existing material, disrupts instructional sequence, exceeds the intended scope, or conflicts with the editorial direction.

## Decision records

Major structural, publishing, licensing, scenario, and curriculum decisions are recorded as Architecture Decision Records under `docs/project/adr/`.

## Releases

The project uses semantic-style release numbers:

- patch releases correct or clarify existing material;
- minor releases add meaningful curriculum content or capability;
- version 1.0 represents the first complete public Foundation and Practitioner study path as defined by the roadmap.
