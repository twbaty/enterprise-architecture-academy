# F3 — The Architecture Development Method: the whole cycle

!!! note "Status"
    draft

## Lesson purpose

F1 and F2 gave you a problem and some words. This lesson gives you a mechanism: the actual method TOGAF runs to move an enterprise from baseline to target, on purpose, instead of by accident. By the end you should be able to trace one real change through the whole thing.

## Prerequisites

F2, or at least the [Glossary](../../glossary.md) entries for baseline, target, and gap.

## Learning objectives

1. Name the ADM phases in order and what each one decides.
2. Explain why the ADM is drawn as a ring, not a line.
3. Explain what Requirements Management does that no single phase does.
4. Trace one concrete change through a full pass of the cycle.
5. Explain iteration at more than one level — not just "start over from the beginning."

## Instructional narrative

### Why a ring, not a line

The standard diagram for the ADM is a circle of phases with one phase sitting in the center, connected to all the others. That shape is doing real work: an enterprise's target architecture is never a permanent end state. The target you set this year becomes next year's baseline, because the business keeps changing underneath it. A line implies you finish. A ring says: you run this again, on purpose, whenever the baseline and the target drift far enough apart to matter.

<figure>
<svg viewBox="0 0 700 800" xmlns="http://www.w3.org/2000/svg" role="img" aria-label="The ADM ring: Preliminary feeds into Phase A; phases A through H are arranged in a circle, each connected to a central Requirements Management hub.">
  <defs>
    <marker id="adm-arrow" viewBox="0 0 10 10" refX="5" refY="5" markerWidth="7" markerHeight="7" orient="auto">
      <path d="M0,0 L10,5 L0,10 z" fill="#5b6b8c"/>
    </marker>
  </defs>
  <g stroke="#5b6b8c" stroke-width="2" fill="none" marker-start="url(#adm-arrow)" marker-end="url(#adm-arrow)">
    <line x1="350" y1="123" x2="350" y2="154"/>
    <line x1="350" y1="460" x2="350" y2="306"/>
    <line x1="350" y1="460" x2="486.6" y2="373.4"/>
    <line x1="350" y1="460" x2="504" y2="460"/>
    <line x1="350" y1="460" x2="486.6" y2="546.6"/>
    <line x1="350" y1="460" x2="350" y2="614"/>
    <line x1="350" y1="460" x2="213.4" y2="546.6"/>
    <line x1="350" y1="460" x2="196" y2="460"/>
    <line x1="350" y1="460" x2="213.4" y2="373.4"/>
  </g>
  <g stroke="#8a97ad" stroke-width="2.5" fill="none" marker-end="url(#adm-arrow)">
    <path d="M350,140 A320,320 0 0 1 576.3,233.7"/>
    <path d="M576.3,233.7 A320,320 0 0 1 670,460"/>
    <path d="M670,460 A320,320 0 0 1 576.3,686.3"/>
    <path d="M576.3,686.3 A320,320 0 0 1 350,780"/>
    <path d="M350,780 A320,320 0 0 1 123.7,686.3"/>
    <path d="M123.7,686.3 A320,320 0 0 1 30,460"/>
    <path d="M30,460 A320,320 0 0 1 123.7,233.7"/>
    <path d="M123.7,233.7 A320,320 0 0 1 350,140"/>
  </g>
  <g font-family="sans-serif" text-anchor="middle">
    <circle cx="350" cy="65" r="58" fill="#eef1f6" stroke="#5b6b8c" stroke-width="2"/>
    <text x="350" y="69" font-size="13" fill="#1f2937">Preliminary</text>
    <circle cx="350" cy="460" r="92" fill="#f5b942" stroke="#b5822a" stroke-width="2"/>
    <text x="350" y="460" font-size="15" font-weight="bold" fill="#1f2937">
      <tspan x="350" dy="-9">Requirements</tspan>
      <tspan x="350" dy="18">Management</tspan>
    </text>
    <circle cx="350" cy="230" r="76" fill="#e8ecf5" stroke="#5b6b8c" stroke-width="2"/>
    <text x="350" y="230" fill="#1f2937">
      <tspan x="350" dy="-16" font-size="15" font-weight="bold">A</tspan>
      <tspan x="350" dy="16" font-size="10.5">Architecture</tspan>
      <tspan x="350" dy="14" font-size="10.5">Vision</tspan>
    </text>
    <circle cx="512.6" cy="297.4" r="76" fill="#e8ecf5" stroke="#5b6b8c" stroke-width="2"/>
    <text x="512.6" y="297.4" fill="#1f2937">
      <tspan x="512.6" dy="-16" font-size="15" font-weight="bold">B</tspan>
      <tspan x="512.6" dy="16" font-size="10.5">Business</tspan>
      <tspan x="512.6" dy="14" font-size="10.5">Architecture</tspan>
    </text>
    <circle cx="580" cy="460" r="76" fill="#e8ecf5" stroke="#5b6b8c" stroke-width="2"/>
    <text x="580" y="460" fill="#1f2937">
      <tspan x="580" dy="-16" font-size="15" font-weight="bold">C</tspan>
      <tspan x="580" dy="16" font-size="10.5">Information Systems</tspan>
      <tspan x="580" dy="14" font-size="10.5">Architectures</tspan>
    </text>
    <circle cx="512.6" cy="622.6" r="76" fill="#e8ecf5" stroke="#5b6b8c" stroke-width="2"/>
    <text x="512.6" y="622.6" fill="#1f2937">
      <tspan x="512.6" dy="-16" font-size="15" font-weight="bold">D</tspan>
      <tspan x="512.6" dy="16" font-size="10.5">Technology</tspan>
      <tspan x="512.6" dy="14" font-size="10.5">Architecture</tspan>
    </text>
    <circle cx="350" cy="690" r="76" fill="#e8ecf5" stroke="#5b6b8c" stroke-width="2"/>
    <text x="350" y="690" fill="#1f2937">
      <tspan x="350" dy="-16" font-size="15" font-weight="bold">E</tspan>
      <tspan x="350" dy="16" font-size="10.5">Opportunities</tspan>
      <tspan x="350" dy="14" font-size="10.5">and Solutions</tspan>
    </text>
    <circle cx="187.4" cy="622.6" r="76" fill="#e8ecf5" stroke="#5b6b8c" stroke-width="2"/>
    <text x="187.4" y="622.6" fill="#1f2937">
      <tspan x="187.4" dy="-16" font-size="15" font-weight="bold">F</tspan>
      <tspan x="187.4" dy="16" font-size="10.5">Migration</tspan>
      <tspan x="187.4" dy="14" font-size="10.5">Planning</tspan>
    </text>
    <circle cx="120" cy="460" r="76" fill="#e8ecf5" stroke="#5b6b8c" stroke-width="2"/>
    <text x="120" y="460" fill="#1f2937">
      <tspan x="120" dy="-16" font-size="15" font-weight="bold">G</tspan>
      <tspan x="120" dy="16" font-size="10.5">Implementation</tspan>
      <tspan x="120" dy="14" font-size="10.5">Governance</tspan>
    </text>
    <circle cx="187.4" cy="297.4" r="76" fill="#e8ecf5" stroke="#5b6b8c" stroke-width="2"/>
    <text x="187.4" y="297.4" fill="#1f2937">
      <tspan x="187.4" dy="-16" font-size="15" font-weight="bold">H</tspan>
      <tspan x="187.4" dy="16" font-size="10.5">Architecture Change</tspan>
      <tspan x="187.4" dy="14" font-size="10.5">Management</tspan>
    </text>
  </g>
