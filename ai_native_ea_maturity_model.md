# AI-Native Enterprise Architecture Maturity Model — Matrix

**Version 1.1.0 — 2026-09-15.** Ten dimensions, five levels (A–E)
per dimension, family vocabulary and matrix form identical to
`STD-SDLC-MM`, `STD-PDLC-MM` and `STD-PRIORITIZATION-MM`. **Locked and
released. Registered as `STD-EA-MM`.** Dimension provenance: the nine elements
of the US Department of Commerce ACMM, as cited in TOGAF's Architecture
Maturity Models chapter, with two deliberate substitutions recorded under
*Dimension provenance* below.

This markdown document is intended as the source of truth for the matrix.
This model does **not** inherit D1–D3 from `STD-SHARED-INTELLIGENCE`:
that layer is market-scoped — market discovery, buyer persona,
positioning — and enterprise architecture is not a market-facing
function. Confirmed by reading the shared layer's own definition, not
assumed.

---

## How to read this matrix

Each dimension has a definition followed by a five-level ladder (A
through E). Levels describe **realistically adjacent states** — each
step implies a roughly costable set of changes, not "more AI, more
thoroughly." A level is not inherently good or bad; it is appropriate or
inappropriate for an organization's size, regulatory context, and risk
tolerance.

Dimensions are scored independently. An enterprise can be Integral in
one and Nascent in another, and ordinal levels are never averaged into a
composite score.

Each level is followed by the transition required to reach the next and
a **verification** statement — a practical test of whether the
destination has actually been reached rather than claimed. Level E is
followed by a sustainment note instead of a transition: at the top of
the ladder the work shifts from climbing to keeping the capability from
quietly regressing.

### Maturity-level names

Family-wide, identical across every dimension and every model in this
family.

| Letter | Name | In one line |
|---|---|---|
| A | **Nascent** | Ad hoc and inconsistent — nobody has yet defined what "good" looks like here. |
| B | **Modeled** | A real, deliberate method exists, but it's manual and owned by one person or function. |
| C | **Continuous** | The method runs constantly on its own cadence, still narrowly owned but always on. |
| D | **Integral** | The capability is load-bearing and shared beyond its original owner — removing it would break something real. |
| E | **Telemetric** | A continuous two-way loop: signal flows in, action flows back out, close to real time. |

---

### Pre-AI — the threshold state

**Pre-AI** designates a dimension in which an enterprise has not yet
adopted AI-assisted practices of any kind. It is a threshold position,
not a maturity level: it sits outside the A–E scale and carries no
letter.

**Pre-AI is not an assessment of general EA maturity.** A practice with
a rigorous TOGAF ADM cadence, a well-governed repository, and a scoring
history against classic EA maturity frameworks — but no AI tooling —
scores Pre-AI exactly as a practice with none of that does. This model
measures AI-native maturity; general architectural excellence is already
well measured elsewhere.

**Transition velocity.** Existing architectural discipline is
transferable substrate. A practice with a real ontology, enforced
metamodel conformance, or an operating repository will typically cross
levels faster than one without — the discipline transfers, the tooling
changes. Pre-AI dimensions may carry a narrative **readiness note**
recording the non-AI maturity that predicts transition speed. The
readiness note is not a score.

**Expect this state to be common.** Enterprise architecture is later to
agentic adoption than software delivery. An assessment in which most
dimensions score Pre-AI is an ordinary result, not a failing one.

### Exempt — the governed stance

**Exempt** designates a dimension an enterprise has deliberately
excluded from AI adoption as a matter of governed policy. It is a
stance, not a state: where Pre-AI describes a position an enterprise
intends to move from, Exempt records a decision it has made and stands
behind. An Exempt designation cites the governing constraint, is
excluded from aggregates, is always rendered rather than hidden, and is
reviewable.

---

### Dimension provenance

Seven dimensions carry the DoC ACMM element names unchanged:
Architecture Process, Architecture Development, Business Linkage, Senior
Management Involvement, Operating Unit Participation, Architecture
Communication, and Architecture Governance.

Two are substituted deliberately:

- **IT Investment and Acquisition Strategy → Strategic Portfolio
  Management & Asset Allocation (D8).** The original frames the scarce
  resource as software procurement. In an AI-native enterprise the
  scarce resources are capital, compute, token budget, and agentic
  capacity, and they are reallocated continuously rather than acquired
  annually.
- **IT Security → Governance & Authority Plane (D7).** Security as a
  *domain* was always an odd member of an architecture *capability*
  model. What agentic operation requires in its place is an explicit
  model of decision rights and the surfaces those rights reach.

**Scope boundary, stated rather than left absent.** This model does not
assess the security programme — data protection, secrets hygiene, vendor
risk, and regulatory security compliance are out of scope. What D7 does
carry is **reachability**: whether an authority boundary has been
established against the surface it actually covers.

