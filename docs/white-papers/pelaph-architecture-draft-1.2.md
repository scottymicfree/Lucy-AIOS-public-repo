# P.E.L.A.P.H. Architecture White Paper

**Planetary Ecosystem Layer for Analysis, Prediction & Hazards — Draft 1.2**

**Author:** Randy Webb  
**Status:** Research / white-paper text edition  

> This GitHub edition is a text transcription of the authored paper. Layout, figures, tables, pagination, and typography may differ from the formatted PDF edition.

---



---

P.E.L.A.P.H. Architecture White Paper | Draft 1.2 | September 2026 | 1
P.E.L.A.P.H.
Planetary Ecosystem Layer for Analysis, Prediction & Hazards
Architecture White Paper
Draft 1.0 | September 2026
A governed architecture for turning heterogeneous planetary observations into traceable analysis, bounded prediction, hazard
intelligence, simulation, and accountable action.
Architecture status Research and development
Operating persona Lucy
Governance authority E.M.M.A. - Enhanced Machine Mind Architecture
Executive Summary
P.E.L.A.P.H. - the Planetary Ecosystem Layer for Analysis, Prediction & Hazards - is a developing systems architecture intended to
combine live environmental and infrastructure observations, evidence-aware analysis, simulation, prediction, hazard reasoning, and
governed execution within one auditable framework.
Its purpose is not to create an unconstrained autonomous system that reacts to every incoming signal. P.E.L.A.P.H. instead treats data
ingestion, interpretation, prediction, simulation, authority, execution, and verification as distinct stages. Observations can inform the
system without automatically becoming truth; predictions and simulations remain distinguishable from measured history; and
consequential actions are intended to pass through an explicit governance boundary.
Lucy is the operating intelligence and human-facing persona within the broader P.E.L.A.P.H. system. E.M.M.A. provides the
governance and authority layer. Helix provides a controlled build, training, and specialist work environment. Live Earth supplies
time-stamped observations. Twin Earth is the proposed simulation and counterfactual environment. External models, cloud resources,
scientific feeds, and specialist agents are treated as replaceable capabilities rather than sovereign authorities.
1. The Problem
Planetary risk information is fragmented across scientific agencies, sensors, infrastructure operators, forecasting systems, public-health
sources, and specialized models. These sources differ in latency, geographic coverage, confidence, provenance, semantics, and
update cadence. Combining them into a useful intelligence system creates a second problem: a system capable of reasoning across
many domains must also be able to explain what it observed, what it inferred, what it simulated, why it acted, and who or what
authorized the action.
P.E.L.A.P.H. addresses these as one architectural problem: build a shared planetary evidence layer while preserving source
provenance, epistemic boundaries, governance, and post-action accountability.
2. Design Principles
• Evidence before assertion: Claims should be traceable to observations, models, assumptions, or explicit inference.
• Observation is not prediction: Measured history, forecasts, simulations, and hypotheses remain separate evidence classes.
• One operating coordinator: Lucy coordinates work; specialist agents and models propose or perform bounded work rather than
becoming independent authorities.
• Authority is explicit: Capability does not imply permission. E.M.M.A. is intended to govern admission and consequential execution.
• Verification closes the loop: Execution is not considered complete merely because a tool reports success; results should be
independently checked where practical.
• Replaceable providers: Models, clouds, scientific services, and compute providers should remain adapters to the architecture rather
than defining it.
• Local-first, scalable outward: Core governance can remain local while approved workloads use remote or elastic compute when
necessary.
3. System Architecture
At a high level, P.E.L.A.P.H. separates observation, reasoning, governance, execution, simulation, and evidence retention.


---

