# Webb — AI and Planetary Boundaries

**Coupled Webb Pressure Equation / technological-transition framework — Model v0.1**

**Author:** Randy Webb  
**Status:** Research / white-paper text edition  

> This GitHub edition is a text transcription of the authored paper. Layout, figures, tables, pagination, and typography may differ from the formatted PDF edition.

---



---

Webb — AI and Planetary Boundaries | 1
Artificial Intelligence and Planetary Boundaries
A Coupled Pressure–Transition Model of Technological Growth Under Earth-System
Constraints
Randy Webb
Project: Lucy AI
September 2026
Contact: scottymicfree@gmail.com
Working manuscript for scholarly review and model calibration


---

Webb — AI and Planetary Boundaries | 2
Abstract
Artificial intelligence (AI) is typically analyzed as a computational, economic, or social technology, yet its 
continued expansion depends on physical infrastructures that consume electricity, freshwater, land, 
semiconductors, critical minerals, cooling capacity, and industrial materials. At the same time, current Earth￾system assessments identify seven of the nine planetary boundaries as transgressed, raising a central 
question: can rapid growth in computational infrastructure amplify existing biophysical pressures enough to 
constrain future technological development itself? This paper proposes a coupled pressure–transition 
framework for examining that question. A Kardashev-inspired technological-development state variable K 
evolves through a sustainability-constrained growth function, while a cumulative planetary-pressure variable 
P is constructed from normalized physical indicators. Net pressure is represented as the balance among 
industrial-material footprint H, technological externalities T, conflict-related ecological damage W, verified 
efficiency E, and verified ecological restoration R. Planetary pressure then feeds back into the effective 
technological transition rate. The framework does not assume that AI is inherently environmentally harmful 
or beneficial. Instead, it generates testable conditions under which AI-associated growth increases or reduces 
net pressure. The paper specifies a reproducible measurement architecture, distinguishes observed, derived, 
estimated, and scenario inputs, and requires sensitivity analysis across aggregation rules and alternative 
coupling functions. Rather than forecasting a predetermined collapse date, the framework is designed for 
scenario analysis, empirical calibration, and falsification.
Keywords: artificial intelligence; planetary boundaries; data centers; industrial ecology; Earth-system 
science; resource constraints; rebound effects; technological growth; sustainability; coupled systems
1. Introduction
Artificial intelligence is commonly described through the language of software, algorithms, models, and 
cloud services. Physically, however, AI depends on an industrial system composed of data centers, 
semiconductor fabrication, electric grids, transmission infrastructure, cooling systems, mineral extraction, 
chemical processing, and global supply chains. The environmental implications of AI therefore extend 
beyond the electricity consumed during model training or inference.
The relevance of this physical dependence is increasing rapidly. The International Energy Agency projects 
global data-center electricity consumption to rise from approximately 485 TWh in 2025 to around 950 TWh 
in 2030, or roughly 3% of global electricity demand, with AI-focused data centers growing substantially 
faster than the data-center sector as a whole. In the United States, Lawrence Berkeley National Laboratory 
estimates that data centers could account for 9.5%–15.3% of national electricity consumption by 2030 under 
its updated scenario range.
These infrastructure demands are expanding within an Earth system already under substantial anthropogenic 
pressure. The planetary-boundaries framework identifies critical Earth-system processes that regulate 
planetary stability. The 2026 Planetary Health Check reports that seven of the nine planetary boundaries are 
transgressed, confirming that the global Earth-system baseline remains outside the safe operating space 
across most assessed processes. The framework does not imply that crossing a boundary causes 
instantaneous collapse; rather, transgression indicates increasing risk of large-scale and potentially 
irreversible change.
This study does not attribute present planetary-boundary transgressions primarily to AI. Agriculture, fossil￾energy use, land conversion, industrial production, chemical pollution, and other human systems remain 
dominant historical drivers. Instead, the paper asks whether AI infrastructure is becoming an important 


---

