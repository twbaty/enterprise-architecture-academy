# F5 — Applying the ADM: Iteration, Landscape, and Architecture Capability

!!! note "Status"
    draft

## Lesson purpose

F3 told you the ADM is iterative. This lesson gives you the tools for actually running it that way in a real organization: deciding how to scope and split the work, seeing what's already deployed before you plan more of it, and standing up the ongoing function that runs all of this rather than a one-off project team.

## Prerequisites

F3, F4.

## Learning objectives

1. Decide, for a given change, which level of iteration it actually needs.
2. Explain Architecture Partitioning and why a single enterprise-wide ADM pass doesn't scale.
3. Explain Architecture Landscape and how it differs from a target architecture.
4. Explain why an Enterprise Architecture Capability has to be a standing function, not a project team that disbands at delivery.
5. Explain how agile delivery cadences and the ADM's phase structure coexist rather than conflict.

## Instructional narrative

### Choosing the right level of iteration

F3 named three levels the ADM can iterate at: the whole cycle, a handful of adjacent phases, or a single phase. Applying that in practice means asking a scoping question every time new information shows up: does this change the vision itself, or does it just change one phase's output without touching what was agreed in Phase A? A newly discovered technology constraint that still fits inside the agreed vision only needs to reopen the phases it actually affects. A change to the vision itself — new scope, a different sponsor, a materially different goal — needs to reopen Phase A, because everything downstream was built on that vision holding.

Getting this wrong in either direction has a real cost: reopening the whole cycle for a change that didn't need it wastes the work already done and signals to stakeholders that nothing is ever actually settled. Treating a vision-level change as a local, single-phase fix produces an architecture that technically satisfies its own internal logic while no longer serving the goal anyone actually approved.

### Architecture Partitioning: splitting the work so it scales

A single enterprise runs many architecture efforts at once — not one ADM cycle for the whole enterprise, but several, scoped to different segments: a business unit, a geography, a domain like identity or data. **Architecture Partitioning** is the discipline of deciding how to split the work into pieces that can run semi-independently, without either duplicating effort or losing the enterprise-level coherence that's the entire point of doing this at all.

The judgment call is where to draw the boundaries. Partition too coarsely and every partition still has to coordinate with every other one constantly, which defeats the purpose of splitting the work. Partition too finely and you're back to F1's original symptom — domains planning independently with no shared picture — just with more formal-sounding boundaries around the same fragmentation.

### Architecture Landscape: what's actually out there right now

A target architecture describes where you're headed. The **Architecture Landscape** is different: it's a description of what's actually deployed and in flight right now, at a given level of detail, maintained as part of the Architecture Repository. Without it, "what do we already have" is a question someone has to answer from memory or by asking around — which is exactly the failure named back in F1: no central place records what already exists, so every new proposal gets evaluated as if it were the first of its kind.

### Why an Enterprise Architecture Capability has to be standing, not temporary

A project team disbands when it delivers. An Enterprise Architecture Capability doesn't, because the problem it exists to solve doesn't end at delivery: new proposals keep arriving, the landscape keeps drifting from the target, and someone has to keep evaluating both. This is F1's symptom 5, given its actual name: "no central evaluation of architecture or technology" is precisely the absence of a standing Architecture Capability. Standing up the capability means committing to roles, a repository, and a governance function that persists — not assembling a team for one initiative and letting the function evaporate when that initiative ships.

### Agile delivery and the ADM aren't in tension

A common assumption is that a phased method like the ADM is incompatible with agile, iterative delivery. In practice they operate at different altitudes: the ADM governs how the *architecture* for a body of work gets developed and kept coherent over time; agile delivery governs how a *team* builds and ships increments of a specific solution. A team can run two-week sprints building toward a target architecture that itself only gets substantially revisited every few months. The ADM doesn't require big upfront design frozen for a year — it requires that when the target does change, the change is deliberate and traceable, not just whatever the last sprint happened to produce.

## Anchor scenario: Northstar Regional Health

Northstar's six-hospital identity consolidation is one partition of a larger enterprise architecture effort — clinical systems, network modernization, and data center consolidation are separate, parallel partitions, each with its own ADM pass, coordinated through a shared Architecture Landscape so the identity team can see that the network team is mid-migration on two of the same six hospitals. The standing Enterprise Architecture Capability is what actually notices that overlap; a temporary identity project team, focused only on its own partition, would have no reason to look for it.

## Guided exercise

Take a change effort you've observed. Identify: was it partitioned sensibly, or did it either drag in unrelated work to coordinate, or ignore an adjacent effort it should have coordinated with? And separately — was there a standing function that would have caught a landscape conflict, or did that depend on someone happening to know about the other effort personally?

## Debrief and model answer

A frequent pattern: two initiatives target the same infrastructure segment months apart, each unaware of the other, because there's no maintained Architecture Landscape either could have checked. Partitioning wasn't the failure — the two efforts were reasonably scoped on their own terms. The missing piece was the standing capability that should have been tracking the landscape across both partitions and flagged the overlap before either team committed resources.

## Knowledge check

1. A newly discovered fact that changes the vision agreed in Phase A requires:
    - a) No action; Phase A is fixed once approved.
    - b) Reopening Phase A, since everything downstream depended on that vision.
    - c) A silent adjustment in whichever phase discovered it.
    - d) Escalation to Phase H only.
2. Architecture Partitioning exists primarily to:
    - a) Give every business unit its own independent architecture with no coordination.
    - b) Split work into pieces that can run semi-independently without losing enterprise-level coherence.
    - c) Reduce the number of stakeholders involved.
    - d) Replace the need for an Architecture Repository.
3. The Architecture Landscape differs from a target architecture because it describes:
    - a) What is planned for five years from now.
    - b) What is actually deployed and in flight right now.
    - c) The organization's governance structure.
    - d) A generic, industry-wide reference model.
4. An Enterprise Architecture Capability is described as a standing function rather than a project team because:
    - a) It is required by law.
    - b) New proposals and landscape drift don't stop after any single delivery.
    - c) Project teams are more expensive to run.
    - d) TOGAF requires a minimum team size.

Answers: 1-b, 2-b, 3-b, 4-b.

## Common misconceptions

- **"Every new fact means restarting the whole ADM cycle."** Most iteration is local — reopen only what the fact actually affects.
- **"Partitioning means each business unit gets total independence."** The point is coordinated semi-independence, not fragmentation with better branding.
- **"Agile delivery and the ADM are incompatible."** They operate at different altitudes and can run at the same time without conflict.

## References

Terms are restated in original language, consistent with the current TOGAF Standard published by The Open Group. See the [Glossary](../../glossary.md).

## Version notes

- Draft written 2026-07-21.