---

## D1. Architecture process

*The capability to create, maintain, and align architectural intent, and
the degree to which semantic discipline and AI assist in translating
human strategy into executable governance.*

**Level A — Nascent**

Architecture processes are manual, document-heavy, and local to IT
silos. Semantic definitions vary by team: what counts as a "service" or
a "customer" differs between the groups that use the words. AI appears
informally, as an individual's brainstorming tool, with no shared
prompts, no common ontology, and no method for validating what it
produces.

**Transition A → B — Establish a machine-readable ontology**

Define a foundational enterprise ontology in a machine-readable form,
and a standardized, AI-assisted method for translating business
capabilities and technology standards into it. Replace fragmented
word-processing documents and static diagrams as the place architectural
meaning lives.

**Verification:** Two teams that previously used a term differently now
resolve it to the same definition by looking it up, and can say where
that definition lives.

**Level B — Modeled**

Architecture is captured in a formal, machine-readable schema grounded
in a stated ontology. Humans do the authoring and the mapping of
business intent into that schema. Generative AI is used as a copilot —
typically to normalize legacy documentation into the shared taxonomy —
but humans remain the mechanical drafters.

**Transition B → C — Charter agents to author, and move humans to validation**

Formally charter architectural AI agents with write access to the
architecture repository, under an explicit statement of what each may
and may not author. Shift the mechanical burden of drafting from humans
to agents, and redefine the human architectural role as validation of
the agent's output against the ontology.

**Verification:** A material architectural change was authored by a
chartered agent and accepted after human semantic review, and the
charter under which it acted can be produced.

**Level C — Continuous**

Chartered agents mechanically author and update the architecture into
the machine-readable single source of truth under stated constraints.
The human process has shifted from document creation to **semantic
validation** — confirming that generated models reflect business intent
and hold to the lexical discipline of the ontology.

**Transition C → D — Make the architecture answer planning questions**

Connect the machine-readable architecture into business planning cycles.
Require that a proposed strategic change be run as a simulation against
the architecture graph, showing downstream impact, before executive
approval.

**Verification:** At least one strategic decision was materially altered
— scope, sequence, or rejection — by what a simulation against the graph
showed, and the alteration is traceable to that run.

**Level D — Integral**

The ontology bridges the business and technology divide. During
planning, agents parse the semantic graph to run simulations that show
stakeholders the operational impact, risk, and cost of a proposed change
before it is committed. Once human consensus is reached, the updated
architecture dictates downstream execution constraints without manual
translation.

**Transition D → E — Close the loop with operational evidence**

Instrument the runtime environment to feed execution signal — system
logs, agent state, resource consumption — back to the architectural
agents, so that operational reality can be compared against declared
intent rather than assumed to match it.

**Verification:** A divergence between declared architecture and
operational reality was detected from telemetry rather than reported by
a person, and produced a reviewed proposal.

**Level E — Telemetric**

The architecture process is a continuous, empirically driven loop rather
than a scheduled drafting exercise. Agents ingest runtime telemetry and
compare operational reality against the ontology. When **semantic
drift** appears — the same concept realized inconsistently across the
estate — the agents draft and propose refactoring or process
optimization for the human review board.

**Sustainment**

Continuously refine the ontology as new business models emerge. The
specific risk at this level is an ontology that stops being revised
because everything downstream now depends on it: stability of meaning
and ossification of meaning look identical from inside.

---

## D2. Architecture development (artifacts and substrate)

*The capability to evolve architecture artifacts from static documents
into a machine-readable substrate that actively binds runtime
execution.*

**Level A — Nascent**

Artifacts are static, disparate, human-readable documents —
presentations, PDFs, whiteboard photographs. There is no central
repository and no consistent structure. AI cannot reliably reason over
the architecture because it has no standard form to read.

**Transition A → B — Impose structure before imposing schema**

Establish standardized templates, taxonomies, and structured formats to
replace ad-hoc documents, preparing the architecture for reliable
machine ingestion. This is a formatting discipline, not yet a data
model.

**Verification:** A tool — not a person — can enumerate the
architecture's artifacts and their types without bespoke parsing per
document.

**Level B — Modeled**

Architecture is developed using strict templates and a formal taxonomy,
but remains fundamentally document-centric rather than a schema or a
graph. Human architects manage the artifacts. AI ingests,
cross-references, and validates them, but the source of truth is still a
collection of human-authored files.

**Transition B → C — Migrate from documents to a schema, and generate the views**

Migrate the structured documentation into a unified machine-readable
schema. Charter an agent to maintain it and to generate human-readable
views on demand, so that no human-facing rendering is separately
maintained.

**Verification:** A human-consumable rendering — workbook, report,
diagram — was regenerated from the schema rather than edited, and the
previously hand-maintained version has been retired.

**Level C — Continuous**

