# AETHERIA Security Platform

**Security Architecture, Eagle Eye, Active Defense, Implementation Evidence, and the Helix Sandbox Relationship — Version 1.1**

**Author:** Randy Webb  
**Status:** Research / white-paper text edition  

> This GitHub edition is a text transcription of the authored paper. Layout, figures, tables, pagination, and typography may differ from the formatted PDF edition.

---



---

Eagle Eye Security Platform V1 | Lucy AIOS Technical White Paper
TECHNICAL WHITE PAPER
AETHERIA
Adaptive Ecosystem Topology & Hazard Response Infrastructure Agent
Security Architecture, Eagle Eye Agent, Active Defense, Implementation Evidence, and the Helix
Sandbox Relationship
Lucy AIOS Project
Version 1.1 | September 2026
Evidence note: Gate 1 and Gate 2 results in this paper are internal engineering validation results,
not independent third-party certification.


---

Eagle Eye Security Platform V1 | Lucy AIOS Technical White Paper
Abstract
AETHERIA is a security architecture for a local-first agentic AI operating system in which the AI is 
allowed to act, learn, and experiment without turning security into a universal approval 
bottleneck. The design separates human authority, AI work, security, resource management, and 
evidence recording. AETHERIA occupies the security plane; Eagle Eye is the active security agent 
inside that platform, responsible for observation, detection, correlation, integrity awareness, and 
the security context used by later defensive response. The current implementation continuously 
observes host processes, network state, protected-resource integrity, and selected runtime events 
while preserving evidence without becoming the owner of Lucy's goals.
The paper presents the motivation for this separation, the threat model, the relationship between 
AETHERIA, Eagle Eye, and the Helix build/train/test sandbox, and internal validation results from 
the first two Eagle Eye implementation gates. It also defines AETHERIA's active-defense concept: 
evidence-based handshake state, bounded defensive probe workers, controlled decoys, 
containment, and diversion into isolated deception environments under the defender's control. 
The current implementation has demonstrated bounded RuntimeHost participation, real Windows 
process and socket observation, protected-file SHA-256 integrity checks, truthful sensor-failure 
reporting, bounded recent-event history, and durable evidence joins. Active defense, router-level 
telemetry, prompt-security correlation, and full Helix integration remain staged future work.
1. Why Agentic AI Needs a Separate Security Plane
A conversational model can be treated primarily as an information system. An agentic operating 
system cannot. Once an AI can invoke tools, create processes, manipulate files, use network 
connectors, start sandboxes, generate executable artifacts, or initiate self-directed experiments, 
language becomes connected to effects. Security therefore has to reason about more than text: it 
must understand processes, resources, network behavior, provenance, execution scope, and the 
boundary between observation and authority.
Traditional perimeter-only assumptions are insufficient for this environment. NIST Zero Trust 
Architecture explicitly rejects implicit trust based only on network location or ownership and 
shifts attention toward protecting resources, identities, services, and workflows. [2]
NIST Cybersecurity Framework 2.0 similarly treats cybersecurity as an organization-wide risk￾management problem rather than a single technical control, organizing outcomes across Govern, 
Identify, Protect, Detect, Respond, and Recover. [1]
AETHERIA applies those ideas to a local agentic system while adding an AI-specific distinction: 
security should protect autonomy without becoming the authority that continuously re-issues 
permission for already-authorized work. Eagle Eye serves as the active security agent within that 
system.


---