P.E.L.A.P.H. Architecture White Paper | Draft 1.2 | September 2026 | 2
Layer Role Authority boundary
P.E.L.A.P.H. Parent planetary analysis, prediction and hazard
architecture.
Defines the system context; does not erase
lower-level governance.
Lucy Operating intelligence, conversation interface,
orchestration and competency selection.
Coordinates; does not grant herself unrestricted
execution authority.
E.M.M.A. Governance kernel and authority boundary. Admits, constrains, records and governs
consequential work.
Live Earth Read-only, time-stamped observation fabric. Incoming data is evidence, not automatic authority.
Twin Earth Proposed simulation, scenario and counterfactual
environment.
Simulated/predicted state must not overwrite
observed history.
Helix Controlled build, training, test and specialist-work
environment.
Workers operate within bounded tasks and
governed handoffs.
Eagle Eye Independent observation/security evidence
function.
Observes and reports; should not silently become
the executor.
DeltaVault / evidence ledger Immutable or append-oriented evidence and
decision history.
Preserves provenance and accountability.
4. Evidence and Data Fabric
The Live Earth lane is intended to normalize heterogeneous external observations into a common, time-aware evidence fabric.
Candidate sources include seismic activity, weather and climate observations, space weather, aviation and mobility signals, air quality,
wildfire events, streamflow and flood data, public-health surveillance, ocean and buoy observations, ocean acidification indicators,
volcanic activity, and electricity/grid information.
The architecture also tracks planetary-boundary context. Current development work models nine planetary boundaries through thirteen
control variables. These are intended to provide system-level environmental context rather than a single deterministic score of planetary
safety.
Evidence classes
Class Meaning Rule
Observed Measured or reported state from an identified
source.
May enter observation history with timestamp and
provenance.
Derived Calculated from observations using a declared
method.
Must retain lineage to inputs and method.
Predicted Estimated future state. Must remain distinguishable from observation.
Simulated State generated inside a model or Twin Earth
scenario.
Cannot silently enter observed history.
Hypothetical Exploratory assumption or counterfactual. Must be explicitly labeled and bounded.
5. From Observation to Hazard Intelligence
P.E.L.A.P.H. is intended to reason across multiple signals without treating correlation as causation or model output as fact. A
representative flow is:
1. Acquire a source observation and record its identity, timestamp, coverage and provenance.
2. Normalize the observation into the shared evidence contract.
3. Score source quality, freshness, confidence and applicability.
4. Evaluate whether the observation activates a relevant dependency or cascade relationship.
5. Admit eligible state changes through the E.M.M.A. authority boundary.
6. Update Live Earth state without contaminating historical observations with predictions or simulations.
7. When warranted, construct Twin Earth scenarios and invoke specialist models.
8. Produce bounded predictions or hazard assessments with uncertainty and evidence lineage.
9. Present recommendations or proposed actions to the appropriate governance/human approval path.
10. Execute only authorized actions, verify outcomes, and retain the evidence trail.


---

P.E.L.A.P.H. Architecture White Paper | Draft 1.2 | September 2026 | 3
6. Lucy: Operating Intelligence
Lucy is the operating persona inside P.E.L.A.P.H., not the entirety of the system. Lucy interprets human requests, maintains task
identity and context, selects relevant competencies, coordinates specialist work, explains results, and presents governed actions. The
design intentionally avoids creating multiple independent 'Lucys.' External agents, models, and tools participate as specialists under
bounded task contracts.
This distinction allows the system to use different AI providers or local models without transferring system identity or governance
authority to any one provider.
7. E.M.M.A.: Governance and Admission
E.M.M.A. - Enhanced Machine Mind Architecture - is the governance kernel. The target architecture separates the ability to perform an
action from the authority to perform it. An external event, model recommendation, specialist proposal, or simulation result can request a
state transition; it should not obtain that authority merely by existing.
The planned E.M.M.A. Admission layer is therefore a critical boundary between incoming evidence/cascade activation and changes to
governed system state. Authorization can include typed work, short-lived context or execution leases, trust requirements, human
confirmation, quarantine, and an auditable record of the decision.
8. Twin Earth
Twin Earth is the proposed simulation layer of P.E.L.A.P.H. It is intended to maintain a computational representation that can explore
scenarios, propagate modeled effects, compare interventions, and support hazard reasoning without rewriting the factual Live Earth
record.
NVIDIA Earth-2, Omniverse and OpenUSD are being explored as supporting technologies for weather/climate modeling, scene
representation and visualization. They are components, not the governing architecture. A separate Twin Earth white paper will define
simulation state, synchronization, uncertainty, spatial representation, scenario branching, and the boundary between observed and
synthetic state.
9. Helix and Governed Engineering
Helix is the system's development, training and controlled specialist-work environment. Its intended role is to let Lucy coordinate
bounded engineering or analytical work through tools such as Codex, Sol, local models, and future providers while preserving task
identity, isolation, verification, and governance.
Future cloud workstations and elastic GPU/CPU resources may be provisioned beneath this layer. Infrastructure-as-Code tools such as
Terraform could eventually provide reproducible infrastructure, while E.M.M.A. remains responsible for whether a proposed
infrastructure change is authorized.
10. Security, Verification and Accountability
P.E.L.A.P.H. treats security as more than access control. The architecture aims to preserve an evidence chain from observation through
reasoning and execution. Eagle Eye provides an independent observation/security role; governed sandboxes isolate executable work;
verification checks outcomes; and the evidence ledger preserves the record needed to reconstruct why a decision occurred.
The long-term objective is simple auditability: a human should be able to ask why the system reached a conclusion or performed an
action and receive a traceable explanation grounded in the relevant evidence, authority, execution and verification records.
11. Current Development Status
Area Status Scope
Lucy operating persona Active development Conversation, orchestration, competency and
governed-runtime integration.
E.M.M.A. governance Active development Existing governance concepts and records;
admission/authority layer remains an active gate.
Live Earth feed fabric Prototype / active development Source registry, scoring, observation contracts,
cascade evaluation and boundary variables.
Twin Earth Foundation / proposed expansion OpenUSD/Earth-2 foundation and strict
observation/simulation separation; full twin
remains future work.