Architecture is natively developed as data within a machine-readable
schema. A chartered agent maintains it and recomposes the graph into
human-consumable formats on demand, eliminating separately maintained
static diagrams. Traversal is fast enough that recomposition is
interactive rather than a batch job.

**Transition C → D — Extend the same schema to execution**

Extend access to the architecture repository down into engineering
execution environments, so that engineering agents and architectural
agents parse and traverse the same schema rather than a translation of
it.

**Verification:** An engineering agent took a constraint directly from
the architecture repository, and no separate engineering-facing copy of
that constraint exists to drift.

**Level D — Integral**

Architecture artifacts and engineering context are nodes in one
structure. Engineering agents parse the same repository to inherit their
constraints, rules, and configuration natively. The artifacts bound the
autonomy of the runtime environment without being translated into
separate engineering documents.

**Transition D → E — Let execution write back**

Embed telemetry hooks in execution environments and configure them to
write operational state changes and performance signal back into the
corresponding architectural nodes.

**Verification:** A node's recorded state changed because the system
changed, with no human edit in the path, and the change is attributable
to a named signal.

**Level E — Telemetric**

Nodes update their own status from execution telemetry. The artifacts
represent not the intended architecture but **the current operational
reality** of the estate, and human-readable exports carry empirical
drift and performance alongside design intent.

**Sustainment**

Prune and optimize the schema as telemetry volume and relationship
density grow, so that traversal stays interactive. Watch specifically
for nodes that update automatically and are read by no one: an
auto-updating artifact nobody consumes is cost without signal.

---

## D3. Business linkage

*The capability to connect business intent, strategic goals, and value
streams structurally to execution, so that technical and agentic work
traces to business authority.*

**Level A — Nascent**

Business strategy exists in isolation from architecture and engineering
backlogs, communicated as narrative documents. Units use conflicting
terms for the same functions. AI initiatives are shadow pilots with no
traceable linkage to enterprise value streams.

**Transition A → B — Distil narrative strategy into named structures**

Distil narrative business strategy into flat, ontological function
models and capability maps, with each function and capability formally
named and defined under the same semantic discipline as the rest of the
architecture.

**Verification:** Every strategic priority currently being funded can be
named as a capability that exists in the map, or is visibly absent from
it.

**Level B — Modeled**

The enterprise holds flat, ontological function models and capability
maps. Business functions and capabilities are formally named and
defined. Linkage between these artifacts and the execution layers
remains manual — cross-referenced by hand. AI assists in parsing
narrative strategy to draft the models.

**Transition B → C — Make lineage an edge, not a spreadsheet**

Ingest the function models and capability maps into the machine-readable
repository as first-class nodes, and replace manual cross-referencing
with lineage edges that resolve.

**Verification:** A proposed initiative was refused, or sent back, for
lacking a resolving edge to an approved capability — and the refusal
came from a check rather than from a person's recollection.

**Level C — Continuous**

Function models and capability maps are interconnected nodes in the
repository. Strategic intent is linked to technical components by
edges. Chartered agents evaluate proposed initiatives and engineering
tasks for an unbroken lineage to an approved capability, and work
lacking machine-verifiable lineage is rejected.

**Transition C → D — Bind operational constraints to capability nodes**

Bind decision thresholds, priority weightings, and agent autonomy
budgets directly to capability nodes, so that a shift in strategic
priority alters runtime constraints rather than only documentation.

**Verification:** A change made to a capability node — and nothing else
— measurably altered runtime behaviour downstream.

**Level D — Integral**

Business intent governs runtime boundaries. When executives alter
strategy, the change is made to the business nodes; because engineering
agents inherit constraints from those nodes, operational parameters,
authorization limits, and tool access reconfigure without manual
translation.

**Transition D → E — Measure realization, not just conformance**

Connect business performance measures — revenue, conversion, unit
economics — to runtime telemetry, so the architecture can evaluate
execution against outcomes rather than against compliance.

**Verification:** A capability that was fully conformant and
nevertheless failed to deliver its expected outcome was identified as
such, and the distinction was visible in the record.

**Level E — Telemetric**

The link between strategy and architecture is a self-evaluating loop.
Telemetry measures **value realization per capability node** against its
declared intent. When a component or agentic workflow fails to deliver
its expected outcome or exceeds unit-economic thresholds, the system
flags the strategic disconnect and models realignments for executive
review.

**Sustainment**

Recalibrate outcome measures as markets shift, so the loop does not
optimize against obsolete indicators. A closed loop pointed at a stale
KPI is more dangerous than an open one, because it acts.

---

## D4. Senior management involvement

*The capability of executive leadership to author foundational intent,
champion semantic discipline enterprise-wide, and trust the
architectural substrate to govern execution.*

**Level A — Nascent**