Eagle Eye Security Platform V1 | Lucy AIOS Technical White Paper
2. Role Separation
Human = Governor / source of production authority
Lucy = Intelligence and agentic worker
AETHERIA = Security system / defensive security platform
Eagle Eye = Active security observation, detection, and correlation agent
EMMA = Evidence, provenance, and integrity record
R1 = Cognitive and compute resource management
Helix = Isolated build / train / test / experiment environment
This split is central to the architecture. AETHERIA can enforce a sandbox boundary without 
deciding what Lucy should be trying to accomplish. Eagle Eye can observe and correlate suspicious
behavior without becoming the owner of the mission. An evidence subsystem can record an action 
without becoming a mandatory permission oracle. A resource manager can limit CPU or memory 
without silently changing the mission. The result is a system in which security boundaries remain 
meaningful while agentic work remains practical.
3. Design Principles
Human authority is persistent within scope. A human-authorized mission should not require re￾approval for every ordinary step already inside that mission.
Awareness is broader than authority. Lucy may observe system state read-only even when she is
not authorized to mutate it.
Security is not governance. AETHERIA protects runtime and system boundaries; Eagle Eye 
observes, detects, and correlates security-relevant behavior. Neither owns Lucy's goals.
Evidence is not approval. EMMA records who did what, why, and with what evidence; recorder 
failure should not automatically disable unrelated authorized work.
Prompts are inputs, not authority. Instructions from users, documents, webpages, models, 
plugins, or other agents retain provenance and cannot silently override active boundaries.
Sandbox autonomy is deliberately broader. Self-directed work may be allowed to build, test, 
retry, and fail inside Helix while promotion to production remains a separate boundary.
Unknown is not malicious. Novelty, suspicion, and confirmed compromise must remain distinct 
epistemic states.
No fabricated telemetry. Security dashboards must show measured data, explicit simulation 
labels, or unavailable states - never invented confidence or threat scores.
4. Threat Model
AETHERIA is designed around a mixed threat model in which risk can originate externally, 
internally, or accidentally. Eagle Eye provides the active observation and correlation layer. The 


---

Eagle Eye Security Platform V1 | Lucy AIOS Technical White Paper
objective is not to assume that every unusual event is an attack, but to preserve enough 
provenance and runtime evidence to distinguish normal variation from boundary-relevant 
behavior.
- External network activity: Unexpected inbound listeners, suspicious outbound destinations, 
unusual process-to-network relationships, or later router/gateway observations.
- Prompt and instruction manipulation: Direct or indirect instructions attempting to override 
mission scope, runtime ownership, sandbox restrictions, credential boundaries, or security 
controls. OWASP identifies prompt injection as a primary risk for LLM applications, including 
indirect injection through external content. [4]
- Compromised or unexpected local processes: Applications or child processes that create 
unanticipated listeners, network connections, persistence, or protected-file changes.
- Generated artifact risk: Scripts, binaries, archives, models, or installers produced by an 
agentic workflow that behave differently from their claimed purpose.
- Sandbox escape or scope expansion: Helix experiments or workers attempting to access host 
resources outside their assigned workspace or network posture.
- Credential exposure: Prompts, tools, logs, or generated code attempting to reveal API keys, 
tokens, private keys, cookies, or protected environment data.
- Telemetry deception: A subsystem reporting healthy, verified, or secure states that are 
synthetic, random, stale, or otherwise unsupported by evidence.
- Security-control impairment: Requests or runtime activity attempting to disable observation, 
evidence recording, sandboxing, or protective boundaries.
5. Architectural Model
 Internet / LAN
 |
 Future Perimeter Adapter
 |
 AETHERIA
 Security Platform/Core
 |
 EAGLE EYE
 Observation / Detection / Correlation
 / | \
 Windows WSL Helix
 Host Broker Sandbox
 \ | /
 Security Events
 / \
 Lucy EMMA
 understanding/action evidence


---