---

P.E.L.A.P.H. Architecture White Paper | Draft 1.2 | September 2026 | 4
Area Status Scope
Helix Active development Controlled engineering environment and specialist
handoff integration.
Eagle Eye Prototype / active development Observer and prompt/security boundary work.
Cloud infrastructure Exploratory Potential governed cloud testing, workstations,
elastic compute and hosted runtime capacity.
12. What P.E.L.A.P.H. Is Not
• It is not a claim that planetary hazards can be predicted with certainty.
• It is not a replacement for scientific agencies, emergency managers, domain experts, or public authorities.
• It is not an architecture in which a language model can silently convert its own inference into real-world authority.
• It is not dependent on a single AI model, cloud provider, scientific data provider, or visualization platform.
• It is not intended to blur observed history with synthetic or predicted state.
13. Development Roadmap
Phase I - Evidence foundation - Expand and validate live-source adapters, provenance, scoring, time semantics and
planetary-boundary snapshots.
Phase II - Authority - Complete E.M.M.A. Admission so evidence and cascade activation cannot mutate governed state without an
explicit authority decision.
Phase III - Twin Earth - Define simulation state, OpenUSD representation, synchronization, scenario branching, uncertainty and Earth-2
integration.
Phase IV - Hazard intelligence - Build cross-domain hazard models, cascade reasoning, confidence handling, explanations and
validation against historical events.
Phase V - Governed response - Connect recommendations to bounded workflows, human decision points, infrastructure resources and
verified execution.
14. Research Questions
• How should confidence propagate when multiple sources disagree or update at different rates?
• How can causal claims be distinguished from correlations in cross-domain cascade graphs?
• What admission rules are appropriate for different classes of state change?
• How should Twin Earth quantify and expose uncertainty across branching scenarios?
• Which hazard predictions can be validated prospectively and which require retrospective benchmarking?
• How can a human audit complex multi-model reasoning without requiring access to private model internals?
• How should compute, latency, privacy, energy use and monetary cost participate in resource selection?
15. Conclusion
P.E.L.A.P.H. proposes a planetary intelligence architecture in which better prediction is inseparable from better evidence discipline and
better governance. Its central architectural choice is to keep observation, inference, simulation, authority, execution and verification
distinct enough to audit while allowing them to cooperate as one system.
Lucy provides the operating intelligence. E.M.M.A. provides the authority boundary. Live Earth provides the evidence fabric. Twin Earth
provides the simulation space. Helix and specialist systems provide bounded capability. Together, these components define a path
toward planetary-scale analysis and hazard intelligence without making autonomy synonymous with authority.
Document Note
Draft status: This document describes an evolving research and engineering architecture as of September 2026. Terms, subsystem
boundaries, implementation details and validation results may change as development continues. Capabilities identified as proposed,
exploratory, foundation, prototype, or active development should not be interpreted as production-deployed guarantees.


---