</svg>
<figcaption>The ADM ring: Preliminary feeds into Phase A; A through H sit in a circle, each wired to Requirements Management at the center rather than to each other.</figcaption>
</figure>

Every phase from A through H connects to Requirements Management at the center, not to each other directly — that's the mechanism from the next section made visible. Preliminary sits outside that ring, feeding into Phase A once, before the cycle proper begins.

### The phases, in one line each

Full technique for each phase gets its own lesson later. For now, just the decision each phase exists to produce:

- **Preliminary** — decide how this organization will run the ADM itself: what gets tailored, skipped, or made stricter.
- **A — Architecture Vision** — get a stated, agreed direction and enough stakeholder backing to justify spending real effort on the rest.
- **B — Business Architecture** — decide the target business capabilities, processes, and organization.
- **C — Data and Application Architecture** — decide the target data and application landscape needed to support B.
- **D — Technology Architecture** — decide the target infrastructure needed to support B and C.
- **E — Opportunities and Solutions** — evaluate candidate solutions against what B, C, and D actually require, and decide which ones you're taking forward.
- **F — Migration Planning** — sequence the work: what moves first, what depends on what, what the risk is if it slips.
- **G — Implementation Governance** — check the thing actually being built against the architecture that was approved.
- **H — Architecture Change Management** — watch for drift or new demand significant enough to justify running part of this cycle again.

### The hub that never turns off

Every phase above runs, roughly, in its turn. **Requirements Management** doesn't — it runs continuously, underneath all of them, for the entire cycle.

Here's what it's actually for: Phase D discovers a hard technology constraint — say, a data residency rule a candidate platform can't meet — that quietly invalidates an assumption Phase B made two phases ago. Without a mechanism to carry that fact backward, it just gets lost; B's assumption stands unchallenged, and the architecture built on it is wrong. Requirements Management is that mechanism. It's the place every phase deposits what it discovers and draws what it needs, so a fact found late in the cycle can still reach the phase that needed to know it.

### One pass through the ring