Eagle Eye Security Platform V1 | Lucy AIOS Technical White Paper
Future active-defense response remains inside AETHERIA; R1 supplies expected resource 
budgets across Lucy and Helix.
5.1 Security planes
Host plane: Windows process state, listening ports, network connections, WSL invocation, 
protected-file integrity, and later service/persistence observations.
Sandbox plane: Broker job lifecycle, process creation, denied paths, network posture, resource 
limits, artifact creation, and boundary-crossing attempts.
Integrity plane: Cryptographic hashing and provenance for critical Lucy, AETHERIA, Eagle Eye, 
broker, Helix, and generated artifacts.
Perimeter plane: A future adapter boundary for router, firewall, DNS, flow, or IDS telemetry. The 
core is intentionally vendor-neutral.
5.2 Event model
Security events are normalized before correlation. A meaningful event may carry sensor identity, 
timestamp, process and parent process identifiers, executable path, local/remote network 
coordinates, resource path, mission/run/experiment references, classification, severity, evidence 
references, and any response taken. Missing fields remain unknown rather than being filled with 
inferred values.
6. AETHERIA, Eagle Eye, and Helix: Security as an Enabler of Autonomy
Helix is the complementary half of the design. Rather than allowing self-directed experimentation 
directly against the production host, Helix provides a separate application and strict sandbox 
workspace in which Lucy can eventually build, test, train, simulate, retry, and create candidate 
capabilities. AETHERIA protects the environment; Eagle Eye observes the boundary and the effects.
Neither becomes the intelligence operating the lab.
Awake Lucy / human mission
 |
 v
 Helix
 |
 Sandbox Broker
 |
 build / test / train
 |
 AETHERIA / Eagle Eye observes
 |


---

Eagle Eye Security Platform V1 | Lucy AIOS Technical White Paper
 result / artifact / evidence
 / \
 Anchor candidate Garage Ticket
 \ /
 Human production decision
This architecture intentionally gives the sandbox more freedom than production. The security 
objective is not to make experimentation impossible; it is to make experimentation bounded, 
observable, attributable, and recoverable. CISA Secure by Design guidance emphasizes building 
security into the product and shifting security burden away from the end user. [3]
7. Active Defense: Adaptive Defensive Probing, Deception, and 
Containment
AETHERIA is intended to do more than raise alerts. Its active-defense concept is designed for 
situations in which inbound or internal behavior has become suspicious enough to justify 
controlled defensive interaction, but the evidence is not yet sufficient to treat every anomaly as a 
confirmed compromise. Eagle Eye supplies observation and correlation; AETHERIA supplies the 
defensive response framework.
The design follows a defensive-only rule: AETHERIA may shape, isolate, deny, redirect, and 
instrument resources inside infrastructure controlled by the system owner. It does not perform 
unauthorized access against an external system. This keeps the concept within defensive cyber 
operations and adversary-engagement principles rather than turning it into hack-back.
7.1 Evidence-Based Handshake State
Inbound and boundary-relevant activity begins as an evidence state, not a verdict. AETHERIA may 
represent the evolving assessment as Green, Amber, or Red. Green means behavior matches an 
expected service, authenticated peer, or known workload. Amber means behavior is unusual, 
incomplete, probing, or insufficiently explained. Red means the observed behavior has crossed a 
protected boundary or accumulated strong evidence of hostile intent. The state is derived from 
observations; it is never a random threat percentage.
State Meaning Typical defensive posture
GREEN Expected or sufficiently 
explained behavior
Observe normally
AMBER Unknown, unusual, or probing
behavior requiring more 
evidence
Increase observation; present 
controlled decoys where 
appropriate
RED Confirmed protected￾boundary violation or strongly
evidenced intrusion behavior
Contain, isolate, deny, or 
divert into an isolated 
deception environment


---

Eagle Eye Security Platform V1 | Lucy AIOS Technical White Paper
8. Implementation Status: Eagle Eye V1
AETHERIA is the broader security-system architecture; the currently implemented and verified 
runtime slice is the Eagle Eye agent foundation. The first two Eagle Eye implementation gates were 
completed on isolated feature branches against the Lucy AIOS canonical baseline. These results are
internal engineering validation and should not be interpreted as an external security certification 
or as proof that the full AETHERIA active-defense architecture is already operational.
Capability Status Evidence / Boundary
Gate 1 - Foundation VERIFIED in isolated tests Typed contracts, event core, 
Windows observation, 
protected-resource integrity, 
sensor health. Lucy read path 
and EMMA join were 
implemented/tested.
Gate 2 - RuntimeHost VERIFIED in isolated Windows
run
One bounded observer 
starts/stops with RuntimeHost;
process/network/listener/integ
rity transitions observed 
continuously; bounded event 
ring and meaningful EMMA 
join.
AETHERIA active defense DEFINED / NOT 
IMPLEMENTED
Handshake state, bounded 
defensive probes, decoys, 
containment, and diversion 
are architectural targets; no 
claim of deployed active 
deception or automated 
containment today.
Prompt/boundary security PLANNED NEXT Provenance-aware prompt 
security, runtime ownership 
conflicts, sandbox escape 
requests, credential risk, and 
prompt-injection 
observations.
Router/perimeter adapter FUTURE Interface planned; no claim of
router-level visibility today.
Helix security integration FUTURE Helix stable recovery baseline 
exists; full 
AETHERIA/Eagle/Broker/R1 