Executives treat architecture as an IT paperwork exercise. Strategic
intent is implicit, undocumented, or scattered across memos. No one
sponsors semantic alignment across units, so marketing, finance, and
technology operate with different definitions of the same things.

**Transition A → B — Put a name on the intent**

Executives formally endorse a unified effort to establish semantic
discipline, and begin explicitly authoring — or explicitly endorsing —
foundational strategic intent as a recorded artifact rather than a
shared understanding.

**Verification:** Foundational intent exists as a citable artifact with
a named author or endorser and a date, and a disputed definition has
been settled by reference to it.

**Level B — Modeled**

Executives author or formally endorse foundational intent, and champion
ontological work across non-technology functions. Management spends the
political capital required to make separate functions agree on unified
function models and capability maps, acting as final arbiter of semantic
disputes.

**Transition B → C — Mandate the repository as the system of record**

Mandate that the machine-readable repository is the official system of
record for strategic planning, and retire bespoke departmental strategy
decks as competing sources.

**Verification:** A strategic planning cycle completed with the
repository as its source, and at least one departmental deck was retired
rather than maintained alongside.

**Level C — Continuous**

Management mandates the repository as sole source of truth for strategy
and architecture. Executives consume strategic updates through the
chartered agent's generated renderings rather than commissioning manual
decks. No capital is deployed and no initiative funded unless it traces
to executive-authored intent in the graph.

**Transition C → D — Simulate before committing**

Shift executive decision-making to use the graph's simulation capability
before approving strategic pivots, organizational changes, or capability
reconfigurations.

**Verification:** A capital commitment was withheld, resized, or
resequenced on simulation evidence, and the decision record cites the
run.

**Level D — Integral**

Executives use the graph as their primary steering mechanism, relying on
simulation before committing capital. They understand that updating
foundational intent or capability constraints is not a documentation act
but an operational one that alters the boundaries and autonomy budgets
of downstream agents.

**Transition D → E — Let evidence reach intent**

Require executive review of operational telemetry, establishing that
runtime evidence informs the next cycle of intent authoring rather than
only the next cycle of delivery.

**Verification:** Foundational intent was revised, and the revision
cites operational evidence rather than conviction.

**Level E — Telemetric**

Executives consume architecture as an empirical feedback loop. When
agents flag that a capability is drifting from authored intent on
runtime evidence, management reviews the proposed realignments.
Foundational intent is refined on operational evidence — and **revisions
to intent are rare but non-zero**, which is itself the signal: intent
revised continuously cannot serve as a benchmark, and intent never
revised is not being tested.

**Sustainment**

Continuously calibrate the boundaries of agentic autonomy against risk
appetite as the market and the technology change. Watch the revision
rate of intent in both directions.

---

## D5. Operating unit participation

*The capability of business units, functions, and capability owners to
engage with, consume, and ultimately be guided by the enterprise
architecture.*

**Level A — Nascent**

Operating units treat architecture as an impediment. Functions operate
in silos with local, unstandardized terminology, relying on shadow
tooling and unsanctioned AI to solve local problems — bypassing the
architecture and creating blind spots in it.

**Transition A → B — Make the units author their own domains**

Require functional leaders to map their operations into the enterprise's
function models and capability maps, distinguishing their functions from
their capabilities in the shared ontology. Participation is authorship,
not review.

**Verification:** Each operating unit's domain is represented in the
shared models by text its own leaders wrote, and they can find it.

**Level B — Modeled**

Operating units participate in the semantic discipline. Leaders define
their domains explicitly within the standardized ontology. Units consume
the architecture as static reference to understand boundaries and
dependencies, but daily execution stays largely disconnected from the
model.

**Transition B → C — Move from reading documents to querying the model**

Shift units from consuming static reference material to querying the
chartered agent for tailored, current recompositions of the architecture
as an input to their own planning cycles.

**Verification:** A unit's planning cycle used a generated
recomposition, and the unit can state when its view was last current —
because the answer is "now."

**Level C — Continuous**

Units actively consume the architecture. Because the agent recomposes
the repository into formats tailored to each domain, functional and
capability leaders use it as their primary trusted tool for operational
planning, dependency tracking, and roadmap alignment. They trust it
because it is current.

**Transition C → D — Let the edge build, bound by the centre**

Empower units to deploy their own local workflow or engineering agents,
under the strict condition that those agents inherit execution
constraints natively from the enterprise repository rather than being
separately configured.

**Verification:** A unit-deployed agent was constrained by an enterprise
boundary it never had configured locally, demonstrated by the constraint
changing centrally and the unit's agent following.

**Level D — Integral**

Units drive innovation at the edge with their own agents and automated
workflows, which parse and bind to the enterprise repository. The
architecture informs and constrains unit execution in real time, so
local agility does not violate enterprise intent or security boundaries.

**Transition D → E — Expose the telemetry to the edge**

