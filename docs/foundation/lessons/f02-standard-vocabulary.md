# F2 — The TOGAF Standard: structure, concepts, and vocabulary

!!! note "Status"
    draft

## Lesson purpose

F1 established why the discipline exists. This lesson gives you the map of the TOGAF Standard itself and the core vocabulary every later lesson relies on.

## Prerequisites

F1.

## Learning objectives

By the end of this lesson you should be able to:

1. Name TOGAF's major structural parts and what each is for.
2. Define *enterprise*, *architecture*, and *enterprise architecture* in TOGAF's sense of each term.
3. Distinguish an Architecture Building Block from a Solution Building Block.
4. Explain baseline architecture, target architecture, and gap.
5. Explain stakeholder, concern, viewpoint, and view as one connected chain.
6. Name the four architecture domains.

## Instructional narrative

### What TOGAF is

TOGAF is a framework for developing, governing, and maintaining architecture at enterprise scope, published by The Open Group. Adoption is voluntary, and most organizations that adopt it tailor it rather than run it exactly as published. It doesn't tell you what your architecture should be — it gives you a method and a shared vocabulary for building, describing, governing, and evolving whatever architecture your enterprise needs.

Full definitions for every bolded term below are in the [Glossary](../../glossary.md).

### The standard, in five pieces

TOGAF breaks into five parts. Each gets a full lesson later — this is just so you know where you are when a later lesson refers back to one of these by name.

- The **Architecture Development Method (ADM)** is the core: a repeatable cycle of phases from vision through implementation and change. F3 walks the whole cycle; the lessons after that take one phase each.
- **ADM Guidelines and Techniques** are the working techniques used inside those phases — setting principles, running stakeholder analysis, doing gap analysis. No separate lesson; they show up inside the phase that uses them.
- The **Architecture Content Framework** (lesson 12) is TOGAF's standard shape for architecture output — what artifacts and deliverables a phase should produce.
- The **Enterprise Continuum and Architecture Repository** (also lesson 12) is where that output lives and how it's classified, from generic industry patterns down to your organization's own implementations.
- The **Architecture Capability Framework** (lesson 13) is how you actually run this as a function inside an organization — governance, roles, skills.

### The vocabulary you need right now

An **enterprise**, in TOGAF's sense, isn't necessarily the whole company — it's whatever set of organizations shares a common goal. Sometimes that's the whole corporation. Sometimes it's one division, or a handful of departments running one initiative together.

TOGAF uses **architecture** two ways: sometimes it means a formal, implementation-ready description of a system; sometimes it means the underlying structure and design principles behind one. Watch which sense is in play — TOGAF's own text switches without flagging it.

The work itself splits into four **domains**, shorthanded BDAT: Business, Data, Application, Technology. Remember symptom 3 from F1 — compute sizing, storage sizing, network sizing, each run independently with no shared picture? BDAT is TOGAF's answer: these four are supposed to be developed as one architecture, not four.