---

Eagle Eye Security Platform V1 | Lucy AIOS Technical White Paper
integration is not yet 
complete.
9. Internal Validation Evidence
9.1 Gate 1
Gate 1 committed the Eagle Eye foundation on a feature branch without modifying canonical Lucy.
Internal verification included 26 targeted tests and three subtests. The implementation observed a 
real Python child process by PID, a real localhost listener and connection with owning PID, a 
disposable file moving through SHA-256 match -> mismatch -> match states, and a forced sensor 
failure reported as OFFLINE. The existing Lucy capability dispatcher returned structured Eagle Eye
status, and a real integrity event was joined to a temporary EMMA ledger.
9.2 Gate 2
Gate 2 integrated one bounded observer with an isolated RuntimeHost and added continuous 
observation. The implementation detected process and network transitions, listener open/close, 
and changes to explicitly registered protected files. A 100-event in-memory ring provided filtered 
read-only history while unchanged state was deduplicated. Meaningful events joined the existing 
EMMA ledger, and listener evidence was capped per poll to bound evidence volume.
The live proof included a harmless child process, localhost connection, listener opening and 
closing, and protected-file mismatch/restoration. A forced sensor failure reported OFFLINE while 
RuntimeHost remained running. At the shipped five-second cadence, the Eagle observer thread 
consumed 0.71% CPU over an 11-second measurement window. Forty-seven tests, thirteen subtests,
and a standalone live proof passed for the gate.
Evidence-honesty note: the governed result's independent verified field remained null during the 
live Gate 2 proof. The gate was therefore described as verified by separate live assertions rather 
than rewriting that field or treating it as positive evidence.
10. Prompt Security as a Security Sensor
The next planned Eagle Eye gate extends security from runtime effects back to the instruction 
source. This is not intended to create a generic censorship filter. The design goal is to preserve 
provenance and detect when an instruction attempts to cross an already-established boundary.
Instruction
 |
 v
Prompt Security Sensor
 |
 +-- source provenance
 +-- requested capability/resource


---

Eagle Eye Security Platform V1 | Lucy AIOS Technical White Paper
 +-- active mission/runtime owner
 +-- affected boundary
 |
 v
Security classification
 |
 +-- NORMAL
 +-- UNTRUSTED_INSTRUCTION
 +-- BOUNDARY_CROSSING
 +-- RUNTIME_OWNERSHIP_CONFLICT
 +-- SANDBOX_ESCAPE_REQUEST
 +-- CREDENTIAL_RISK
 +-- SECURITY_OVERRIDE_ATTEMPT
 +-- PROMPT_INJECTION_SUSPECTED
This direction aligns with the practical risk described by OWASP: model behavior can be 
manipulated not only by direct user prompts but also by external content such as webpages or 
files. [4]
The architectural response is provenance plus boundary correlation rather than trust-by-text. A 
prompt may be syntactically valid while still conflicting with runtime ownership, mission scope, a 
credential boundary, or a sandbox boundary.
11. Alignment with Established Security Guidance
Reference AETHERIA relationship Citation
NIST CSF 2.0 AETHERIA / Eagle Eye 
primarily supports Detect and 
Protect outcomes, supplies 
evidence relevant to 
Govern/Respond, and 
preserves recoverability as a 
design constraint.
[1]
NIST SP 800-207 Zero Trust No implicit trust based solely 
on local placement, 
application ownership, or 
network location; resources 
and workflows remain 
bounded.
[2]
CISA Secure by Design Security is built into the 
architecture and stable 
defaults rather than delegated
entirely to the user. Evidence 
[3]