Webb — AI and Planetary Boundaries | 3
marginal pressure multiplier within an already stressed Earth system, and whether that additional pressure 
can feed back into the material and institutional capacity required for further technological expansion.
1.1 Research Question
The central research question is: under what conditions does technological expansion increase planetary 
pressure faster than verified efficiency and restoration reduce it, and can sufficiently high pressure 
subsequently constrain the effective rate of technological development?
1.2 Contribution
The paper contributes a coupled civilization–planet model that links a Kardashev-inspired technological￾development variable to a cumulative pressure framework referred to here as the Webb pressure model. The 
contribution is not a new planetary boundary. Rather, it is a testable mathematical architecture for examining 
cross-boundary pressures generated by resource-intensive technological systems.
1.3 Scope of AI and Adjacent Digital Infrastructure
The framework focuses on AI because accelerated computing is currently a major driver of new data-center 
investment and load growth, but the physical accounting architecture is not inherently limited to AI. 
Conventional cloud services, cryptocurrency mining, high-performance computing, and other digital 
workloads can be represented using the same energy, water, material, land, and waste channels. For 
attribution, however, AI-specific results should be based only on loads or infrastructure that can be credibly 
assigned to AI workloads. Shared facilities should otherwise be reported as broader digital-infrastructure 
pressure, with AI treated as a disaggregated component only where workload-level evidence exists.
2. Planetary Boundaries and AI’s Industrial Metabolism
The planetary-boundaries framework provides a useful structure for organizing environmental pressures 
because it treats the Earth system as a set of interacting processes rather than as a collection of isolated 
pollutants. AI infrastructure can affect several of these processes simultaneously through energy use, water 
consumption, material extraction, land conversion, chemical use, and electronic waste.
Planetary boundary 2026 global status Illustrative AI-related pressure pathway
Climate change Transgressed Operational and embodied emissions; 
grid expansion
Biosphere integrity Transgressed Mining, land conversion, infrastructure 
fragmentation
Land-system change Transgressed Data centers, energy and transmission 
infrastructure, mining
Freshwater change Transgressed Cooling and semiconductor fabrication; 
basin-level stress
Biogeochemical flows Transgressed Mining/refining and industrial chemical 
pathways
Novel entities Transgressed Semiconductor chemicals, plastics, 
hazardous and electronic waste
Ocean acidification Transgressed Indirectly through additional CO2 
emissions
Atmospheric aerosol loading Within global safe space; strong regional Backup generation, construction, 


---

Webb — AI and Planetary Boundaries | 4
variation industrial combustion
Stratospheric ozone depletion Within safe operating space Limited direct pathway in current 
formulation
Table 1. Current global planetary-boundary status and illustrative pathways through which AI infrastructure may add pressure. 
Status reflects the 2026 Planetary Health Check; pathways are hypotheses to be quantified rather than assertions of dominant 
causation.
2.1 Energy and Grid Dependence
AI workloads depend on continuous electrical supply. The environmental effect of additional load depends 
not only on electricity quantity but also on location, timing, marginal generation, transmission constraints, 
and the pace at which new low-carbon generation and grid infrastructure can be deployed. For this reason, a 
megawatt-hour of AI load cannot be assigned a globally uniform climate impact.
2.2 Water
Data-center cooling and semiconductor fabrication create direct and indirect water demands. Water impacts 
are highly location dependent: the same volume consumed in a water-abundant region and in a stressed basin
can have very different ecological and social consequences. Existing literature also identifies persistent 
transparency gaps in facility-level water measurement, making water a strong candidate for regional rather 
than purely global modeling.
2.3 Materials, Semiconductor Fabrication, and Waste
Compute infrastructure depends on copper, aluminum, gallium, germanium, hafnium, silicon-related 
feedstocks, rare-earth elements, and other materials. The U.S. Geological Survey’s 2026 Mineral Commodity
Summaries documents production, trade, reserves, resources, and critical-mineral applications across more 
than 90 commodities. Semiconductor fabrication also uses fluorinated gases with high global-warming 
potential, while rapid hardware turnover contributes to a growing global electronic-waste stream.
3. Coupled Pressure–Transition Framework
The framework contains two linked state variables. Technological development is represented by K(t), while 
cumulative planetary pressure is represented by P(t). Both are model constructs. Neither should be 
interpreted as a directly observed physical constant.


---

Webb — AI and Planetary Boundaries | 5
Figure 1. Coupled pressure-transition architecture. Pressure-generating terms H, T, and W and pressure-reducing terms E and R
determine net pressure flux ΔP, which accumulates in P and can constrain the effective transition rate R_eff. Resource scarcity may
also feed back into conflict-related pressure.
3.1 Technological Development
dK/dt = R_eff(t) · K(t) · [1 − K(t)/S]
Here K is a dimensionless technological-development state, R_eff is the effective transition rate, and S is a 
sustainability-constrained carrying parameter. The logistic form is a parsimonious baseline rather than an 
empirical law and should be compared with alternative growth functions.
Time convention. The baseline implementation uses a discrete annual update for planetary pressure, P(t+1), 
while the technological-development equation is written in continuous form for interpretability. For 
numerical simulation, both components should be evaluated on a common time step Δt (for example, one 
year), using an explicit numerical integration scheme for K. All reported simulations must state the time step 
and integration method.
Carrying parameter S. In the baseline model, S is fixed within each scenario so that changes in K can be 
attributed cleanly to the pressure coupling. A later extension may allow S=S(t) to evolve when verified 
restoration, infrastructure substitution, or durable resource expansion changes the effective technological 
carrying capacity. Such an endogenous S should be treated as a separate model extension rather than 
introduced implicitly.
3.2 Cumulative Planetary Pressure
P(t+1) = P(t) + ΔP_net(t)
ΔP_net = αH + βT + ωW − εE − ρR
H represents direct industrial-material throughput; T represents technological externalities not captured by 
throughput alone; W represents conflict-related ecological and infrastructural damage; E represents verified 
efficiency gains; and R represents verified ecological restoration. The coefficients α, β, ω, ε, and ρ scale the 
relative contributions of the pressure terms.