Every architecture effort compares two states and names the difference: a **baseline** (what exists now), a **target** (what you're building toward), and a **gap** (the stated difference between them). Migration planning, in lesson 8, exists purely to close stated gaps.

Now the pair that answers symptom 4 — solutions rated on their own merits instead of against what the enterprise actually needs. An **Architecture Building Block** states a requirement with no vendor attached: "single sign-on across the enterprise, meeting both clinical and administrative access rules." A **Solution Building Block** is the specific product bought to satisfy it. Evaluate a proposal against the ABB and you're asking "does the enterprise need this." Evaluate it only as an SBB and you're asking "does this product work" — a much easier question to answer yes to, and the wrong one.

A **stakeholder** has a **concern** — cost, risk, how long it takes, whether it passes an audit. A **viewpoint** is a recipe for building a representation that addresses one kind of concern; a **view** is what actually gets produced for one stakeholder from that recipe. The point of naming all four separately: "what do we show this person" becomes a decision tied to what they need to judge, instead of everyone getting the same diagram regardless of what they're actually deciding.

A **capability** is something the organization can do — usually named at a level well above any one system, and built from some mix of people, process, and technology together, not from technology alone.

An **architecture principle** is a rule, written down once, that a proposal gets checked against. This is symptom 1 and symptom 5 from F1, directly: a principle is something you can check a proposal against *before* it's built, and something a standing group can hold people to instead of re-litigating every time.

Governance vocabulary — Architecture Board, Architecture Compliance, Architecture Contract — and the Enterprise Continuum in more depth are coming in lessons 12 and 13. For now just recognize the names; later phase lessons will use them in passing before you've formally covered them.

## Anchor scenario: Northstar Regional Health

- **Enterprise**: Northstar's whole health system, since identity strategy is meant to span all six hospitals, not one.
- **Baseline / target / gap**: baseline is five separate identity systems (one per acquired hospital); target is one federated identity domain; the gap is the difference between them.
- **ABB vs. SBB**: the ABB is "single sign-on capability satisfying both clinical and administrative access requirements across all six hospitals" — a requirement, no vendor implied. The SBB is whichever specific identity product Northstar selects to fulfill it.
- **Stakeholder / concern / viewpoint / view**: a CISO's concern is risk exposure across all five current identity systems; a chief clinical officer's concern is clinician login friction during patient care. The same underlying architecture produces two different views, each built from a viewpoint suited to that concern.

## Guided exercise

Take a system or initiative you're familiar with and write:

1. One Architecture Building Block relevant to it, stated as a capability or requirement, with no vendor or product named.
2. One Solution Building Block that fulfills it.
3. One stakeholder, their concern, and what a view addressing that concern would need to show them.

## Debrief and model answer

Worked example — a network access capability: the ABB is "capacity for a stated number of concurrent authenticated sessions within a stated latency bound." The SBB is a specific vendor's access product, configured to that specification. The stakeholder is a network operations lead; their concern is capacity and latency; the view they need is a capacity dashboard against the stated bound, not a full network architecture diagram.

## Knowledge check

1. In TOGAF's sense, "enterprise" refers to:
    - a) Always the entire legal company.
    - b) Whatever collection of organizations shares a common set of goals.
    - c) Only the IT department.
    - d) A single system under architecture review.
2. The difference between an ABB and an SBB is:
    - a) ABBs are for business, SBBs are for technology.
    - b) An ABB states what's needed, vendor-neutral; an SBB is a specific implementation that fulfills it.
    - c) There is no meaningful difference.
    - d) SBBs are always more abstract than ABBs.
3. A "view" in TOGAF's sense is:
    - a) Any diagram produced during an architecture effort.
    - b) A representation built from a viewpoint to address a specific stakeholder's concern.
    - c) A synonym for a stakeholder.
    - d) The final approved architecture document.
4. The four architecture domains are:
    - a) Vision, Governance, Migration, Compliance.
    - b) Business, Data, Application, Technology.
    - c) Baseline, Target, Gap, Transition.
    - d) Enterprise, Segment, Capability, Solution.

Answers: 1-b, 2-b, 3-b, 4-b.

## Common misconceptions

- **"Enterprise always means the whole company."** It means whatever scope shares common architecture goals — sometimes narrower, occasionally broader than one legal entity.
- **"ABB and SBB are the same thing at different levels of detail."** They differ in kind, not just detail: an ABB is a requirement, vendor-neutral by design; an SBB is a specific, real implementation.
- **"A view is just another word for a diagram."** A view is tied to a specific stakeholder's concern through a defined viewpoint. Not every diagram produced during an architecture effort qualifies.

## References

Precise definitions: [Glossary](../../glossary.md). Terminology has been refined across TOGAF editions — check the current official glossary at [opengroup.org/togaf](https://www.opengroup.org/togaf) before relying on exact current wording for exam preparation.

## Version notes

- Draft written 2026-07-21.