---

Eagle Eye Security Platform V1 | Lucy AIOS Technical White Paper
honesty supports 
transparency/accountability.
OWASP GenAI - Prompt 
Injection
Prompt provenance and 
boundary detection address 
direct and indirect instruction
manipulation without treating
all unusual text as malicious.
[4]
MITRE ATT&CK Process/network/integrity 
telemetry can later support 
defensive mapping across 
execution, persistence, 
credential access, command￾and-control, exfiltration, and 
impact categories.
[5]
MITRE Engage Supports the active-defense 
design rationale for defensive 
denial, deception, controlled 
adversary engagement, 
hypothesis testing, and 
learning from hostile behavior
without requiring hack-back.
[6]
NIST cyber-deception 
terminology
NIST defines misdirection as 
maintaining deception 
resources or environments 
and directing adversary 
activities toward them; this 
closely matches AETHERIA's 
controlled decoy and 
diversion concept.
[7]
7.2 Adaptive Defensive Probing
When activity remains in an Amber state, Eagle Eye may request small, bounded defensive probe 
workers (internally described as mini-probers). These workers do not attack the remote system. 
They operate only inside defender-controlled surfaces and ask narrow questions through 
controlled decoys: What resource is the interaction seeking? Does it follow a decoy path? Does it 
enumerate services? Does it interact with inert credential-shaped artifacts? Does it attempt to move
beyond the originally contacted surface?
Each defensive probe is disposable and narrowly scoped. It receives a specific question, a short 
lifetime, no genuine sensitive data, no authority to leave the controlled defensive environment, 
and a complete evidence trail. Multiple probes may independently test file, authentication, service-


---

Eagle Eye Security Platform V1 | Lucy AIOS Technical White Paper
enumeration, or network hypotheses; their results are merged by Eagle Eye as evidence rather 
than treated as independent authorities.
7.3 Controlled Decoys and Misdirection
AETHERIA may expose decoy directories, synthetic service descriptions, inert credentials, 
fabricated configuration, or other non-production resources when doing so can help distinguish 
ordinary behavior from deliberate probing. This is defensive deception: real assets remain 
concealed while the suspicious interaction is given controlled opportunities to reveal what it is 
trying to reach. NIST uses the term misdirection for maintaining deception resources or 
environments and directing adversary activity toward them. [7]
MITRE Engage similarly describes cyber denial and deception as defensive techniques that can 
increase uncertainty for an adversary while helping defenders expose activity, elicit intelligence 
about tactics and techniques, test hypotheses, and improve threat models. [6]
The historical internal design lineage for this adaptive deception concept was informally called the 
'Pandora Maze.' In the public AETHERIA architecture, the formal name is Active Deception & 
Containment. The historical codename is retained only as design lineage, not as a separate product 
name.
7.4 Confirmation Through Behavior
AETHERIA should prefer behavioral confirmation over assumption. A single unusual packet, 
process, or request may justify observation but not a hostile verdict. Confidence rises when 
independent evidence accumulates: service enumeration, repeated protected-path probes, 
interaction with credential decoys, privilege-oriented behavior, persistence attempts, or attempts 
to reach resources unrelated to the legitimate session. The evidence remains inspectable so an 
operator can understand why the state changed.
If behavior is clearly dangerous, containment takes priority over further probing. AETHERIA does 
not need to continue an experiment merely to obtain a higher confidence score. The design 
principle is contain first when the protected boundary is clearly at risk, then investigate safely 
afterward.
7.5 Isolation and Diversion
Once behavior is confirmed as sufficiently risky, AETHERIA may deny the specific action, isolate 
the affected workload, or divert the interaction away from production into a fully instrumented 
deception environment. Such an environment may contain synthetic filesystem structures, decoy 
services, disposable workloads, inert credential material, fabricated application state, and 
controlled network topology. The objective is to keep real Lucy, EMMA, credentials, production 
files, and services outside the presented attack surface while collecting forensic evidence about 
what the interaction attempted to discover or access.
This creates a defensive progression: observe -> probe -> accumulate evidence -> contain -> 
isolate/divert -> analyze. The progression is not mandatory in every incident; AETHERIA may skip 
directly to containment when the evidence already establishes a critical boundary violation.