---

Webb — AI and Planetary Boundaries | 6
3.3 Pressure Aggregation
P(t) = Σᵢ wᵢ Bᵢ(t), with Σᵢ wᵢ = 1
Each B_i is a normalized boundary or resource-pressure indicator. The model does not assume that all 
boundaries are commensurable in a physical sense; normalization is an analytical transformation used to 
compare scenarios. Results must therefore be tested under multiple weighting and aggregation schemes.
3.4 Pressure–Development Coupling
R_eff = R₀ · (1 − P)^γ
This baseline relationship formalizes the hypothesis that increasing planetary pressure can reduce the 
effective technological transition rate. The function is not presented as an established law of civilization. Its 
functional form and sensitivity parameter γ require calibration and comparison with competing mechanisms.
3.5 Alternative Cost-Mediated Coupling
R_eff = R₀ / [1 + λ C_resource(t)]
The cost-mediated alternative captures a different mechanism: technological growth slows because energy, 
water, materials, land, and infrastructure become increasingly costly or difficult to secure. Sector-specific 
ceilings, threshold functions, delayed responses, and piecewise relationships should also be tested.
4. Methods
4.1 Normalization
Bᵢ(t) = [Xᵢ(t) − Xᵢ,ref] / [Xᵢ,crit − Xᵢ,ref]
X_i(t) is the observed indicator, X_i,ref is a stated reference condition, and X_i,crit is a selected high￾pressure reference or scientifically established boundary where available. Values above 1 may be permitted 
when observed conditions exceed the selected reference. No three-decimal precision should be reported 
unless the underlying data and uncertainty justify it.
4.2 Input Classes
Class Definition Example
Observed Direct empirical measurement TWh of electricity; tonnes of mineral 
production; water withdrawal
Derived Calculated from observations Carbon intensity; material intensity of 
compute
Estimated Parameter inferred from literature or 
fitting
γ; rebound fraction; restoration 
effectiveness
Scenario Assumption used to explore futures Future compute growth; governance 
effectiveness; conflict intensity
4.3 Spatial and Temporal Representation
A global pressure index should be supported by regional sub-indices where the constraint is inherently local. 
Water should be represented at watershed or basin scale; electricity at grid-region scale; mineral pressure at 
extraction and processing regions; and semiconductor impacts at manufacturing clusters. Temporary grid 
congestion or supply shortages should not automatically be interpreted as permanent erosion of global 
development capacity.


---

Webb — AI and Planetary Boundaries | 7
P(t) = P_persistent(t) + P_transient(t)
P_transient(t+1) = (1 − δ) P_transient(t) + S_t
δ is a recovery or dissipation parameter and S_t is a temporary shock. This decomposition prevents short-run 
bottlenecks from being conflated with cumulative Earth-system degradation.
4.4 Verification of Efficiency and Restoration
D_t = e_t · Q_t
An engineering efficiency improvement occurs when resource intensity e declines. An absolute 
environmental reduction occurs only when total demand D also declines relative to an appropriate 
counterfactual. This distinction is necessary because rebound effects can offset per-unit efficiency gains.
E_verified = E_gross − J − D_externalized
J represents rebound effects and D_externalized represents displaced or externalized environmental costs. 
Restoration should likewise be credited only when additionality, measurement, durability, and leakage are 
explicitly addressed.
5. Empirical Data Architecture
The empirical layer should preserve raw observations, transformations, data provenance, and uncertainty. 
The preferred sequence is Raw Observation → Derived Indicator → Normalization → Pressure Component 
→ P(t).
Figure 2. Measurement pipeline for constructing the composite pressure variable. Raw observations are transformed through 
explicit, documented stages before entering P(t).
Component Primary observables Preferred scale Data availability Candidate source 
family
Energy / climate
Electricity demand; 
generation mix; 
operational and 
embodied emissions
Grid / facility / global High IEA; LBNL; grid 
operators
Freshwater
Withdrawal; 
consumption; basin 
stress
Facility / basin Moderate
Hydrological agencies; 
facility disclosures; 
literature
Materials
Production; trade; 
reserves; recycling; 
import reliance
Country / global High USGS and national 
geological surveys
Semiconductors Water; electricity; 
fluorinated gases; 
Fab / cluster Moderate EPA; lifecycle studies; 
company verified 