Expose runtime telemetry directly to unit leaders, shifting their focus
from deploying capabilities to measuring them against the graph.

**Verification:** A unit changed its own local workflow on telemetry it
read itself, without central prompting.

**Level E — Telemetric**

Units consume the architecture as a live operational view. Functional
leaders monitor the feedback loop to see how their domains execute
against intent, and rely on agents to highlight local inefficiency and
propose refactoring. **The distinctive measure at this level is the
centre's accuracy about the edge**: how faithfully the enterprise
repository reflects what operating units are actually doing.

**Sustainment**

Units must formalize local ontologies as they spin up new capabilities,
so the centre stays accurate. The failure mode is a repository that
describes the edge as it was chartered rather than as it operates.

---

## D6. Architecture communication

*The capability to socialize, query, and proactively surface
architectural intent, constraints, and semantics to humans and AI
assistants across the enterprise.*

**Level A — Nascent**

Communication is pull-based and human-to-human. Anyone needing
architectural guidance must find the right architect or search
fragmented repositories. Answers are frequently out of date by the time
they are given, and no channel is authoritative.

**Transition A → B — Give the architecture one address**

Centralize structured documentation and capability maps into a single,
visible repository that is the explicit reference point for all teams.

**Verification:** A question previously answered by asking a person is
now answered by going to a known location, and the location is the same
one for every team.

**Level B — Modeled**

The enterprise communicates architecture through a central repository
holding the function models and capability maps. Information is
standardized but communication is static and pull-based: users must
navigate to find the constraints relevant to their work.

**Transition B → C — Put a query layer in front of the graph**

Deploy an interface over the repository that allows the chartered agent
to act as a conversational query layer, recomposing the graph on demand
into the form the asker needs.

**Verification:** A non-architect obtained a correct, current answer to
an architectural question without knowing the repository's structure.

**Level C — Continuous**

Architecture is communicated through a browsable interface over the
repository and through natural-language query of the chartered agent.
Instead of searching static documents, stakeholders ask; the agent
traverses the graph and answers by recomposing it into a form tailored
to the asker.

**Transition C → D — Open the graph to non-technology assistants**

Open the repository to specialized functional AI assistants outside
technology — finance, HR, executive copilots — so they parse the
architecture at runtime to give their own users contextual guidance.

**Verification:** A functional assistant outside the technology
organization gave architecturally correct guidance, sourced from the
repository, to a user who never queried it.

**Level D — Integral**

Communication is decentralized and embedded in daily work. Functional
assistants parse the repository continuously, guiding their users and
defending the ontology in the moment — for instance, surfacing the
approved term while a memo is being drafted, so semantic drift is
prevented rather than corrected.

**Transition D → E — Let the architecture initiate**

Configure the architecture to speak without being asked: telemetry-driven
alerts when execution approaches or crosses an architectural boundary,
addressed to the owner of the thing affected.

**Verification:** An owner learned of a boundary condition from an
unsolicited, correctly addressed alert before anyone thought to look.

**Level E — Telemetric**

The architecture moves from queried reference to **initiator**. Driven
by telemetry, agents alert capability owners, functional assistants, and
engineering teams when semantic drift appears in production, performance
degrades, or a boundary is breached. The dialogue is empirical and
started by the system.

**Sustainment**

Continue training agents on local context and operational vernacular so
that proactive guidance is phrased in the language of the unit receiving
it. The failure mode at this level is alert fatigue: an unsolicited
channel that is ignored is worse than one that does not exist, because
it is believed to be working.

---

## D7. Governance and authority plane (Auctoritas)

*The capability to model, delegate, and programmatically enforce
decision rights, authority boundaries, the surfaces those boundaries
actually cover, and policy compliance across both human actors and
machine agents.*

**Level A — Nascent**

Governance is manual, fragmented, and bureaucratic. Policies live in
static documents or are enforced through ad-hoc committee review.
Nothing structurally distinguishes an action requiring executive
sign-off from a routine automated task, and no record states which
surfaces any given authority applies to. Agents and operational teams
act on implicit, unmonitored decision rights.

**Transition A → B — Name the authorities and their extent**

Model governance rules, decision thresholds, and authority delegations
as structured ontological nodes mapped to the capability map. For each
authority, state the surfaces it covers — the systems, data, and tools
inside its extent. An authority with no stated extent is undefined
rather than merely undocumented, because nothing can later establish
whether it was honoured.

**Verification:** For any consequential action, a reader can name both
who may authorize it and which surfaces that authorization reaches,
without asking the person who wrote the policy.

**Level B — Modeled**

Governance policies, decision rights, and authority boundaries are
formally defined and mapped to functions and capabilities within the
ontology, each naming the surfaces it covers. The enterprise holds a
documented map of who — or which agentic tier — may take which action
over what. Enforcement remains manual: periodic audits, human sign-offs,
and review boards.