---

Eagle Eye Security Platform V1 | Lucy AIOS Technical White Paper
7.6 Analysis, Learning, and Evidence
Eagle Eye analyzes what the contained interaction searched for, enumerated, attempted to execute,
or tried to persist. AETHERIA can summarize likely defensive objectives such as credential 
discovery, service enumeration, configuration discovery, persistence attempts, or lateral 
movement patterns. EMMA preserves the lineage from initial observation through handshake 
transitions, defensive probes, containment, and final outcome. Sanitized evidence may later 
become a Lucy curiosity event or a Helix security experiment used to reproduce the behavior and 
test a mitigation without exposing the attacker to Helix itself.
7.7 Current Implementation Boundary
The active-defense architecture described above is a design target, not a claim about the current 
deployed runtime. As of Eagle Eye Gate 2, real host observation, continuous bounded monitoring, 
protected-resource integrity, sensor health, recent-event buffering, Lucy read access, and EMMA 
evidence joins have been internally verified. Adaptive mini-probers, automated inbound diversion,
dynamic decoy filesystems, active deception environments, router-level traffic redirection, and 
automated containment remain future AETHERIA work. Existing sandbox denials must not be 
relabeled as a fully implemented active-defense runtime until those connections are built and 
verified.
12. What AETHERIA Is Not
- A substitute for human authority.
- A mandatory approval gateway for every Lucy action.
- A claim that every unusual event is malicious.
- A router-level IDS today.
- A malware-classification engine today.
- A claim that adaptive deception, containment, or diversion is fully implemented today.
- A security dashboard whose visual appearance is treated as proof.
- Independent certification of Lucy AIOS security.
13. Current Limitations
- The current continuous observer uses a polling cadence; sufficiently short-lived activity 
between polls can be missed.
- No production dashboard conversation was exercised in Gate 2.
- AETHERIA active defense - including adaptive probing, decoy interaction, isolation/diversion, 
and automated containment - is defined architecturally but is not yet implemented in the 
verified Gate 2 runtime.
- Router/gateway telemetry is not yet connected.
- Prompt and boundary security is planned but not yet part of the verified Gate 2 baseline.
- Full Helix/Broker/R1/Eagle integration remains future work.


---

Eagle Eye Security Platform V1 | Lucy AIOS Technical White Paper
- Helix recovery is stable as a local read-only application baseline, but outbound-network 
isolation has not yet been independently proven.
- The implementation evidence is project-internal; no external penetration test, third-party code 
audit, or formal certification is claimed.
14. Roadmap
1. Gate 3 - Prompt and Boundary Security: Instruction provenance, runtime ownership conflicts, 
sandbox escape requests, credential risk, security-override attempts, and minimal runtime 
correlation.
2. Helix V2 Integration: Connect Lucy, R1 budgets, Governed Sandbox Broker, Eagle Eye events, 
and EMMA evidence while preserving Helix as a separate sandbox application operated by the 
same Lucy.
3. AETHERIA Active Defense Foundation: Define evidence-backed Green/Amber/Red handshake 
state, bounded defensive-probe contracts, decoy-resource contracts, containment policy, and 
explicit no-hack-back boundaries before enabling automatic response.
4. Perimeter Adapter: Add the first real router/firewall/gateway adapter using the same 
normalized event model.
5. Baseline and Correlation: Build historical baselines and multi-sensor correlation without 
collapsing novelty into threat.
6. Active Deception & Containment: After the foundation is stable, implement isolated decoy 
environments, defensive misdirection, bounded diversion, richer artifact analysis, and evidence￾driven containment without extending activity beyond defender-controlled infrastructure.
15. Discussion
The central engineering tension in agentic AI is not simply autonomy versus safety. It is where 
each kind of authority belongs. A system that requires a universal approval hop for every low-level
action may be safe in the narrow sense that it does little, but it also destroys the operational 
continuity that makes an agent useful. Conversely, a system that gives an AI broad, unobservable 
production access has no reliable way to distinguish intended autonomy from error, prompt 
manipulation, compromised dependencies, or boundary escape.
AETHERIA approaches the problem by making security a separate, evidence-driven plane. Eagle 
Eye provides the active observation and correlation agent inside that plane. Lucy can continue to 
reason and work within human-authorized scope; AETHERIA can independently protect hard 
technical boundaries; and EMMA can preserve what occurred. Helix then provides a place where 
autonomy can be broader because the blast radius is intentionally constrained.