---

Webb — AI and Planetary Boundaries | 8
wafer throughput reports
Novel entities
Persistent chemicals; 
hazardous waste; 
releases
Facility / regional Low–moderate Regulatory inventories;
peer-reviewed studies
E-waste
Retired equipment; 
collected/recovered 
material
National / global Moderate ITU/UNITAR; national
waste statistics
Land / biosphere Area converted; 
ecological sensitivity Site / regional Moderate Land-cover and 
biodiversity datasets
Efficiency Resource intensity per 
unit useful compute Workload / fleet Moderate–low
Benchmarking; 
operator data; research 
datasets
Restoration Verified physical 
ecological outcome Project / regional Low–moderate
Independent 
monitoring and 
restoration datasets
Conflict
Destroyed 
infrastructure; 
contamination; 
reconstruction burden
Event / regional Low–moderate
Event datasets; 
environmental 
assessments
5.1 Energy Indicators
C_operational = Σᵣ Eᵣ · CIᵣ
E_r is electricity consumed in grid region r and CI_r is the relevant carbon intensity. The model should 
distinguish AI-focused load from conventional data-center load when data permit, and should avoid 
assuming a uniform global marginal generation mix.
5.2 Water Indicators
W*r = W_consumption,r · S_r
S_r is a local water-stress multiplier. Withdrawal and consumption should be reported separately. Regional 
weighting is essential because water scarcity is not spatially uniform.
5.3 Material and Supply-Risk Indicators
M_j(t) = Q_j(t) · I_j(t) · S_j(t)
Q_j is demand for mineral j, I_j its environmental intensity, and S_j a supply-risk or concentration factor. 
Supply risk should initially remain analytically distinct from ecological pressure so that scarcity and 
environmental damage are not conflated.
5.4 Semiconductor Externalities
Semiconductor fabrication should track electricity, ultrapure water, process chemicals, fluorinated-gas 
emissions, hazardous waste, and embodied emissions. EPA identifies perfluorocarbons, hydrofluorocarbons, 
nitrogen trifluoride, sulfur hexafluoride, fluorinated heat-transfer fluids, and nitrous oxide among relevant 
semiconductor process gases. Where possible, the analytical chain should progress from fab to wafer to die 
to accelerator to deployed compute.
5.5 Electronic Waste
EW_AI = N_retired · M_device · (1 − R_effective)


---

Webb — AI and Planetary Boundaries | 9
R_effective should represent verified recovery of usable material rather than equipment merely collected for 
recycling. The Global E-waste Monitor reports that 62 billion kg of e-waste were generated worldwide in 
2022, while only 22.3% was documented as formally collected and recycled in an environmentally sound 
manner.
5.6 Data Quality
Some policy-relevant indicators, particularly novel-entity generation, AI-specific hardware retirement, and 
verified restoration outcomes, remain sparse or inconsistently reported. A data-quality classification should 
therefore accompany each pressure component: A (directly measured and independently validated), B 
(measured but incomplete), C (proxy-based estimate), or D (insufficient for primary quantitative calibration).
6. Hypotheses and Scenario Design
6.1 Pressure-Dominance Hypothesis (H1)
αH + βT + ωW > εE + ρR ⇒ dP/dt > 0
During rapid expansion, industrial-material throughput and technological externalities may exceed verified 
efficiency and restoration, causing modeled pressure to increase.
6.2 Regenerative-Transition Hypothesis (H2)
εE + ρR > αH + βT + ωW ⇒ dP/dt < 0
If verified absolute efficiency gains and restoration exceed pressure-generating processes, technological 
activity may reduce net modeled pressure.
6.3 Development-Constraint Hypothesis (H3)
If technological growth materially depends on resource and Earth-system conditions, sufficiently high P or 
resource cost should reduce R_eff. Evidence that development remains insensitive to severe and persistent 
pressure would weaken or falsify this coupling.
6.4 Scenario Set
- Scenario A — Unconstrained Compute Expansion: rapid compute and infrastructure growth, weak 
restoration, and limited absolute resource reductions.
- Scenario B — Efficiency-Dominated Expansion: strong per-unit computational efficiency with continued
aggregate demand growth.
- Scenario C — Regenerative Transition: verified absolute reductions in material and energy intensity 
combined with substantial ecological restoration.
- Scenario D — Resource-Constrained Expansion: technological growth increasingly limited by energy, 
water, minerals, land, or semiconductor capacity.
- Scenario E — High-Pressure / Conflict Feedback: resource stress interacts with geopolitical competition,
damaged infrastructure, and replacement demand.
6.5 Interpretation of Scenario Thresholds
Threshold-crossing dates are scenario outputs unless the index, parameters, and thresholds are empirically 
calibrated and validated. A statement such as “P = 1 in 2046” should therefore not be presented as a forecast 
in the present paper. Future calibrated versions should report ranges and uncertainty intervals rather than a 
single deterministic year.