**Transition B → C — Make the rules machine-verifiable, and establish reach by attempt**

Ingest the governance nodes and authority tokens into the
machine-readable repository so that proposed initiatives, changes, and
agentic workflows are checked automatically before clearance. In the
same motion, establish each boundary's actual reach by attempting access
rather than by reading configuration. A control's declared scope and its
enforced scope are two different claims, and only the second protects
anything.

**Verification:** A gate refuses a real action lacking a valid authority
path, demonstrated by attempting it rather than by inspecting the rule;
and for each enforced boundary, the reachable surface has been probed
rather than inferred from settings.

**Level C — Continuous**

Governance policies and authority tokens are active nodes in the
repository. Automated checks clear or block proposed initiatives,
engineering changes, and agentic workflows before deployment without
routing through committee review. Each enforced boundary's reach has
been established by attempt, so the surface a control actually covers is
known rather than assumed.

**Transition C → D — Mediate at runtime, and declare what is not mediated**

Move enforcement from deploy-time gating to runtime mediation, verifying
an actor's graph-backed authority at the moment of execution. Require
every mediation point to declare the paths by which it can be crossed,
or to assert that none exist. An undeclared exclusion is the boundary
most likely to be found first by someone outside the enterprise.

**Verification:** A consequential action is refused at runtime on
authority grounds; and every mediation point carries a current statement
of what it does not mediate, with at least one exclusion traceable to a
deliberate design decision rather than to an oversight.

**Level D — Integral**

The governance plane mediates execution in real time. No actor — a human
operating through an assistant, or an autonomous workflow — executes a
consequential action without the runtime verifying an explicit,
graph-backed authority token against the repository. Policies bind
dynamically: updating a risk threshold or decision right alters the
operational boundary across the system. Every mediation point states its
own exclusions.

**Transition D → E — Instrument the hits and the silence**

Connect runtime governance exceptions, policy violations, and
authority-boundary hits to a continuous telemetric loop. Instrument the
inverse in the same motion: a control that has never refused anything is
either unnecessary or pointed where nothing passes, and only telemetry
distinguishes the two.

**Verification:** The loop reports both boundary hits and un-fired
controls, and at least one control has been retired, retargeted, or
confirmed necessary on that evidence.

**Level E — Telemetric**

The governance plane is a self-regulating empirical loop. The system
continuously evaluates friction, exceptions, and risk events against
stated risk appetite, reporting not only where boundaries were hit but
**where they never were**. When policies prove overly restrictive, fail
to catch emerging risk, or enforce nothing at all, the architecture
flags the disconnect and proposes optimized rules and authority
realignments for executive endorsement.

**Sustainment**

Audit the governance graph against shifting regulatory landscapes and
macro strategy. Re-establish boundary reach by attempt on a standing
cadence: a surface probed once is a claim with a date on it, and
infrastructure changes without announcing itself.

---

## D8. Strategic portfolio management and asset allocation

*The capability to price, prioritize, and allocate capital, compute, and
agentic resources across competing initiatives on machine-verifiable
capability lineage.*

**Level A — Nascent**

Initiatives, software acquisitions, and AI projects are funded through
annual cycles and departmental politics. No shared model exists for
pricing risk or comparing competing efforts. AI spending is fragmented
across uncoordinated budgets with no portfolio-level visibility.

**Transition A → B — Price against the capability map**

Establish standardized, ontological frameworks for pricing initiatives
and mapping competing backlogs to enterprise capabilities, so that
competing proposals are compared on a common basis.

**Verification:** Two initiatives from different units were compared on
the same stated criteria, and the criteria existed before the comparison
rather than being constructed for it.

**Level B — Modeled**

The enterprise uses function models and capability maps to categorize
proposals, and standardized criteria to price and prioritize competing
initiatives. Allocation remains a periodic manual review, with budgets
locked into static allocations rather than shifting with feedback.

**Transition B → C — Require lineage to hold funding**

Ingest prioritized backlogs and portfolio allocations into the
repository, and require every funded initiative to hold valid, resolving
capability lineage.

**Verification:** Funding was withheld or withdrawn from an initiative
for lacking machine-verifiable lineage, not merely flagged for it.

**Level C — Continuous**

Portfolio priorities and allocations are maintained in the repository.
Proposed features, internal tooling, and agentic workflows are
prioritized against capability nodes using shared economic models.
Chartered agents assess the backlog continuously so that no capital or
compute is allocated without machine-verifiable business lineage.

**Transition C → D — Let resources move between planning cycles**

Move from periodic planning to continuous allocation, so that compute,
token budget, and agentic capacity flow toward verified high-yield
capabilities as evidence changes, with switching costs priced rather
than ignored.

**Verification:** Resources moved materially between capabilities
outside a planning cycle, and the switching cost of the move was
computed rather than assumed negligible.

**Level D — Integral**

