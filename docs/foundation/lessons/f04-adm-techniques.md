# F4 — ADM Techniques, Principles, and Stakeholder Management

!!! note "Status"
    draft

## Lesson purpose

F3 gave you the ADM's shape. This lesson gives you the working tools that get used inside that shape, no matter which phase you're in: architecture principles, stakeholder analysis, business scenarios, interoperability, readiness assessment, and risk. At Foundation depth, the job is recognizing each technique and what it's for — applying them under real, conflicting pressure is Practitioner's job.

## Prerequisites

F3.

## Learning objectives

1. Explain what an architecture principle is for, and what makes one usable versus decorative.
2. Run a basic stakeholder analysis: map power and interest, and connect each stakeholder to a concern.
3. Explain what a business scenario is and when it's worth building one.
4. Explain interoperability as a design concern, not just a technical checkbox.
5. Explain what a Business Transformation Readiness Assessment checks for, and why architecture work fails without it even when the design is sound.
6. Explain how risk is tracked across the ADM rather than handled once and forgotten.

## Instructional narrative

### Architecture principles: rules that get checked, not posters

An architecture principle only earns its place if someone can point at a real proposal and say "this violates principle 4" — that's the whole test. A principle that can't be checked against a concrete decision is decoration, not a working tool.

A usable principle has three parts: a **statement** (the rule itself), a **rationale** (why it matters enough to constrain behavior), and **implications** (what it costs to follow it — because a principle with no real cost isn't constraining anything). "Prefer cloud-native services over self-managed infrastructure" is a real principle: it's checkable, it has a rationale (reduced operational burden), and it has implications (vendor dependency, migration cost for existing self-managed systems). "Strive for excellence in architecture" is not a principle — nothing can violate it, so it can never be the reason a proposal gets rejected.

### Stakeholder analysis: power and interest, not just a contact list

A stakeholder list without power and interest attached is just an address book. The useful version places each stakeholder on two axes — how much power they have to help or block the work, and how much interest they have in its outcome — because that placement tells you what to actually do with each person: someone with high power and low interest needs to be kept satisfied with minimal engagement, not flooded with detail they didn't ask for; someone with high interest and low power needs to be kept informed, since they can't block you but can make life difficult if blindsided; someone high on both is who you manage closely.

This connects directly to a gap named back in F1: "no discussion of the architecture of the enterprise, only independent domain sizing." Part of why that gap exists is stakeholder analysis skipped entirely — nobody mapped who actually had a concern about the combined footprint, so nobody thought to ask them.

### Business scenarios: forcing the "why" before the "what"

A business scenario is a short, structured description of a real business problem, its context, and the desired outcome — written before any solution work starts. Its job is narrow: force an explicit answer to "why does this need architecture work at all" before anyone reaches for a design. Not every initiative needs a formally written business scenario; the technique is worth using when the problem is ambiguous enough, or the stakes high enough, that skipping straight to a solution risks solving the wrong problem well.

### Interoperability: a design concern, not a checkbox

Interoperability is usually treated as "can System A pass data to System B" — a yes/no technical check. TOGAF treats it as a design concern with degrees: two systems can exchange data but disagree on what it means (a shared field that two systems interpret differently is technically interoperable and substantively broken), or exchange data cleanly but couple two systems so tightly that changing one breaks the other. Treating interoperability as a spectrum to be designed for, rather than a box to check once integration works, is the actual skill.

### Business Transformation Readiness Assessment: the organization is part of the architecture

A technically sound design can still fail — not because the architecture was wrong, but because the organization wasn't ready to absorb it. A Business Transformation Readiness Assessment checks factors like: is there genuine sponsorship, or just nominal approval? Do the people who'll operate the new state have the skills for it? Is there capacity to run the old and new states in parallel during transition, or will the organization be asked to do both jobs with the staffing for one? None of these are architecture questions in the traditional sense — they're organizational questions that determine whether the architecture survives contact with reality.

### Risk: tracked across the cycle, not handled once

Risk isn't a single gate passed once, early, and then forgotten — it's tracked and re-assessed continuously as the ADM cycle proceeds, because the risk picture that existed when a vision was approved is rarely the risk picture that exists by the time implementation starts. A residual risk accepted in Phase A (say, "we're proceeding without a full data residency review because timeline pressure is high") is a fact Requirements Management needs to carry forward — otherwise it just quietly disappears, and the person governing implementation in Phase G has no idea a risk was ever accepted rather than resolved.

## Anchor scenario: Northstar Regional Health

Northstar's identity consolidation, run through these techniques: a usable principle might be "identity must be centrally federated across all hospitals" — checkable against any hospital's proposal to stand up its own local directory. Stakeholder analysis places the CISO (high power, high interest — manage closely) against a hospital's local IT lead (lower power, high interest — keep informed, since they'll surface real operational friction the CISO won't see). A Business Transformation Readiness Assessment might reveal that three of six hospitals' helpdesk staff have never operated a federated identity system — a readiness gap no technical design review would catch.

## Guided exercise

Take a principle, real or draft, from your own organization (or write one). Check it against the three-part test: does it have a stated rationale, and can you name a real implication — something it costs to follow? If it fails either test, rewrite it until it passes.

## Debrief and model answer

A common failure: "we will use industry-standard technologies" — no rationale beyond appeal to authority, and no real implication, since almost anything can be described as "industry-standard" after the fact. A working replacement: "new systems must support SAML 2.0 federation" — rationale (centralized identity control), implication (excludes products that only support proprietary or legacy auth), and it's directly checkable against any specific proposal.

## Knowledge check

1. What makes an architecture principle usable rather than decorative?
    - a) It is approved by an executive.
    - b) It has a stated rationale and a real implication, so a specific proposal can be checked against it.
    - c) It is written in formal language.
    - d) It applies to every possible situation without exception.
2. In stakeholder power/interest mapping, a stakeholder with high power and low interest should be:
    - a) Ignored entirely.
    - b) Managed closely with frequent detailed updates.
    - c) Kept satisfied with minimal engagement.
    - d) Removed from the stakeholder list.
3. A Business Transformation Readiness Assessment primarily checks:
    - a) Whether the technical design is sound.
    - b) Whether the organization can actually absorb the change, independent of the design's technical merit.
    - c) The project budget.
    - d) Compliance with data residency law.
4. Risk in the ADM is best described as:
    - a) Assessed once at the start and then closed.
    - b) Tracked and re-assessed continuously as the cycle proceeds.
    - c) Solely the responsibility of Phase G.
    - d) Not formally part of the method.

Answers: 1-b, 2-c, 3-b, 4-b.

## Common misconceptions

- **"A principle that sounds good is a good principle."** If nothing can violate it, it isn't doing any work.
- **"Interoperability is a yes/no technical fact."** It's a spectrum with real design trade-offs, not a single check.
- **"Readiness assessment is a soft, optional add-on."** A technically sound architecture can fail entirely without it — it's not optional, it's a different axis of the same risk.

## References

Terms and techniques are restated in original language, consistent with the current TOGAF Standard published by The Open Group. See the [Glossary](../../glossary.md).

## Version notes

- Draft written 2026-07-21.