---

Webb — AI and Planetary Boundaries | 10
7. Empirical Demonstration: Model v0.1
This section demonstrates how factual observations can enter the coupled framework without implying that 
the full planetary-pressure index has already been calibrated. The first demonstration uses electricity because 
it is currently one of the best-constrained physical inputs. All coefficients not directly measured are labeled 
as sensitivity parameters rather than empirical constants.
7.1 Time Horizon and Notation
The demonstration uses the five-year interval from 2025 through 2030. Raw electricity consumption is 
denoted by E_t and reported in terawatt-hours (TWh). The symbol H_E is reserved exclusively for the 
dimensionless relative growth in data-center electricity demand across this interval. It is not used for raw 
electricity consumption.
E_2025 = 485 TWh
E_2030 = 950 TWh
These values are taken from the International Energy Agency's updated central outlook, which projects 
global data-center electricity demand to roughly double over the period (IEA, 2026).
7.2 Observed Electricity Growth
ΔE_2025→2030 = E_2030 - E_2025 = 950 - 485 = 465 TWh
H_E = (E_2030 - E_2025) / E_2025 = 465 / 485 ≈ 0.959
Thus, the IEA central projection corresponds to an approximately 95.9% cumulative increase in global data￾center electricity demand between 2025 and 2030.
7.3 Annualized Growth Rate
g_E = (E_2030 / E_2025)^(1/5) - 1
g_E = (950 / 485)^(1/5) - 1 ≈ 0.144 ≈ 14.4% per year
The annualized growth rate is reported separately from H_E. H_E is the five-year cumulative relative 
change, whereas g_E is the compound annual growth rate over the same interval.
7.4 Minimum Pressure Demonstration
Before water, materials, land, waste, efficiency, and restoration are fully normalized, a minimum 
demonstration can isolate the electricity component. For this demonstration, the five-year pressure change 
associated with electricity growth is written:
ΔP_2025→2030 = α · H_E
ΔP_2025→2030 = 0.959 α
The coefficient α is a sensitivity parameter in Model v0.1, not an empirically established constant. 
Accordingly, the resulting ΔP values are five-year cumulative scenario changes for 2025–2030 and must not 
be interpreted as annual rates or measured planetary damage.
Illustrative α ΔP_2025→2030 Interpretation
0.05 ≈ 0.048 Five-year cumulative scenario change; 
not an observed pressure value.
0.10 ≈ 0.096 Five-year cumulative scenario change; 


---

Webb — AI and Planetary Boundaries | 11
not an observed pressure value.
0.20 ≈ 0.192 Five-year cumulative scenario change; 
not an observed pressure value.
The rounded sensitivity results are therefore approximately 0.048, 0.096, and 0.192 for α values of 0.05, 
0.10, and 0.20 respectively. Their function is to demonstrate model sensitivity while the empirical electricity 
trajectory is held fixed.
7.5 Multidimensional Extension
The electricity demonstration is intentionally incomplete. The full model uses a multidimensional set of 
pressure indicators that must first be normalized independently because their physical units are not directly 
additive.
X_2030 = [ E_2030, W_2030, M_2030, L_2030, EW_2030, ... ]^T
Here E denotes electricity demand, W water pressure, M material pressure, L land pressure, and EW 
electronic-waste pressure. Each raw observation is transformed through its own normalization function:
B_i(t) = N_i(X_i(t))
H = w_E B_E + w_W B_W + w_M B_M + w_L B_L + ...
T = w_EW B_EW + w_NE B_NE + ...
ΔP = αH + βT + ωW_c - εE_v - ρR
To prevent notation collisions, W_c denotes conflict-related ecological damage in this subsection, E_v 
denotes verified efficiency, and R denotes verified restoration. The distinction is necessary because W is also
commonly used for water in empirical datasets.
7.6 Two-Equation Coupling
The numerical demonstration becomes dynamically relevant when the Webb pressure equation is coupled to 
the technological-transition equation. The first equation determines net change in planetary pressure over the 
chosen time step; the accumulated pressure state then modifies the effective technological transition rate used
by the second equation.


---