Take a concrete case: the enterprise decides to consolidate five regional data centers down to two.

- **A** sets the vision — two data centers within eighteen months — and gets the executive sponsorship to make the next several phases worth doing.
- **B** decides which business processes must stay available during the transition, and which can tolerate planned downtime.
- **C** decides which applications move, which get retired outright, and what data residency constraints apply to each.
- **D** decides the target network, compute, and storage footprint for the two surviving data centers.
- **E** evaluates candidate migration approaches and vendor solutions against what B, C, and D actually specified — not against which one looks best on its own.
- **F** sequences it: which site migrates first, what the dependencies are, what the fallback is if a migration window is missed.
- **G** checks the migration as it happens against what was actually approved back in E and F — not just whether it works, but whether it's what was approved.
- **H** watches afterward. Three months post-migration, a business unit requests a third region for latency reasons the original vision didn't anticipate.

That request in H is a new fact. Requirements Management captures it, and depending on its size, it either reopens Phase A (if it changes the vision itself) or drops directly into B or D (if it's a scoped addition that doesn't touch the original vision at all). Either way, the ring runs again — not from panic, but because that's what the ring is for.

### Iteration happens at more than one level

"The ADM is iterative" doesn't just mean "loop back to Phase A when you're done." TOGAF describes iteration at several levels: across the whole cycle (a new planning cycle, effectively restarting), across a handful of adjacent phases (bouncing between B, C, and D as new information surfaces, without touching A), and within a single phase (refining one phase's own output before moving on). Most real architecture work never touches all three levels in a single pass — recognizing which level a new fact belongs at is part of the judgment the method requires.

## Anchor scenario: Northstar Regional Health

Run Northstar's identity consolidation through one lap: **A** sets the vision (one identity domain across all six hospitals, sponsored by the CIO). **B** decides which clinical and administrative processes can't tolerate any access disruption during cutover. **C** and **D** decide the target identity platform's data model and the infrastructure it runs on. **E** evaluates vendor identity products against that target, not against which one has the best demo. **F** sequences which hospital migrates first — likely the smallest, lowest-risk site. **G** checks each hospital's actual cutover against the approved design. **H**, a year later, catches a newly acquired seventh hospital that wasn't in scope at all — a fact Requirements Management routes back to reopen Phase A for that hospital specifically, without disturbing the five already migrated.

## Guided exercise

Pick a real change effort you've been part of (generalized, no confidential detail). For it, identify:

1. What, if anything, played the role of Phase A — a stated vision people actually agreed to before work started?
2. One fact that surfaced late (in what would be C, D, or G) that should have changed an earlier decision, but didn't reach the people who made it.
3. Which level of iteration that fact belonged at — whole-cycle, a few phases, or a single phase.

## Debrief and model answer

A common pattern: a project has something that functions as Phase A (a kickoff deck with a stated goal) but nothing that functions as Requirements Management. A constraint discovered during build (equivalent to D or G) — a licensing limit, a bandwidth ceiling — never gets carried back to whoever set the original scope, because no mechanism exists to carry it. The project finishes something, but not the thing the vision described, and nobody can point to the moment the two diverged.

## Knowledge check

1. The ADM is drawn as a ring rather than a line because:
    - a) It has more phases than a line could show clearly.
    - b) A target architecture is not a permanent end state; it becomes the next baseline.
    - c) The phases have no fixed order.
    - d) Governance requires a circular diagram by convention.
2. Requirements Management is different from the other phases because:
    - a) It only runs during the Preliminary Phase.
    - b) It runs continuously across the whole cycle, carrying facts between phases as they're discovered.
    - c) It is optional and most organizations skip it.
    - d) It replaces the need for Phase A.
3. A fact discovered in Phase D that invalidates an assumption from Phase B, without changing the original vision, is an example of iteration at:
    - a) The whole-cycle level.
    - b) The level of a handful of adjacent phases.
    - c) No level — this can't happen under the ADM.
    - d) The Preliminary Phase only.
4. Phase E's job is best described as:
    - a) Picking the vendor with the best demo.
    - b) Evaluating candidate solutions against what earlier phases actually specified.
    - c) Writing the final migration schedule.
    - d) Approving the budget for Phase F.

Answers: 1-b, 2-b, 3-b, 4-b.

## Common misconceptions

- **"You run the ADM once, start to finish, and you're done."** The ring shape exists specifically to reject this — the method assumes you'll run it again.
- **"Requirements Management is a phase you visit once, like the others."** It's active for the entire cycle, not a stop along the ring.
- **"Iteration means restarting from Phase A."** Most iteration is local — a handful of phases, or one phase — not a full restart.

## References

Phase names and the Requirements Management role are restated in original language, consistent with the current TOGAF Standard published by The Open Group. See the [Glossary](../../glossary.md) for ADM.

## Version notes

- Draft written 2026-07-21.