P.E.L.A.P.H. Architecture White Paper | Draft 1.2 | September 2026 | 5
Technical Specification Addendum - Draft 1.2
This addendum formalizes the architectural contracts that were intentionally left conceptual in Draft 1.0. The schemas below are
reference contracts: they define required semantics and boundaries without locking P.E.L.A.P.H. to a specific database, cloud, model
provider, transport, or serialization format.
A. Seven-Layer System Diagram
The seven named layers are shown as a governed information-and-action loop. The arrows describe intended responsibility flow, not
unrestricted trust or direct write authority.
1 LUCY Operating intelligence: intent, context, competency
selection, explanation and orchestration.
2 E.M.M.A. Governance and authority: admission, policy,
leases, approvals and bounded execution rights.
3 LIVE EARTH Time-stamped observed state: normalized external
evidence with provenance.
4 TWIN EARTH Simulation state: scenarios, forecasts,
counterfactuals and uncertainty-aware branches.
5 HELIX Controlled engineering/training workspace:
specialist builds, tests and experiments.
6 EAGLE EYE Independent observation/security function: detects
anomalies, boundary violations and suspicious
behavior.
7 DELTAVAULT Evidence ledger: append-oriented record of inputs,
decisions, executions, verification and lineage.
Primary flow: Live Earth -> Lucy/context and analytical competencies -> E.M.M.A. admission -> Twin Earth or governed execution ->
verification -> DeltaVault. Helix supplies bounded specialist work; Eagle Eye observes the boundaries and can raise evidence or
quarantine signals. DeltaVault is cross-cutting: every consequential stage should be reconstructable from its records.
B. Evidence Contract
Every datum eligible to influence governed state should be wrapped in an evidence envelope. Payload schemas may differ by domain,
but the envelope remains stable enough for provenance, scoring, replay and audit.
Field Type Required Meaning / rule
evidence_id UUID / content-addressed ID Yes Globally unique identity; immutable
after admission.
observed_at UTC timestamp Yes* When the source says the event/state
occurred. *For observations; null only
when genuinely unknowable.
ingested_at UTC timestamp Yes When P.E.L.A.P.H. received the
record.
source_id String / registry key Yes Stable identifier resolving to the
source registry.
source_uri URI or source locator When available Origin endpoint, dataset, sensor, file
or publication locator.
source_class Enum Yes sensor | agency | operator | model |
human | internal-derived | simulation.
evidence_class Enum Yes observed | derived | predicted |
simulated | hypothetical.
domain Enum/string Yes Examples: weather, wildfire, seismic,
hydrology, grid, health, ocean,
aviation.
geometry GeoJSON-like / grid reference When spatial Point, line, polygon, volume or
grid-cell reference.
value Typed payload Yes Domain-specific
measurement/event/state; must carry
units where applicable.


---

P.E.L.A.P.H. Architecture White Paper | Draft 1.2 | September 2026 | 6
Field Type Required Meaning / rule
units UCUM-like string When numeric Explicit physical or domain units; no
implicit unit conversion.
uncertainty 0..1 and/or distribution When estimable Quantified uncertainty; never silently
converted into certainty.
quality_score 0..1 Yes System quality estimate based on
source, freshness, completeness and
validation.
lineage List[evidence_id] Derived+ Parents used to calculate, predict or
simulate this record.
method_id String/version Derived+ Algorithm/model/rule and version
responsible for transformation.
integrity Hash/signature metadata Yes Supports tamper detection and
content verification.
admission_state Enum Yes raw | validated | admitted |
quarantined | rejected | superseded.
retention_class Enum/string Yes Retention and privacy handling
policy.
metadata Map<string, typed value> Optional Domain-specific annotations that
cannot override required fields.
Provenance Rules
• No source laundering: derived or predicted records retain links to their upstream evidence rather than presenting themselves as direct
observations.
• No class promotion: simulated, hypothetical or predicted values cannot be relabeled as observed because they later appear plausible.
• No silent mutation: admitted evidence is append-oriented. Corrections create a new record that supersedes the old record while
preserving both.
• Time is dual: observed_at and ingested_at remain distinct so delayed, replayed or backfilled feeds can be identified.
• Units and transformations are explicit: conversions record the method and source value.
• Conflicts are preserved: disagreement between credible sources is represented, scored and surfaced rather than overwritten by
last-write-wins behavior.
• Quarantine is evidence-preserving: suspicious data can be isolated without destroying the original record or its provenance.
• Replay must be deterministic where practical: a historical analysis should identify the exact evidence and method versions used.
C. Authority Decision Model
Authority is modeled as a five-stage chain. Passing one stage does not imply permission to skip the next.
Stage Decision responsibility Minimum artifact
1. Admission Validate identity, provenance, policy eligibility, task
context and requested capability.
AdmissionDecision: admit | quarantine | reject;
reasons; policy version.
2. Lease Issue narrowly scoped, time-limited authority for an
admitted task.
Lease: subject, capability, resources, constraints,
TTL, trust requirement, approval state.
3. Execution Executor performs only the operations covered by
the active lease.
ExecutionReceipt: executor, commands/actions,
inputs, timestamps, environment and exit/result
state.
4. Verification Independently test whether the intended effect
occurred and boundaries were respected.
VerificationRecord: checks, evidence, pass |
partial | fail, residual risk.
5. Ledger Append the complete decision and outcome chain
to DeltaVault.
LedgerRecord linking request -> admission ->
lease -> execution -> verification.
Fail-closed rule: missing, expired, mismatched or unverifiable authority does not become implicit approval. A new request or
re-admission is required when scope materially changes.