Webb — AI and Planetary Boundaries | 12
Figure 3. Relationship between the Webb pressure equation and the Kardashev-inspired technological-transition equation. 
Technological activity changes pressure-generating and pressure-reducing terms; the resulting pressure state feeds back into the 
effective transition rate.
7.7 Regional Validation Case
The United States provides a useful regional validation case. Lawrence Berkeley National Laboratory's 2025 
Update reports a 2030 reference-case data-center electricity demand of 649 TWh, with compounded 
uncertainty scenarios ranging from 521 to 843 TWh. The report estimates that data centers could account for 
11.8% of U.S. electricity consumption in the reference case and 9.5%–15.3% across the scenario range 
(LBNL, 2026).
E_US,2030 ∈ [521, 843] TWh
Model v0.1 should propagate this empirical uncertainty rather than selecting only the central value. This 
creates a direct sensitivity test in which the physical input varies while the mathematical architecture remains
unchanged.
7.8 Interpretation
Model v0.1 establishes only a modest empirical claim: the physical infrastructure supporting data centers is 
projected to expand rapidly under current central scenarios. It does not yet establish the absolute magnitude 
of the composite planetary-pressure state P, the value of a universal critical threshold, or the calibrated 
strengths of α, β, ω, ε, ρ, and γ.
The initial empirical test of the pressure-dominance hypothesis is therefore the sign of net pressure change:
αH + βT + ωW > εE + ρR ?
If the pressure-generating side exceeds verified efficiency and restoration, ΔP is positive. If verified 
efficiency and restoration exceed the pressure-generating terms, ΔP is negative. This keeps the framework 
neutral and makes the competing pathways explicit and testable.


---

Webb — AI and Planetary Boundaries | 13
7.9 Earth-System Context
The Planetary Health Check 2026 reports that seven of nine planetary boundaries are transgressed. That 
observation provides Earth-system context but should not be converted mechanically into P = 7/9. The 
number of transgressed boundaries describes breadth of disturbance, whereas P is a separately constructed 
composite state whose magnitude must depend on boundary-specific control variables, normalization, 
weighting, and uncertainty.
Empirical anchors for Model v0.1: International Energy Agency (2026) for the global electricity trajectory; 
Lawrence Berkeley National Laboratory (2026) for the U.S. regional electricity case; and Planetary Health 
Check (2026) for the current planetary-boundary context. Additional water, material, semiconductor, land, 
and waste variables should be added only when their attribution and normalization rules are documented.
8. Discussion
The proposed framework shifts the debate from whether AI is categorically sustainable or unsustainable to a 
more measurable question: what is the net balance between the physical pressures created by technological 
expansion and the verified pressure reductions enabled by efficiency and restoration? This distinction is 
important because per-unit efficiency and absolute environmental improvement are not equivalent.
The framework also suggests that compute may be better conceptualized as a cross-boundary pressure 
multiplier than as a tenth planetary boundary. A planetary boundary refers to a fundamental Earth-system 
process with scientifically defined control variables and a safe operating space. Compute is instead an 
anthropogenic activity capable of propagating pressure through several existing boundaries simultaneously.
Another implication is that global averages may conceal binding regional constraints. A data center may be 
globally small in water terms while locally significant in a stressed watershed. Likewise, global mineral 
abundance may coexist with acute concentration risk in specific processing jurisdictions. Spatially 
differentiated modeling is therefore not an optional refinement but an eventual requirement for policy￾relevant implementation.
The framework is deliberately neutral regarding AI’s long-run environmental role. If AI materially 
accelerates grid optimization, material substitution, climate mitigation, scientific discovery, and ecological 
restoration—and those benefits are verified at system level—the negative terms in the pressure equation can 
dominate. If rebound, infrastructure growth, and material throughput dominate instead, the model should 
show the opposite. Both outcomes are admissible.
9. Limitations and Open Questions
Aggregate pressure variable. Operationalizing P is difficult because planetary boundaries are 
heterogeneous, non-linear, and measured on different spatial and temporal scales. Aggregation can obscure 
binding constraints. Multiple weighting schemes and sensitivity tests are therefore required.
Spatial and temporal resolution. Water, electricity, mining, semiconductor manufacturing, and ecological 
damage occur at different geographic scales. Short-run bottlenecks must also be distinguished from persistent
degradation. Regional pauses in growth need not imply a simultaneous decline in aggregate K.
Single technological stock. K simplifies a heterogeneous technological system. Frontier training, distributed 
inference, specialized accelerators, algorithmic efficiency, and application mix may evolve with different 
resource intensities. Future versions should allow sectoral decomposition.


---

