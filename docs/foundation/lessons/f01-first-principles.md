# F1 — Enterprise Architecture from first principles

!!! note "Status"
    draft

**Central proposition:** An enterprise can be full of competent people making sound decisions in their own domain, and still have no enterprise architecture at all — because nobody ever evaluates, connects, or verifies those decisions against the whole.

## Lesson purpose

Before introducing TOGAF's vocabulary in F2, establish the gap that Enterprise Architecture exists to close. This is not a story about any one company; the pattern below is common across large organizations regardless of industry, and you have almost certainly seen a version of it.

## Prerequisites

General experience designing, building, or operating IT systems. No TOGAF knowledge assumed.

## Learning objectives

By the end of this lesson you should be able to:

1. Recognize the five recurring symptoms of "no enterprise-level architecture" listed below.
2. State the central proposition in your own words.
3. Name which part of TOGAF each symptom points toward, at a preview level of detail.
4. Explain why domain-level competence does not, by itself, produce enterprise-level architecture.

## Instructional narrative

### Five symptoms, one underlying gap

Picture a large IT organization — thousands of employees, tens of thousands of managed assets, many delivery teams. It has good engineers. Compute sizes its servers competently. Storage sizes its storage competently. Network plans capacity competently. Application teams pick sound designs for their own systems. None of that is the problem.

The problem shows up as a specific, recognizable set of symptoms:

1. **Architecture gets evaluated during or after implementation, not before it.** A design is reviewed once it's already being built, or after — not while it's still a decision that could be changed cheaply.
2. **Nobody verifies that what got built matches what was proposed — and often there was nothing precise enough to check against.** Sometimes a real design is approved and the built system quietly drifts from it with no one checking. Just as often, what got approved was never a concrete design at all — it was an amorphous solution concept, vague enough that "did we build what we approved" isn't even answerable, because there was no defined architecture to hold the build accountable to.
3. **Domains plan independently instead of as one architecture.** Compute does its sizing, storage does its sizing, network does its sizing — each rating its own piece as fine — with no discussion of them as one system serving one enterprise.
4. **Solutions get rated as standalone, not as fits into the enterprise.** A given solution can look sound in isolation — reasonable cost, meets its requirements — while still being redundant with something the organization already has, or incompatible with where the organization is headed.
5. **No group has the job of evaluating architecture or technology centrally.** Every domain and every project is a decision boundary; nothing is evaluated at the level of "the enterprise."

Read those five again. Notice that none of them requires anyone to be incompetent. Compute really can size correctly. The application team really can pick a defensible design. Each of the five is a *missing function*, not a *broken decision*. That is the central proposition in practice: local competence was never the scarce resource. The scarce resource was the function that would evaluate, connect, and verify across domains and over time — and in this picture, that function does not exist anywhere.

### Why this is worth a whole discipline, not just a policy

A natural reaction is "so write a policy requiring cross-domain review." That helps, but a policy without a standing method, a defined governance body, and defined artifacts tends to erode under delivery pressure — it becomes the step people skip when the deadline is real. TOGAF's answer is not a single policy; it is a full method (a sequence of phases that produce and connect business, data, application, and technology architecture before and during implementation, not only after), a governance structure (a defined body with authority to evaluate architecture and technology centrally), and a repository (a place that records what already exists, so a new solution can be checked against it instead of evaluated as if it were the first of its kind).

The rest of this course is essentially a detailed answer to the five symptoms above. As a preview, without yet teaching the formal terms:

| Symptom | What TOGAF provides (covered in later lessons) |
|---|---|
| Evaluated after implementation, not before | A method whose early phases (architecture vision, then business, data, application, and technology architecture) happen before solution design is locked in |
| No verification that built matches proposed | A governance phase dedicated to checking implementation against the approved architecture |
| Domains plan independently | A requirement that business, data, application, and technology architecture be developed as one connected set, not four separate ones |
| Solutions rated as standalone | A phase dedicated to evaluating candidate solutions against the target architecture and against what the organization already has |
| No central evaluation function | A defined governance body with the authority and standing responsibility to evaluate architecture and technology across the enterprise |

You do not need to remember these terms yet. Notice instead that each row is a direct answer to a symptom you can recognize, not an abstract improvement.

## Anchor scenario: Northstar Regional Health

Northstar Regional Health — six hospitals, over a hundred clinics, two data centers, multiple cloud providers — exhibits the same five symptoms. Its infrastructure and application teams are each competent. What Northstar lacks is the connecting function: nothing evaluates a new clinical system against what the six hospitals already run; nothing checks that a newly built integration matches what was proposed; nothing treats storage, network, and application capacity planning as one picture instead of three. Northstar will be the running example used throughout this course to make later, more detailed lessons concrete.

## Guided exercise

Pick one of the five symptoms above and describe a version of it you have personally observed — anonymized, no confidential detail required. For that instance:

- What made the local decision(s) reasonable at the time, from where the deciding team sat?
- What connecting function was missing — evaluation before build, verification after build, cross-domain planning, fit-to-enterprise assessment, or central authority?
- What would have had to exist for that gap to be caught?

## Debrief and model answer

Using symptom 3 (domains planning independently) as the worked example: a new application requires additional compute, storage, and network capacity. Each infrastructure team receives its own request, sizes it correctly for the number stated, and approves it. No one asks whether the application's assumptions matched what the other two domains were told, or whether the combined footprint fits any enterprise-level capacity plan — because no such enterprise-level view exists for anyone to check against. Every local approval was correct. The missing piece was a connecting function that treats the three domains as one architecture rather than three independent approvals.

## Knowledge check

1. The central proposition of this lesson is best restated as:
    - a) Most enterprise architecture failures are caused by incompetent staff.
    - b) An enterprise can have competent domain decisions and still lack enterprise architecture, because nothing connects or verifies those decisions against the whole.
    - c) Enterprise Architecture's main purpose is to centralize every technical decision.
    - d) Domain teams should be replaced by a single architecture team.
2. "Solutions rated as standalone" means:
    - a) A solution is evaluated only against its own requirements and cost, not against what the enterprise already has or where it's headed.
    - b) A solution has no documentation.
    - c) A solution was built without any requirements.
    - d) A solution failed its own acceptance testing.
3. Which symptom is most directly about checking that what was built matches what was approved?
    - a) No central evaluation function
    - b) No verification that built matches proposed
    - c) Domains planning independently
    - d) Solutions rated as standalone

Answers: 1-b, 2-a, 3-b.

## Common misconceptions

- **"These problems mean the domain teams did something wrong."** In every example above, the local decision was reasonable given what the team could see and was accountable for. The gap is a missing connecting function, not a bad decision.
- **"A written policy requiring cross-domain review solves this."** A policy without a standing method, governance authority, and repository tends to be the first thing skipped under delivery pressure.
- **"Enterprise Architecture means one team approves everything."** The goal is a defined function with the authority to evaluate architecture centrally — not the elimination of domain-level decision-making.

## References

This lesson is original explanatory writing. It does not reproduce or paraphrase specific text from The Open Group's TOGAF Standard, and it introduces no TOGAF-specific terminology by design — that begins in F2. General framing is consistent with TOGAF's own stated purpose, published at [opengroup.org/togaf](https://www.opengroup.org/togaf).

## Version notes

- Draft written 2026-07-21. First revision, rebuilt around five concrete, generalizable symptoms in place of a single narrative example.