---

Eagle Eye Security Platform V1 | Lucy AIOS Technical White Paper
This separation does not eliminate security risk. It creates a structure in which risk can be 
measured, attributed, tested, and improved without turning every subsystem into a competing 
authority.
16. Conclusion
AETHERIA is being developed as the security foundation for a local agentic AI system, with Eagle 
Eye serving as its active security agent rather than as a replacement for human control. Its defining
architectural decision is separation of concerns: human authority, AI work, security, resource 
management, evidence, and sandbox experimentation remain distinct but connected. The first two 
Eagle Eye implementation gates demonstrate that part of this separation can be made operational: 
real host observations can participate in the AI runtime, remain bounded, join durable evidence, 
fail visibly, and shut down cleanly without taking over the mission-control path.
The next challenge is to extend that same evidence discipline to instructions themselves, carry the 
security plane into Helix, and then build the active-defense layers described here: evidence-based 
handshake state, bounded defensive probes, controlled decoys, containment, and isolated 
diversion. The intended end state is straightforward: security that protects autonomy, learns from 
hostile behavior inside controlled boundaries, and never confuses defensive response with 
ownership of Lucy's goals.
References
[1] National Institute of Standards and Technology (NIST). The NIST Cybersecurity Framework 
(CSF) 2.0. CSWP 29, 2024. Source
[2] Rose, S., Borchert, O., Mitchell, S., and Connelly, S. Zero Trust Architecture. NIST SP 800-207, 
2020. Source
[3] Cybersecurity and Infrastructure Security Agency (CISA) et al. Shifting the Balance of 
Cybersecurity Risk: Principles and Approaches for Security-by-Design and -Default. Source
[4] OWASP GenAI Security Project. LLM01:2025 Prompt Injection. Source
[5] MITRE. ATT&CK Enterprise Matrix. Source
[6] MITRE. A Practical Guide to Adversary Engagement. Engage Handbook v1.0, 2022. 
https://engage.mitre.org/
[7] National Institute of Standards and Technology (NIST). "Misdirection" cybersecurity glossary 
entry, sourced to NIST SP 800-172r3. https://csrc.nist.gov/glossary/term/misdirection
Appendix A - Current Evidence Snapshot
- Canonical Lucy baseline used for Eagle V1 foundation work: reconcile/one-lucy at 
d26b1438a2ba15cfaf5e895bd25ca40ff5bc3fda.


---

Eagle Eye Security Platform V1 | Lucy AIOS Technical White Paper
- Eagle Eye Gate 1 foundation commit: b20332e68810c579c9079605a794f5194db7420d.
- Eagle Eye Gate 2 live RuntimeHost commit: ee1102cbeb61b9471fdde8dd3ab844062476f393.
- Gate 2 observer cadence: five seconds in the shipped isolated proof.
- Gate 2 measured observer CPU: 0.71% over an 11-second measurement window.
- Recent-event ring capacity: 100 events.
- Canonical branch remained unchanged during isolated Gate 1 and Gate 2 development.
Appendix B - Publication and Reproduction Note
This white paper describes an evolving engineering system. Commit identifiers and internal test 
counts are provided to make the implementation claims traceable within the Lucy AIOS project. 
Readers should distinguish AETHERIA architectural intent from the demonstrated Eagle Eye 
implementation status. Features explicitly labeled planned, future, missing, partial, unproven, or 
design-only - including active defensive probing, deception, isolation/diversion, and automated 
containment - are not represented as operational security controls.