---

P.E.L.A.P.H. Architecture White Paper | Draft 1.2 | September 2026 | 7
D. Minimal Twin Earth State Model
Twin Earth is modeled as a versioned set of spatial-temporal cells plus branch metadata. The model is intentionally minimal so different
simulators can participate without redefining the system of record.
Field Type Rule
twin_state_id UUID/hash Identity of an immutable Twin Earth snapshot.
parent_state_id UUID/hash/null Immediate ancestor; null only for a root snapshot.
branch_id String/UUID Scenario branch identity.
scenario_type Enum baseline | forecast | intervention | counterfactual |
stress-test.
valid_time UTC timestamp/range Time represented by this state.
grid_spec Object Coordinate reference system, extent, tiling/index
scheme and vertical dimension if used.
resolution Object Spatial and temporal resolution; may vary by layer
and region.
cells Map[cell_id, state vector] Variables for each represented cell; sparse
representation permitted.
uncertainty Per-variable distribution/range Uncertainty is first-class and propagates through
transformations.
evidence_basis List[evidence_id] Observed/derived evidence used to initialize or
constrain the state.
model_basis List[method_id/version] Models and parameter sets used to evolve the
state.
branch_assumptions Typed map Explicit assumptions/interventions unique to the
branch.
confidence_summary Structured score/distribution Summary only; cannot replace variable-level
uncertainty.
Branching rule: a scenario forks from an identified parent state. It may evolve independently but cannot overwrite its parent or Live Earth
history. Promotion from a Twin Earth result into a real-world recommendation requires a new authority decision and retains the
originating branch, model versions and uncertainty.
E. Threat Model
Threat Failure mode Primary controls
Prompt/tool misuse A user, agent or compromised integration attempts
actions beyond intended scope.
Typed capabilities; E.M.M.A. admission;
least-privilege leases; human confirmation for
consequential actions; sandboxing; audit.
Model hallucination A model invents a source, event, causal link or
confidence.
Evidence-required claims; source IDs; class
separation; verification; refusal to promote
unsupported inference into observed state.
Cascade error A wrong dependency or amplified signal
propagates across domains and creates false
hazard escalation.
Bounded cascade depth/weights; uncertainty
propagation; multi-source corroboration; circuit
breakers; replay; human review at high
consequence thresholds.
Corrupted/poisoned source Feed is compromised, spoofed, stale or
systematically biased.
Integrity checks; source registry; freshness rules;
cross-source comparison; anomaly detection;
quarantine; source revocation without deleting
history.
Simulation leakage Predicted/simulated state is accidentally treated as
real observation.
Hard evidence-class boundary; separate
stores/namespaces; explicit branch IDs; admission
checks blocking synthetic-to-observed promotion.
Privilege escalation Worker or specialist attempts to expand its own
authority.
Workers cannot self-issue leases; server-side
authority source; TTL; capability binding;
independent verification.
Replay/stale authority Old approval or lease is reused after conditions
change.
Nonce/correlation identity; expiration;
task/resource binding; re-admission on material
scope change.


---