Webb — AI and Planetary Boundaries | 14
Measurement architecture. Calibration requires data on compute intensity, water use, materials, embodied 
emissions, chemical externalities, hardware lifetimes, and restoration outcomes. Several of these remain 
incomplete, proprietary, or inconsistently reported.
Efficiency and restoration verification. Efficiency gains may be offset by rebound, while restoration can be
delayed, reversible, or displaced. Explicit accounting rules and counterfactuals are necessary before E or R 
should reduce P.
Institutional feedbacks. Policy, standards, disclosure, procurement, capital allocation, and governance 
influence both efficiency and restoration. In the first model these may remain exogenous scenario drivers 
rather than fully endogenous variables.
Conflict endogeneity. W is initially exogenous or semi-exogenous, but competition over minerals, energy, 
water, and infrastructure could make conflict partly endogenous to technological scaling.
Coupling uncertainty. R_eff = R0(1−P)^γ is a transparent hypothesis, not an empirical law. Cost-mediated, 
threshold, delayed, piecewise, and sector-specific alternatives must be compared.
Uncertainty communication. Parameter uncertainty should be separated from structural uncertainty. The 
former concerns unknown values within a model; the latter concerns whether the model architecture itself is 
correct.
These limitations define the empirical research program rather than invalidating the framework. Its value lies
in making assumptions explicit, testable, and replaceable as better observations become available.
10. Governance and Research Implications
A calibrated version of the framework could support decision-making without embedding a predetermined 
policy conclusion. It could compare, for example, the effects of regional siting rules, water-stress constraints,
hardware-lifetime standards, energy-source requirements, recycling improvements, or restoration investment.
The model’s purpose would be to expose trade-offs and pressure transfers rather than to select a political or 
regulatory outcome.
Comparative policy analysis could therefore be implemented as matched scenarios rather than as normative 
recommendations. For example, one scenario might impose basin-level water-stress siting constraints, 
another might extend accelerator service life through hardware-lifetime standards, and a third might allocate 
equivalent investment to independently verified ecological restoration. Their effects could then be compared 
across ΔP, regional bottlenecks, cost, and technological-development trajectories. The model would expose 
trade-offs and burden shifting without declaring a preferred political outcome.
The framework also creates a strong transparency requirement. Any deployment of the model for public or 
corporate decision support should publish its parameter registry, datasets, normalization functions, 
uncertainty ranges, scenario assumptions, and model version. This is particularly important because a 
composite index can otherwise create an appearance of precision that exceeds the evidence.
11. Conclusion
Artificial intelligence is a physical industrial system as well as an informational technology. Its future scale 
will depend on electricity, water, minerals, semiconductor capacity, land, infrastructure, and functioning 
ecological and economic systems. These dependencies justify examining AI growth within the broader 
context of planetary boundaries and industrial metabolism.


---

Webb — AI and Planetary Boundaries | 15
This paper proposes a coupled pressure–transition framework in which technological development K affects 
cumulative planetary pressure P through industrial-material throughput, technological externalities, conflict 
damage, efficiency, and restoration, while planetary pressure can in turn alter the effective technological 
transition rate. The model does not establish a predetermined collapse trajectory and does not treat an 
arbitrary P = 1 crossing as a known physical date. Instead, it provides a reproducible structure for testing 
competing pathways.
The central empirical question is therefore not whether AI is inherently a planetary threat or a planetary 
solution. It is whether verified system-level reductions in pressure can outpace the additional physical 
demands created by technological expansion. Answering that question requires transparent data, spatially 
resolved indicators, explicit uncertainty, alternative coupling models, and open sensitivity analysis. Those 
requirements define the next stage of the Webb pressure framework.
12. Priority Empirical Next Steps
The highest-priority empirical work is not additional theoretical complexity but better attribution and 
measurement. Three gaps are especially important: (1) AI-specific water and material intensities that 
distinguish training, inference, and shared facility overhead; (2) verified restoration metrics that quantify 
additionality, durability, leakage, and counterfactual outcomes; and (3) regionally resolved semiconductor 
externalities, including water, electricity, fluorinated-gas emissions, hazardous materials, and embodied 
impacts from fabrication through accelerator deployment.
A second priority is workload attribution. Where AI and conventional digital services share the same data 
center, electricity, cooling, land, and infrastructure burdens should not be assigned to AI without an explicit 
allocation rule. Improved workload-level reporting would substantially strengthen both the H and T terms 
and reduce reliance on sector-wide proxies.
13. Data and Code Availability
This manuscript presents the conceptual and methodological specification of the model. A reproducible 
reference implementation, machine-readable parameter registry, and scenario datasets should accompany a 
subsequent calibrated release. Public-source data should be archived by version and retrieval date, and 
proprietary inputs should be clearly identified and excluded from claims that require independent replication.
References
International Energy Agency (IEA). (2026). Key Questions on Energy and AI: Executive Summary. IEA, 
Paris. https://www.iea.org/reports/key-questions-on-energy-and-ai/executive-summary
Planetary Health Check. (2026). Planetary Health Check 2026: A Scientific Assessment of the State of the 
Planet. Potsdam Institute for Climate Impact Research. https://www.planetaryhealthcheck.org/
Planetary Health Check. (2025). Planetary Health Check 2025: A Scientific Assessment of the State of the 
Planet. Potsdam Institute for Climate Impact Research. 
https://www.planetaryhealthcheck.org/downloads/
Richardson, K., Steffen, W., Lucht, W., et al. (2023). Earth beyond six of nine planetary boundaries. Science 
Advances, 9(37), eadh2458.