Allocation operates as a continuous portfolio engine. The enterprise
prices and re-prices competing initiatives against shifting market
signal and strategic intent. Compute, token budgets, and agentic
capacity route to capability nodes demonstrating value realization, and
underperforming initiatives are deliberately starved.

**Transition D → E — Close the loop on unit economics**

Connect runtime telemetry and actual unit-economic outcomes to the
valuation engine, so reallocation responds to realized return rather
than projected return.

**Verification:** A reallocation was driven by realized unit economics
that contradicted the initiative's original valuation, and the
contradiction is on the record.

**Level E — Telemetric**

Portfolio management is an empirical, self-optimizing loop. The system
measures **realized economic return and operational efficiency per
funded capability** against its original valuation. When markets shift
or bottlenecks appear, the engine models — and where authorized,
executes — reallocation of compute, capital, and agentic capacity.

**Sustainment**

Recalibrate pricing and prioritization as macroeconomic conditions and
technology cost curves move, particularly token economics, which can
invalidate a valuation model without any change in the initiatives it
ranks.

---

## D9. Architecture governance

*The capability to maintain architectural integrity — shifting from
gatekeeping review toward hyper-available clarity and anomaly-driven
architecture review.*

**Level A — Nascent**

Architecture governance does not exist in practice. Teams build in
isolation, producing semantic fragmentation and structural debt.
Architectural failures are handled reactively as incidents, with no
systemic review.

**Transition A → B — Establish a baseline and a reference**

Establish a review process and centralize documentation so that teams
have a single point of reference for architectural standards, and a
known moment at which conformance is examined.

**Verification:** A change was examined against a written standard
before release, and the standard existed before the change.

**Level B — Modeled**

Governance relies on periodic review boards and manual audits. Teams
submit static artifacts for evaluation, and compliance is enforced
through scheduled meetings rather than continuous visibility.

**Transition B → C — Replace policing with availability**

Make the architecture hyper-available through a traversable repository
and conversational tooling, so that teams align their intent before
execution rather than being corrected after it. Reserve governance
intervention for friction that rises above ordinary noise.

**Verification:** The proportion of review findings raised *before*
implementation exceeded those raised after, and teams can say what they
consulted.

**Level C — Continuous**

Governance rests on proactive clarity rather than policing. Because the
repository is available and traversable, teams align to the models
without being made to. Intervention is the exception: operational
friction or semantic misalignment above baseline triggers a review that
treats the friction as a symptom of a design flaw rather than a
violation to punish.

**Transition C → D — Detect the friction rather than wait for it**

Automate detection of systemic friction and repeated boundary hits, and
feed those anomaly signals into the architecture practice as review
triggers.

**Verification:** An architecture review was triggered by detected
friction rather than by a person noticing, and the trigger threshold was
set in advance.

**Level D — Integral**

The governance plane monitors for systemic anomalies. When friction
points or repeated boundary hits cluster around a capability or a
boundary, the system flags a probable defect in the ontology or the
capability map and triggers a targeted review of the root cause rather
than the symptom.

**Transition D → E — Measure the health of the graph itself**

Connect anomaly detection into a continuous loop measuring the overall
structural and semantic stability of the enterprise graph, not only
individual incidents.

**Verification:** A structural pattern spanning multiple unrelated
incidents was identified from the loop, and no single incident would
have revealed it.

**Level E — Telemetric**

Architecture governance is a self-diagnosing system. The practice tracks
**the rate and distribution of friction-triggered reviews across the
graph** as its own health measure. When structural patterns emerge,
agents model and propose ontological refactoring, capability
adjustments, or intent realignments that eliminate friction at its
source.

**Sustainment**

Refine the sensitivity threshold for what counts as actionable friction
against normal variance. Both failure modes are live at this level: a
threshold too tight produces chase, and a threshold too loose produces a
governance function that reports health while the estate fragments.

---

## D10. Shared language (*Vocabula*)

*The capability to hold one governed vocabulary and operate it in both
directions — resolving a term to its precise sense inside the
enterprise, and translating it outward with a record of what the
translation collapsed.*

**Level A — Nascent**

Terms are used without shared referents and nothing surfaces the
divergence. The same word means different things in different
functions, and the difference is discovered in rework — a launch built
for one population, a contract written about another. Either no
glossary exists, or one exists and nobody can say where. Outward-facing
language is written per document, in whatever voice the author has.

**Transition A → B — Name the terms and their senses**

Enumerate the terms that actually collide, each with its distinct
senses and the function that owns each sense. **The test of inclusion
is collision in practice, not importance in the abstract** — a term
nobody disputes does not need a row. Each sense states what it covers
and what it excludes, because a definition without an exclusion cannot
settle an argument.

**Verification:** A reader can establish, without asking the author,
that the enterprise distinguishes *customer*, *buyer* and *user*, and
what each one excludes.