P.E.L.A.P.H. Architecture White Paper | Draft 1.2 | September 2026 | 8
Threat Failure mode Primary controls
Ledger tampering Evidence or decision history is modified after the
fact.
Append-oriented records; integrity
hashes/signatures; cross-record linkage; protected
backups/replication; anomaly alerts.
Resource exhaustion Bad workload consumes GPU, CPU, network,
storage or money.
Quotas; budget constraints; execution timeouts;
resource leases; monitoring; kill/quarantine paths.
F. Worked Architectural Examples
Scenario Evidence inputs P.E.L.A.P.H. behavior
Wildfire Satellite/fire feed reports a hotspot; weather
supplies wind/humidity; vegetation/drought context
adds fuel conditions.
Live Earth retains observations. A Twin Earth
branch estimates spread under multiple wind
scenarios. Lucy summarizes the evidence and
uncertainty. E.M.M.A. governs any outbound
notification or resource action. Verification checks
delivery/action; DeltaVault links the chain.
Flood Rainfall, radar, stream gauges, soil saturation and
forecast data indicate rising risk.
Conflicting gauges remain visible. Derived basin
state cites its parents. Twin Earth evaluates
inundation scenarios at declared resolution.
Hazard output remains a prediction until confirmed
by observation.
Grid failure Grid telemetry shows frequency/voltage anomalies
while weather and wildfire data indicate external
stress.
Cascade logic may connect environmental stress
to infrastructure risk, but causal claims require
evidence. Any proposed load-management or
external action requires a scoped lease; execution
and resulting telemetry are verified.
Volcanic activity Seismic swarms, deformation, gas measurements
and agency bulletins change over time.
P.E.L.A.P.H. fuses time-aligned evidence without
replacing the volcanological authority. Twin Earth
can test plume/ash scenarios; uncertainty and
model assumptions remain explicit. Public-safety
recommendations are presented as decision
support, not autonomous scientific authority.
G. Architectural Glossary
Term Definition
Admission Governance decision determining whether a request, evidence item or state
transition is eligible to proceed.
Authority Explicit permission to perform a bounded action; distinct from technical
capability.
Cascade A modeled dependency through which a change in one variable/domain can
influence another.
Competency A named, bounded ability Lucy can select for a task.
DeltaVault Append-oriented evidence and accountability ledger for decisions, actions
and verification.
Eagle Eye Independent observer/security function that detects and records anomalies or
boundary violations.
E.M.M.A. Enhanced Machine Mind Architecture; governance kernel and authority
boundary.
Evidence envelope Standard metadata and provenance wrapper around an observation,
derivation, prediction or simulation result.
Helix Controlled environment for engineering, training, testing and specialist work.
Lease Short-lived, scoped authorization granting a specific executor defined
capabilities and constraints.
Live Earth Read-only conceptual fabric of time-stamped observed
planetary/infrastructure state.
Lucy Operating intelligence/persona that interprets intent, coordinates
competencies and explains system results.


---

P.E.L.A.P.H. Architecture White Paper | Draft 1.2 | September 2026 | 9
Term Definition
P.E.L.A.P.H. Planetary Ecosystem Layer for Analysis, Prediction & Hazards; parent
architecture.
Provenance Traceable origin and transformation history of evidence.
Twin Earth Versioned simulation/counterfactual environment derived from evidence but
kept distinct from observed history.
Verification Independent or separately reasoned check that an execution produced the
intended bounded result.
Draft 1.2 note: The contracts in this addendum are architectural specifications, not claims that every field, control or workflow is already
production-implemented. They are intended to guide implementation and later validation while preserving provider and storage
independence.
H. Formal Cascade Graph Specification
The Cascade Graph is a bounded, typed dependency graph used to evaluate whether admitted evidence may justify additional
analytical work. It is not an unrestricted causal engine. A cascade edge expresses a declared relationship that can activate evaluation; it
does not, by itself, prove causation or authorize execution.
Node type Purpose Examples
OBSERVATION Admitted measured/reported evidence. River gauge, PM2.5 sensor, seismic event
DERIVED_STATE Deterministic or declared-method transformation of
evidence.
Soil-moisture anomaly, rolling load margin
BOUNDARY_VARIABLE Planetary-boundary control-variable state. Atmospheric CO2, green-water deviation
HAZARD Potential damaging condition requiring
assessment.
Flood, wildfire spread, ash plume
INFRASTRUCTURE Physical or digital system whose state may affect
risk.
Grid region, hospital, transport corridor
COMPETENCY Lucy capability eligible to evaluate a typed
problem.
Hydrology, wildfire, grid reliability
DECISION_GATE Explicit point requiring E.M.M.A.
admission/authority.
Escalation, simulation, external execution
Edge semantics
Edge Meaning Permitted effect
SUPPORTS Source node adds evidence for evaluating target. Raises evidentiary support; never grants authority.
CONTRADICTS Source conflicts with target state or hypothesis. Reduces confidence or forces review.
DEPENDS_ON Target cannot be evaluated without source
class/state.
Blocks evaluation when prerequisite absent.
INFLUENCES Declared directional relationship without claiming
deterministic causality.
Allows bounded propagation.
CORRELATES_WITH Observed association; explicitly non-causal. May trigger analysis only.
TRIGGERS_CHECK Threshold/state requires evaluation of target. Schedules/activates a bounded check.
MITIGATES / AMPLIFIES Source is modeled to decrease/increase target
risk.
Adjusts modeled risk only with declared
model/version.
Confidence propagation
Each traversed edge carries an edge confidence c_e in [0,1], a provenance class, and an optional model/version. A candidate path
confidence is the product of the admitted source confidence and traversed edge confidences, multiplied by freshness and applicability
factors. Multiple independent paths may be combined only by a declared aggregation rule; they are not assumed independent by
default. Contradictory evidence must be retained and may lower confidence or force human/domain review. Confidence never increases
merely because a graph contains more hops.
Default conservative rule: C_path = C_source × Π(c_edge × freshness × applicability). The production implementation may substitute
calibrated domain models, but the rule and model version must be recorded in the evidence lineage.