---

Webb — AI and Planetary Boundaries | 16
Steffen, W., Richardson, K., Rockström, J., et al. (2015). Planetary boundaries: Guiding human development 
on a changing planet. Science, 347(6223), 1259855.
Smith, S. J., Hubbard, A., Newkirk, A., et al. (2026). United States Data Center Energy Usage Report: 2025 
Update. Lawrence Berkeley National Laboratory. https://seta.lbl.gov/publications/united-states-data￾center-energy-2025
Shehabi, A., Smith, S. J., Hubbard, A., et al. (2024). 2024 United States Data Center Energy Usage Report. 
Lawrence Berkeley National Laboratory. https://doi.org/10.71468/P1WC7Q
U.S. Geological Survey. (2026). Mineral Commodity Summaries 2026 (Version 1.3). U.S. Geological 
Survey. https://doi.org/10.3133/mcs2026
International Telecommunication Union (ITU) & United Nations Institute for Training and Research 
(UNITAR). (2024). The Global E-waste Monitor 2024.
Mytton, D. (2021). Data centre water consumption. npj Clean Water, 4, 11. https://doi.org/10.1038/s41545-
021-00101-w
Li, P., Yang, J., Islam, M. A., & Ren, S. (2023). Making AI Less “Thirsty”: Uncovering and Addressing the 
Secret Water Footprint of AI Models. arXiv:2304.03271.
U.S. Environmental Protection Agency. (2026). Semiconductor Industry: Fluorinated Greenhouse Gas 
Emissions. https://www.epa.gov/eps-partnership/semiconductor-industry
Taiwan Semiconductor Manufacturing Company (TSMC). (2025). 2024 Sustainability Report.
Appendix A. Initial Parameter Registry Template
Symbol Meaning Class Unit Initial treatment Uncertainty
P₀ Initial composite 
pressure
Derived Normalized Compute from selected 
indicators Report propagation
R₀
Unconstrained 
technological transition 
rate
Estimated / scenario time ¹⁻ Fit or scenario range Distribution
S Carrying parameter Scenario / estimated Normalized Sensitivity range Distribution
γ Pressure sensitivity Estimated Dimensionless Fit across candidate 
models Confidence interval
α
Industrial-pressure 
coefficient Estimated Model-specific Calibration Confidence interval
β Externality coefficient Estimated Model-specific Calibration Confidence interval
ω Conflict coefficient Estimated / scenario Model-specific Scenario then calibration Range
ε
Efficiency offset 
coefficient Estimated Model-specific Calibration Range
ρ Restoration coefficient Estimated Model-specific Calibration Range
λ Resource-cost sensitivity Estimated Model-specific Alternative coupling 
calibration Range


---

Webb — AI and Planetary Boundaries | 17
Appendix B. Glossary of Symbols
Symbol Meaning Interpretive note
K(t) Technological-development state Dimensionless aggregate state variable; not an AI 
benchmark score.
S Technological carrying parameter Fixed within baseline scenarios; may become S(t) 
only in an explicit extension.
R₀ Unconstrained transition rate Baseline growth parameter before pressure or 
resource constraints.
R_eff Effective transition rate Growth rate after pressure/resource feedback is 
applied.
P(t) Composite planetary-pressure state Model-derived index; not a published planetary￾boundary control variable.
ΔP_net Net pressure flux Balance of pressure-generating and pressure￾reducing terms over one time step.
H Industrial-material footprint Direct energy, water, material, land, and embodied 
throughput.
T Technological externalities Impacts not captured by throughput alone, including
waste and process externalities.
W Conflict-related damage Ecological and infrastructural pressure from 
conflict; initially exogenous or semi-exogenous.
E Verified efficiency Only system-level reductions after rebound and 
displacement are accounted for.
R Verified restoration
Measured ecological improvement subject to 
additionality, durability, measurement, and leakage 
rules.
γ Pressure sensitivity Controls strength of the P→R_eff coupling in the 
baseline power-law form.
λ Resource-cost sensitivity Controls the alternative cost-mediated coupling.
wᵢ Pressure-component weight Aggregation weight assigned to normalized 
component Bᵢ.
Bᵢ(t) Normalized pressure component Transformed indicator retaining source, scale, and 
uncertainty metadata.
δ Transient-pressure recovery rate Controls decay of temporary shocks in the transient￾pressure component.