**Level B — Modeled**

A governed vocabulary exists. Terms have senses, senses have owners,
and the document is findable. **Nothing consults it.** The definitions
are correct and inert — read when someone is already suspicious, which
is the case where they were least needed. Outward translation remains a
per-author judgment. **An organization at B typically believes it is
higher, because the artifact exists and is not wrong.**

**Transition B → C — Put the definition where the language is produced**

Bind the vocabulary to the surfaces where writing happens — the
editor, the ticket, the document, the agent's context — so the
definition **arrives at the moment of authorship** instead of waiting
to be looked up. An agent meeting an ambiguous term challenges it in
one interaction, **cites the vocabulary as the source of the
challenge**, and makes the answer cheap to give.

**Verification:** An author writing an ambiguous term is challenged as
they write it; the challenge names the vocabulary it came from; and
answering costs one click rather than a sentence.

**Level C — Continuous**

The vocabulary is active at the point of authorship. Ambiguity is
surfaced rather than discovered downstream, and the challenge cites its
source so the author can judge whether to trust it. **The author can
answer *loose sense, deliberately* and proceed.** Outward-facing
language is still handled term by term: nothing distinguishes a term
that must be translated for an external reader from one that may cross
unchanged.

**Transition C → D — Resolve what context settles, and invert the control at the boundary**

**Two moves, one capability.** *Inward:* give the agent enough governed
context — function, audience, document type — that a term whose sense
the context settles is **resolved rather than queried**, with the agent
stating which sense it used. **Asking is correct for genuine ambiguity
and is a tax everywhere else.** *Outward:* at the boundary the
operation inverts. An internal term leaving for an external reader is
not disambiguated, it is **translated**, and the translation **records
what it collapsed**.

**Verification:** For an internal document in a known function, the
agent resolves without asking and names the sense it used. For an
outbound document, the same term raises the reverse challenge — *this
word carries three senses inside and one outside; is the collapse
intended?* — and the answer is recorded with the document.

**Level D — Integral**

One vocabulary, two governed operations. Inside, terms resolve from
context and the agent states its reading, so precision is affordable
and traversal is deep — a term reaches its sense, its siblings and its
owner. At the boundary, translation is a controlled act whose
collapses are recorded with the document that made them, so a later
reader of the contract and a later reader of the press release can each
establish what was meant. **The distinction survives the crossing in
both directions.**

**Transition D → E — Measure the vocabulary against its own use**

Instrument both operations: where terms are queried, where they
resolve, where authors mark a sense deliberately loose, and where an
outbound translation is overridden. **Read the results as evidence
about the MODEL rather than about the authors.** A distinction
repeatedly waved away is one the enterprise does not hold.

**Verification:** A term is retired, merged or re-scoped on the
evidence of its own usage record, and the change is traceable to the
measurements that prompted it.

**Level E — Telemetric**

The vocabulary is a measured instrument. The enterprise can see which
distinctions its people operate and which they route around, and
corrects the model on that evidence rather than on advocacy. **Terms
are retired and merged as readily as they are added.** The outward
translation layer is tuned by what external readers actually misread,
not by what internal authors assume they will.

**Sustainment**

Reconcile the model against its own usage record on a standing
cadence, retiring distinctions the enterprise has stopped operating.
Both failure modes are live here: a vocabulary that keeps every
distinction becomes ceremony, and one that merges on waiver counts
alone loses the term a single function was the only one using.

---

### D1 / D2

- D1 governs **how architectural intent is formed and validated** — the
  process and the human role within it.
- D2 governs **what the architecture is made of** — the artifacts and
  the substrate they live in.
- A practice can run a mature process over a poor substrate, and a rich
  substrate can be maintained by an immature process. Score them apart.

### D3 / D8

- D3 governs whether work **traces to business authority** — lineage and
  intent.
- D8 governs how **scarce resources are allocated among** things that
  all trace correctly.
- Valid lineage is a precondition for D8, not a substitute for it:
  everything in a portfolio can be properly linked and still be the
  wrong portfolio.

### D4 / D5

- D4 governs the **authoring of intent** and the trust placed in the
  substrate by those who author it.
- D5 governs **consumption and participation** by those who operate
  within it.
- The two move independently and often diverge: executive mandate
  without unit participation produces a repository nobody uses, and unit
  adoption without executive mandate produces a repository nobody obeys.

### D7 / D9

- D7 governs whether an actor **may act**, and over **which surfaces**.
- D9 governs whether the architecture itself remains **coherent**, and
  treats friction as a symptom of a design flaw.
- An action can be fully authorized and still indicate an ontological
  defect. That is D9's signal, not D7's.
- **Neither covers the security programme.** Data protection, secrets
  hygiene, vendor risk, and regulatory security compliance are outside
  this model's scope — stated as a boundary rather than left as an
  absence.