---

P.E.L.A.P.H. Architecture White Paper | Draft 1.2 | September 2026 | 10
Bounded traversal and circuit breakers
• Default maximum cascade depth: 4 edges. A domain may request a lower limit; raising the limit requires an explicit policy/version.
• No node may be revisited within the same evaluation path. Cycles are detected and terminated.
• Maximum fan-out, total evaluated nodes, wall-clock time, and compute budget are lease-scoped resource limits.
• Stop propagation when path confidence falls below the domain minimum, evidence becomes stale, provenance is unresolved, or
required evidence is missing.
• Trip the circuit breaker on contradictory high-confidence observations, rapid confidence oscillation, abnormal fan-out, repeated source
failure, suspected source corruption, policy violation, or budget exhaustion.
• A tripped breaker freezes downstream state mutation, records the partial graph/evidence, and routes the case to E.M.M.A. for
quarantine, re-evaluation, or human review.
I. Planetary Boundary Control Variables
P.E.L.A.P.H. uses the planetary-boundaries framework as scientific context, not as a proprietary score. The working 13-variable
mapping below follows the 2023 framework interpretation used by the architecture. Because the scientific framework evolves, each
stored boundary snapshot must include framework/version metadata.
Boundary Control variable Representative unit/metric Spatial interpretation
Climate change Atmospheric CO2 concentration ppm Global
Climate change Radiative forcing / Earth energy
imbalance
W m^-2 Global
Biosphere integrity Genetic diversity / extinction rate E/MSY Global
Biosphere integrity Functional integrity / human
appropriation of net primary
production (HANPP)
% of potential NPP Global
Land-system change Forest cover remaining % of original forest cover Biome / global aggregate
Freshwater change Blue-water change / streamflow
deviation
% deviation from pre-industrial
variability
Basin / global aggregate
Freshwater change Green-water change / root-zone
soil-moisture deviation
% land area outside variability
envelope
Grid / global aggregate
Biogeochemical flows Anthropogenic nitrogen fixation /
reactive N flow
Tg N yr^-1 Global / regional
Biogeochemical flows Phosphorus flow Tg P yr^-1 Global ocean + regional freshwater
Ocean acidification Surface-ocean aragonite saturation
state
Omega arag relative to pre-industrial Global / ocean region
Atmospheric aerosol loading Aerosol optical depth /
interhemispheric aerosol loading
AOD / distribution metric Regional + global context
Stratospheric ozone depletion Stratospheric ozone concentration Dobson Units (DU) Global / latitude band
Novel entities Release/introduction of synthetic
substances; operational proxy: share
insufficiently assessed
Framework-defined proxy Global / category
J. Governed Execution Sandbox Specification
The execution sandbox is a disposable or tightly bounded environment for approved work. The sandbox is an enforcement mechanism
beneath E.M.M.A.; it is not an authority source.
Control Baseline requirement
Isolation model Separate workspace and process namespace; no implicit host filesystem
access; network disabled by default; explicit mount and network allowlists;
disposable execution identity.
Filesystem Read-only base image where practical; task-scoped writable workspace; host
paths denied unless explicitly leased; outputs exported through a controlled
handoff.


---

P.E.L.A.P.H. Architecture White Paper | Draft 1.2 | September 2026 | 11
Control Baseline requirement
Syscalls Default-deny or platform-equivalent syscall filtering. Permit only calls required
for ordinary computation/file I/O; deny raw device access, kernel/module
manipulation, ptrace of host processes, privileged mounts, and namespace
escape primitives unless a specialized lease explicitly requires them.
Privileges Non-root/non-administrator execution by default; no ambient credentials;
short-lived task credentials only.
Network Off by default. When permitted, destination/protocol/port are lease-scoped
and logged; unrestricted outbound access is not a baseline capability.
Resource caps Lease defines CPU, memory, process count, storage, wall-clock, GPU
allocation and network budget. Exceeding a hard cap terminates or pauses
the job.
Logging Append-oriented job record: ticket/lease IDs, image/environment identity,
command/tool invocation, timestamps, exit status, resource use, approved
network destinations, input/output hashes and verification result.
Secrets Injected only when explicitly required; redacted from normal logs; never
persisted into reusable images/workspaces.
Termination Lease expiry, policy violation, circuit breaker, resource breach, or explicit
revocation stops the job and preserves forensic metadata.
Platform-specific syscall profiles may differ between Linux, Windows Sandbox and future cloud runtimes. The invariant is capability
minimization plus auditable deviation: any relaxation from the baseline must be named in the lease.
K. Twin Earth to Live Earth Reconciliation Rules
Synthetic state is never promoted into Live Earth as an observation. Twin Earth may generate a candidate hypothesis, forecast,
anomaly target, or expected state. Live Earth changes only when new external evidence independently supports the real-world state
and that evidence passes admission.
Gate Minimum requirement
1. Candidate declaration Twin Earth output carries branch ID, model/version, assumptions, time
horizon, spatial resolution, uncertainty and complete evidence lineage.
2. External corroboration At least one authoritative or independently verifiable real-world observation
supports the candidate. Safety-critical domains should require multiple
independent sources when feasible.
3. Temporal/spatial match Corroborating evidence must fall inside the candidate's declared time window
and spatial applicability.
4. Uncertainty threshold No universal numeric threshold is hard-coded. Each domain policy defines
maximum uncertainty/minimum confidence before automatic admission is
even eligible. Missing calibration blocks automatic admission.
5. Conflict check Search for contradictory admitted observations. Material conflict blocks
automatic reconciliation and triggers review.
6. Source/integrity verification Validate source identity, freshness, integrity/hash/signature where available,
units, coordinate/time normalization and provenance chain.
7. E.M.M.A. admission E.M.M.A. evaluates evidence and policy. Twin Earth confidence is supporting
context, never the sole admission basis.
8. Live Earth write Only the newly corroborated observation/derived state is written. The original
simulation remains separately classified and linked as prior predictive
evidence.
9. Post-write verification Re-read resulting state, verify lineage/classification, and record the decision
plus before/after state in DeltaVault.
For safety-critical hazards, a domain can require human confirmation even when all quantitative thresholds are met. A failed or
indeterminate gate leaves Live Earth unchanged.
L. Lucy Competency Contract
A competency is a typed, bounded capability that Lucy may select to perform analysis or propose work. Competency registration
describes what a capability can do; it does not grant permission to execute consequential actions.


---

P.E.L.A.P.H. Architecture White Paper | Draft 1.2 | September 2026 | 12
Field Type Contract meaning
competency_id string Stable unique key, e.g.
wildfire.spread_assessment.
version semver/string Implementation/contract version.
owner string Responsible subsystem/provider.
inputs typed schema Accepted evidence/context classes and required
fields.
outputs typed schema Permitted result/proposal classes.
domains set[string] Declared subject domains.
capabilities set[string] Specific operations the competency may perform.
prohibited_actions set[string] Explicitly disallowed operations.
evidence_requirements policy reference Minimum provenance, freshness and confidence
requirements.
trust_tier enum/policy Minimum trust/verification level required to invoke.
execution_class enum READ_ONLY, ANALYSIS, SIMULATION,
PROPOSE_ACTION, or EXECUTE_GOVERNED.
resource_profile object Expected CPU/GPU/memory/network/tool needs.
authority_requirement policy reference Required E.M.M.A. admission/lease class.
verification_contract policy/schema How outputs are checked before acceptance.
fallbacks list[competency_id] Eligible alternatives when unavailable or
disqualified.
Invocation rules
• Lucy resolves the user/task intent to one or more competency keys through the competency graph; provider identity is secondary to
competency eligibility.
• A competency is eligible only when input schema, domain, trust tier, evidence requirements, mode/task identity and resource
requirements are satisfied.
• READ_ONLY and ANALYSIS competencies may operate under lower-risk policies; SIMULATION, PROPOSE_ACTION and
EXECUTE_GOVERNED require progressively stronger authority and verification.
• Competencies receive a task-scoped context package/lease, not unrestricted global memory or authority.
• Specialists return typed results or proposals to Lucy. They do not directly confer with one another outside governed orchestration and
do not write durable memory merely because they produced an output.
• If multiple competencies qualify, Lucy's arbitration records the candidates and selection rationale. Cost, latency and provider availability
may break ties only after safety, trust and capability requirements are met.
• Failure, low confidence, schema mismatch, trust degradation or verification failure causes fallback, escalation or abstention; it must not
silently widen the competency's authority.
Draft 1.2 Engineering Note
The numerical defaults in this draft (including cascade depth) are conservative starting policies, not immutable constants. They are
intended to be versioned, tested and calibrated by domain. Scientific control-variable definitions and thresholds must likewise carry
framework/version metadata so P.E.L.A.P.H. can adopt future peer-reviewed revisions without rewriting historical snapshots.
