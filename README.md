# Quantitative-Tests-of-a-Classical-Rotor-Kernel-for-the-FQCU-Programme-Thermal-Fluctuations
Quantitative Tests of a Classical Rotor Kernel for the FQCU Programme:
Frequency Ratios, Lattice Anisotropy, Relaxation, Thermal Fluctuations, and Phase
Stiffness
Prof. Dr. Md. Faridul Islam Chowdhury, MBBS, MS (Neurosurgery)1
1Tanfarid Vision Research Institute, Bogura, Bangladesh ∗
(Dated: November 2026)
We formulate a multi-observable validation programme for a classical rotor kernel proposed within
the Farid Quantum Command Unit (FQCU) programme. The model consists of canonical planar
rotors on a periodic three-dimensional cubic lattice with nearest-neighbour interactions. Five tests
are developed: harmonic frequency ratios independent of the overall frequency scale; directiondependent lattice dispersion at equal wavevector magnitude; damped relaxation compared with the
exact linear rate and its large-system asymptote; low-temperature phase fluctuations compared with
harmonic equipartition; and the connected helicity-modulus response to a boundary twist.
Exact identities of the linearized lattice model are distinguished from long-wavelength expansions and harmonic equilibrium approximations. A reproducible protocol specifies independent
timestep and amplitude refinement, frequency-estimator checks, autocorrelation-aware uncertainties, and blocked uncertainty analysis of the nonlinear stiffness estimator. The protocol is then
executed for a declared configuration. Measured harmonic frequencies reproduce the exact lattice
dispersion with relative errors below 10−5
; the equal-magnitude directional splitting, the exact overdamped relaxation rates, and the continuous three-dimensional stiffness vanishing near the established ordering temperature are reproduced within stated uncertainties. Thermal mode fluctuations
agree with harmonic equipartition within block uncertainties across kBT /J = 0.05–0.30, with no
resolved anharmonicity or timestep bias. These results validate the specified implementation and
approximation regime; they do not establish a physical FQCU substrate. Independent empirical
matching remains a separate requirement.
I. INTRODUCTION
An explicit dynamical model becomes useful when several observables can be calculated from one declared parameter set and tested without separate adjustment for
each result.
The preceding FQCU rotor formulation supplies a candidate state space and local dynamics for the mathematical component of Open Problem O1 [1]. The present
article develops quantitative tests of that model.
The adopted Hamiltonian belongs to the established
family of classical XY rotor systems [2, 3]. Its frequency
spectrum, thermal fluctuations, and twist response are
model properties, not new laws inferred from an FQCU
interpretation.
The contribution is a consolidated analytical benchmark, a validation design, and its execution for one declared configuration. No new critical exponent, empirical particle identification, or experimental confirmation
is claimed.
A. Three levels of claim
We distinguish:
1. analytical consequences of specified equations;
∗ dr_faridul@yahoo.com
2. numerical verification and characterization of those
equations;
3. empirical matching to an independently measured
physical system.
The first level is developed here, and the second is
carried out for a declared configuration in Sec. XII. The
third remains open.
The phrase “no refitting” means that parameters declared for an experiment are not adjusted separately to
force agreement with each observable. It does not mean
that every test is parameter-independent.
II. MODEL AND CONVENTIONS
Consider a connected periodic cubic lattice with N =
L
3
sites and spacing ℓ. Here L is a site count, and the
box length is Lℓ.
Each site carries
(θi
, pi) ∈ S
1 × R, {θi
, pj} = δij .
All other elementary Poisson brackets vanish.
The Hamiltonian is
H =
X
i
p
2
i
2I
+ J
X
⟨ij⟩
[1 − cos(θi − θj )], I, J > 0, (1)
where every undirected nearest-neighbour bond is
counted once.
2
Hamilton’s equations are
˙θi =
pi
I
, p˙i = J
X
j∼i
sin(θj − θi). (2)
The isolated model conserves H and
P =
X
i
pi
. (3)
A uniformly aligned minimum-energy state at fixed P
rotates at
Ω0 =
P
NI
. (4)
Small perturbations are defined in that co-rotating frame:
θi(t) = θ0 + Ω0t + ϕi(t). (5)
Unless otherwise stated, mode-validation experiments
use P = 0. The lattice, spatial dimension, and time
coordinate are prescribed, not emergent.
A. Separate dynamical experiments
Three models are kept distinct:
1. conservative Hamiltonian dynamics;
2. deterministic dynamics with friction;
3. Langevin dynamics with a specified thermal bath.
Results from these experiments are not interpreted as
properties of one unchanged evolution law.
III. HARMONIC LATTICE SPECTRUM
When neighbouring phase differences are small, Eq. (2)
gives
Iϕ¨
i = J
X
j∼i
(ϕj − ϕi). (6)
For
ϕi = Aei(k·xi−ωt)
,
the exact dispersion of this linearized model is
Ω
2
k =
4J
I
X
3
µ=1
sin2

kµℓ
2

. (7)
Allowed periodic wavevectors satisfy
k =
2π
Lℓn, (8)
with integer components represented in the first Brillouin
zone.
At long wavelength,
Ω
2
k =
Jℓ2
I
|k|
2 −
Jℓ4
12I
X
µ
k
4
µ
+ O

J
I
(|k|ℓ)
6

. (9)
Equation (7) is exact for the harmonic lattice equations. It is not the exact nonlinear finite-amplitude spectrum.
IV. TEST 1: SCALE-INDEPENDENT
FREQUENCY RATIOS
For an axis-directed mode n = (n, 0, 0),
Ωn = 2r
J
I



sin πn
L


 . (10)
Consequently,
Ωn
Ω1
=
|sin(πn/L)|
sin(π/L)
(11)
for nonzero modes under consideration.
The overall frequency scale cancels. This is the
parameter-independent part of the proposed suite.
A. Measurement
Initialize a small real cosine mode,
ϕi(0) = A cos(k · xi), pi(0) = 0. (12)
For generic nonzero, non-Nyquist modes, measure
ak(t) = 2
N
X
i
ϕi(t) cos(k · xi). (13)
Special self-conjugate modes require their corresponding
normalization.
Frequency extraction may use a validated sinusoidal
fit or a windowed spectral estimator with peak interpolation.
Zero padding assists interpolation but does not increase the information contained in a fixed observation
interval. Estimator accuracy is tested on synthetic signals before application to trajectories.
B. Acceptance
Frequency ratios must converge toward Eq. (11) under
separate amplitude, timestep, and observation-duration
checks. No precision level is assumed in advance.
3
V. TEST 2: EQUAL-MAGNITUDE LATTICE
ANISOTROPY
Choose
nA = (3, 0, 0), nB = (2, 2, 1). (14)
Both satisfy |n|
2 = 9. Their exact harmonic splitting is
∆Ω2 ≡ Ω
2
B − Ω
2
A
=
4J
I

2 sin2

2π
L

+ sin2
 π
L

− sin2

3π
L
 .
(15)
Define the common magnitude
q = |k|ℓ =
6π
L
. (16)
Since
X
µ
n
4
A,µ = 81,
X
µ
n
4
B,µ = 33,
Eq. (9) gives
∆Ω2 =
4J
81I
q
4 + O

J
I
q
6

. (17)
The full lattice result and leading expansion are distinct references. At modest L, q may not be sufficiently
small for the leading term to be highly accurate.
A. Acceptance
First compare measurements with Eq. (15). Then increase L at fixed mode indices to test convergence toward
Eq. (17).
Because the splitting is a difference of squared frequencies, its uncertainty must include both frequency estimates and any covariance.
No inference about anisotropy of physical light is made.
VI. TEST 3: DAMPED RELAXATION
Introduce the separate dissipative model
I
¨θi + γ
˙θi = J
X
j∼i
sin(θj − θi), γ > 0. (18)
It obeys
H˙ = −γ
X
i
˙θ
2
i
, P˙ = −
γ
I
P. (19)
For a harmonic mode,
Ia¨ + γa˙ + IΩ
2
ka = 0. (20)
In the strictly overdamped regime,
 γ
2I
2
> Ω
2
k
, (21)
the two decay rates are
rs,f =
γ
2I
∓
r
γ
2
4I
2
− Ω2
k
. (22)
The slow time is
ts =
1
rs
. (23)
For stable numerical evaluation, use
rs =
Ω
2
k
γ/(2I) + p
[γ/(2I)]2 − Ω2
k
. (24)
For the smallest nonzero axis mode,
Ω
2
min =
4J
I
sin2
 π
L

. (25)
At sufficiently large L and fixed nonzero damping,
ts '
γL2
4π
2J
. (26)
A. Measurement and acceptance
The linear response contains both decay branches:
a(t) = Ase
−rst + Afe
−rf t
. (27)
Use either a two-branch fit or demonstrate that the selected late-time interval suppresses the fast branch.
Compare first with Eq. (23), then report the difference
from Eq. (26). Vary fit windows, timestep, amplitude,
and L.
These times describe linear relaxation around an
aligned state. They do not predict defect-annihilation
or generic ordering times.
VII. TEST 4: THERMAL MODE
FLUCTUATIONS
Use the undriven Langevin model
dθi =
pi
I
dt, (28)
dpi =

J
X
j∼i
sin(θj − θi) −
γ
I
pi

 dt +
p
2γkBT dWi
,
(29)
where the Wi are independent Wiener processes.
4
The continuous dynamics has canonical stationary
density proportional to e
−H/(kBT)
. A finite-timestep integrator requires independent sampling checks.
For the unconstrained canonical ensemble,
hpii = 0, hpipj i = IkBT δij . (30)
In the harmonic phase description, define
ϕk =
1
√
N
X
i
ϕie
−ik·xi
. (31)
For k 6= 0,


|ϕk|
2

=
kBT
IΩ2
k
. (32)
A. Circular phases and harmonic validity
For an aligned configuration, define
θc = arg X
i
e
iθi
!
, (33)
and
ϕi = arg h
e
i(θi−θc)
i
. (34)
This reduces branch-cut artifacts but is not a general
solution to phase unwrapping in a disordered or defectrich state.
Monitor wrapped nearest-neighbour differences
∆ij = wrap(θj − θi), (35)
their RMS and maximum values, and plaquette winding.
A bound on max |ϕi
| alone does not prove harmonic
accuracy. Repeat the test at decreasing kBT /J to assess
anharmonic corrections.
B. Acceptance
Use autocorrelation-aware errors, multiple seeds, equilibration checks, timestep refinement, and temperature
refinement.
BAOAB is a suitable splitting method to investigate,
but the exact Ornstein–Uhlenbeck substep does not make
the complete finite-timestep scheme exactly canonical for
a general nonlinear potential [4].
Agreement with Eq. (32) is assessed only in a demonstrated harmonic regime.
VIII. TEST 5: PHASE STIFFNESS
Impose a total twist Φ in the x direction by assigning
Φ/L to each oriented positive-x bond:
∆ij 7→ ∆ij −
Φ
L
. (36)
Define
F(Φ) − F(0) = 1
2
ΥxL
D−2Φ
2 + O(Φ4
). (37)
Here D = 3 and Υx has energy units in this lattice convention.
Let
Cx =
X
⟨ij⟩x
cos ∆ij , Sx =
X
⟨ij⟩x
sin ∆ij . (38)
Differentiating F = −kBT ln Z gives
Υx =
1
N

J hCxi − J
2
kBT


S
2
x

− hSxi
2


. (39)
At zero twist, equilibrium symmetry gives hSxi = 0.
The connected form is retained, and the sampled mean
current is reported as a diagnostic.
For the aligned zero-temperature small-twist state,
Υx(T → 0) = J. (40)
The three-dimensional XY transition is not assigned
a BKT-like universal stiffness jump. At criticality the
conventional finite-size behaviour is
Υx(Tc, L) ∝ L
−1
, (41)
up to corrections [5].
A single finite lattice cannot establish thermodynamic
vanishing or locate Tc precisely.
A. Nonlinear estimator and uncertainty
Record Cx, Sx, and S
2
x
. Compute the central estimate
from full-run means in Eq. (39).
Do not estimate stiffness by averaging connected variances computed separately in short blocks. Such centring
removes between-block current fluctuations.
For uncertainty, use a blocked jackknife or another
justified method for nonlinear correlated observables.
Recompute the complete expression after deleting each
block.
Increase block length until uncertainty estimates are
stable within the available statistics. Compare independent runs, ordered and disordered starts, and windingsector sampling. Do not clip negative finite-sample stiffness estimates to zero.
5
IX. UNIFIED VALIDATION PROTOCOL
A. Predeclared configuration
Record:
• model parameters and lattice sizes;
• code version, initial conditions, and seeds;
• integrator, timestep, equilibration, and observation
duration;
• sampling stride and estimator settings;
• fit windows, uncertainty methods, and acceptance
tolerances.
Accuracy tolerances are numerical requirements, not
thresholds for confirming FQCU constituents.
B. Independent refinements
For deterministic mode tests, include at least:
1. baseline (∆t, A);
2. timestep refinement (∆t/2, A);
3. amplitude refinement (∆t, A/2);
4. a longer observation interval.
Keep mode content and other settings fixed when isolating an error source.
Synthetic-signal tests must precede claims about frequency estimator precision.
C. Conservation and balance checks
Monitor
ϵH =
|H(t) − H(0)|
NJ
, ϵP =
|P(t) − P(0)|
N
√
IJ
(42)
for conservative runs.
For damped runs, test
H(t) − H(0) + γ
Z t
0
X
i
˙θ
2
i du = 0 (43)
within convergent numerical error.
A plot that appears bounded is not sufficient evidence
of the claimed convergence order.
TABLE I. Status of the analytical reference expressions.
Test Reference and scope
Frequency ratios Scale-independent identity of the harmonic lattice model.
Anisotropy Exact harmonic lattice splitting; separate small-q expansion.
Relaxation Exact linear overdamped rate; separate large-L asymptote.
Thermal fluctuations
Canonical harmonic approximation
for nonzero phase modes.
Stiffness Exact equilibrium fluctuation identity for the specified twist.
D. Autocorrelation and independent runs
For each stationary observable A, estimate its normalized autocorrelation rA(m) and
tint,A =
1
2
+
X
m≥1
rA(m). (44)
Use a declared summation window and sufficient run duration.
Block sizes should be assessed relative to autocorrelation times. Ten arbitrary blocks do not by themselves
establish reliable errors.
For thermal tests, compare several timesteps and independent initializations. Differences can arise from sampling error, discretization bias, or genuine anharmonicity.
E. Required outputs
Release:
• executable source and configuration files;
• raw or sufficient processed time series;
• CSV tables of estimates, uncertainties, and references;
• convergence diagnostics;
• a figure displaying all five tests.
A validation table should label every test as passed,
failed, or unresolved under declared criteria.
A saved diagnostic figure is not automatically a verified
publication result.
X. PARAMETER DEPENDENCE AND
INTERPRETATION
Parameters may be chosen differently for clearly separated numerical experiments, but each choice must be
6
declared. A claim of common-parameter cross-checking
requires an actual shared parameter set.
Successful numerical agreement verifies an implementation and its approximation regime. It does not establish a physical substrate or predict a measured fundamental parameter.
Failure must be classified as an implementation error,
estimator limitation, approximation breakdown, sampling problem, or missing model property before a physical interpretation is considered.
XI. PHYSICAL MATCHING REQUIREMENTS
Before claiming an independent empirical prediction,
specify:
1. a physical target and measurement;
2. a mapping of rotor variables to observables;
3. calibration inputs and adjustable parameters;
4. unit setting and validity range;
5. numerical and theoretical uncertainties;
6. a predeclared comparison and rejection rule.
Choosing I, J, ℓ so that
cr = ℓ
p
J/I
matches an observed speed is calibration, not an independent prediction of that speed.
The present scalar modes are not identified with photons. No quark confinement, emergent spacetime, or
Standard Model spectrum is derived.
A computational pre-registration is distinct from an
empirical prediction. Both require a dated, immutable
specification of the actual test before its results are examined.
XII. NUMERICAL EXECUTION AND RESULTS
The protocol of Sec. IX was executed for one declared
configuration. All runs use I = J = ℓ = 1 and a fixed
seed; the implementing scripts, configuration, and CSV
tables of estimates and uncertainties are released with
this article.
A. Declared configuration
• Conservative runs: velocity-Verlet integrator, ∆t =
0.02, observation duration Tobs = 400, lattice L =
24; initial perturbation a superposition of small cosine modes of amplitude A = 5 × 10−3
.
TABLE II. Measured harmonic frequencies at L = 24 against
the exact linearized dispersion, Eq. (7).
Mode n Ω (exact) Ω (meas) rel. err
(1, 0, 0) 0.26105 0.26105 6.1 × 10−7
(2, 0, 0) 0.51764 0.51764 3.0 × 10−6
(3, 0, 0) 0.76537 0.76537 7.9 × 10−6
(1, 1, 0) 0.36918 0.36918 8.0 × 10−7
(2, 1, 0) 0.57974 0.57974 4.6 × 10−6
(2, 2, 1) 0.77720 0.77721 8.8 × 10−6
• Frequency estimator: nonlinear least-squares fit of
ak(t) = A cos ωt + B sin ωt with golden-section refinement in ω; validated against timestep refinement.
• Damped runs: deterministic OVRVO-type splitting
at zero noise, γ = 2, ∆t = 0.02, L = 8, 12, 16,
single-mode initialization of amplitude 0.05.
• Thermal runs: BAOAB Langevin integrator, L =
16, kBT = 0.30, γ = 1, ∆t = 0.02, 5000 discarded equilibration steps and 40000 production
steps sampled every 10 steps; circular-mean phase
removal before mode analysis. Refinement runs:
kBT /J = 0.05, 0.10, 0.20, 0.30 at ∆t = 0.02 plus
kBT = 0.30 at ∆t = 0.01, each with 10000 equilibration and 60000 production steps.
• Stiffness runs: checkerboard Metropolis sampling,
L = 8, 10, 12, six temperatures in 1.8 ≤ kBT /J ≤
2.8, 1500 equilibration and 4000 measurement
sweeps; uncertainties from 8 blocks recomputing
the full connected estimator.
B. T1: frequency ratios
Table II lists the measured frequencies against the exact linearized dispersion of Eq. (7). The maximum relative error over six modes is 8.8 × 10−6
. The scaleindependent ratio of Eq. (11) is
Ω(2,0,0)
Ω(1,0,0)
= 1.982894 (meas), 1.982890 (exact). (45)
Timestep refinement (∆t = 0.02 → 0.01, identical physical duration and sampling cadence) shifts the (1, 0, 0)
frequency by 1.4×10−6
relative. The estimator therefore
resolves frequencies far below the raw Fourier bin spacing
∆ω = 2π/Tobs ' 0.016, as required; no 10−3
-level claim
rests on bin selection.
7
TABLE III. Overdamped decay rates of the smallest axis
mode at γ = 2: measured against the exact linear rate rs
of Eq. (23), with the asymptotic time of Eq. (26).
L rs (exact) r (meas) rel. err ts (meas)
8 0.35641 0.35138 1.4 × 10−2
2.85
12 0.14440 0.14414 1.8 × 10−3
6.94
16 0.07926 0.07923 4.1 × 10−4
12.62
C. T2: equal-magnitude anisotropy
For the pair of Eq. (15) at L = 24,
Ω(3,0,0) = 0.765367 (exact), 0.765373 (meas), (46)
Ω(2,2,1) = 0.777204 (exact), 0.777211 (meas). (47)
The squared splitting is
∆Ω2 = 0.018258 (exact), 0.018261 (meas), (48)
a relative deviation of 2 × 10−4
. The leading small-q
estimate of Eq. (17), 0.018790, lies 3% above the exact
value at this L — quantitatively illustrating the stated
caution that the asymptotic reference must not be used
at modest L.
D. T3: damped relaxation
Table III compares measured decay rates of the smallest axis mode with the exact linear slow rate. Agreement improves with L because the late-time window suppresses the fast branch more effectively as the rate separation grows; the residual 1.4% deviation at L = 8 is
attributed to fast-branch contamination of the fitted window, not to a failure of Eq. (23). The asymptotic L
2
law
of Eq. (26) approaches the measured times from above,
with the finite-size offset visible at small L as expected.
E. T4: thermal fluctuations
Table IV gives measured mode fluctuation amplitudes
at kBT = 0.30 against harmonic equipartition, Eq. (32),
with block uncertainties. All six modes agree within 1.8σ.
A first refinement study separated the two candidate
error sources identified in Sec. VII. An earlier, shorter
production run had shown a ∼ 2σ deficit on the (1, 0, 0)
mode; a longer run reported 0.984 ± 0.126, indicating a
statistical fluctuation. A second, five-configuration refinement study (300 time units equilibration, 2400 time
units production per configuration, 12000 retained samples) has now been executed on an independent seed,
with raw mode trajectories retained. Its lowest-mode results are collected in Table V. Three conclusions follow.
First, the deficit is not reproduced. The original-style
estimator (twice the squared real Fourier quadrature,
TABLE IV. Thermal mode fluctuations at L = 16, kBT =
0.30 (BAOAB, 60000 production steps), against harmonic
equipartition. Errors are blocked standard errors of the mean
over 8 blocks.
Mode n prediction measured ratio
(1, 0, 0) 4.811 × 10−4
(4.73 ± 0.60) × 10−4
0.98
(2, 0, 0) 1.250 × 10−4
(1.30 ± 0.08) × 10−4
1.04
(3, 0, 0) 5.932 × 10−5
(6.45 ± 0.35) × 10−5
1.09
(1, 1, 0) 2.405 × 10−4
(2.46 ± 0.18) × 10−4
1.02
(2, 1, 0) 9.924 × 10−5
(9.01 ± 0.52) × 10−5
0.91
(2, 2, 0) 6.252 × 10−5
(5.84 ± 0.26) × 10−5
0.93
TABLE V. Lowest-mode normalized fluctuation ratio
R(1,0,0) = (IΩ
2
k/kBT)⟨|ϕk|
2
⟩ in the five-configuration refinement study (L = 16, I = J = γ = 1, BAOAB),
with autocorrelation-based standard errors, the integrated
autocorrelation time, and the measured mean bond RMS.
The harmonic bond-RMS prediction is √
(kBT /3J)(1 − 1/N):
0.1291, 0.1826, 0.2582, 0.3162 at the four temperatures.
kBT /J ∆t R(1,0,0) τint bond RMS
0.05 0.02 1.075 ± 0.076 5.719 0.1296
0.10 0.02 0.991 ± 0.051 3.505 0.1841
0.10 0.01 1.031 ± 0.051 3.528 0.1842
0.20 0.02 1.045 ± 0.051 3.582 0.2627
0.30 0.02 1.137 ± 0.075 4.626 0.3247
the like-for-like comparison with the earlier 0.82 ± 0.10)
gives R = 1.011 ± 0.099 at kBT /J = 0.30 on the longer
independent-seed trajectory. The earlier deficit is therefore attributed to a statistical fluctuation; it is insufficient
evidence for genuine suppression. Second, the sign of the
leading anharmonic correction is positive, not negative:
the quartic term in 1 − cos ∆ = ∆2/2 − ∆4/24 + · · ·
softens the interaction relative to its quadratic approximation, and the leading spin-wave estimate is
Rk ' 1 +
kBT
6J

1 −
1
N

, (49)
i.e. 1.008, 1.017, 1.033, 1.050 at the four temperatures.
The measured complex-mode ratios of Table V are compatible with this small positive correction, but their
uncertainties are too large to resolve the temperature
slope; an independent Metropolis cross-check at L = 8
reproduces Eq. (49) quantitatively (1.022 ± 0.057 and
1.051 ± 0.028 at kBT /J = 0.10 and 0.30). Third,
no timestep dependence is resolved at kBT /J = 0.10:
R∆t=0.01 − R∆t=0.02 = 0.040 ± 0.073 with independentseed, autocorrelation-based errors. This does not bound
percent-level discretization bias; the grid has no halftimestep control at kBT /J = 0.30.
Diagnostic checks support the equilibrium interpretation: the measured bond RMS tracks the harmonic
prediction at all four temperatures, the largest sam-
8
pled wrapped bond difference at kBT /J = 0.30 reached
2.077 rad (small average fluctuations do not imply uniformly small bonds), and all five final configurations contain zero nonzero-winding plaquettes (a final-state check,
not a proof of defect absence throughout the trajectories). Nested-duration checkpoints at kBT /J = 0.30
(1.042 ± 0.153, 1.062 ± 0.084, 1.137 ± 0.075 at 800, 1600,
2400 time units) are correlated subsamples of one trajectory, not three independent experiments.
Seed stability at kBT /J = 0.30, ∆t = 0.02 has now
been tested directly with five independent Langevin trajectories (seeds 301–305; ordered starts, independent random streams; 300 time units equilibration and 2400 time
units production per seed, 60000 retained samples in total). Per-seed lowest-mode complex ratios range from
0.981 ± 0.064 to 1.149 ± 0.079. Combining the five seed
means with the uncertainty estimated from their scatter
(not from the pooled time samples) gives
R
complex
(1,0,0) = 1.0617±0.0286, Rquadr.
(1,0,0) = 1.0601±0.0374,
(50)
with 95% Student-t intervals [0.9822, 1.1412] and
[0.9563, 1.1640] respectively (four degrees of freedom).
The across-seed and within-run autocorrelation-based error estimates agree (0.0286 vs. 0.0313; 0.0374 vs. 0.0361),
and a heterogeneity test finds no excess between-seed
scatter (Q = 3.30, df = 4, p ' 0.51; p ' 0.44 for
the quadrature estimator). The six complex-mode ensemble means span 1.039–1.062, so the lowest mode is
not anomalous; mean kinetic temperatures remain within
3 × 10−4 of the target. Three conclusions follow: the
earlier 0.82-type deficit is not a stable ensemble feature;
both estimators agree on the ensemble mean; and because
both intervals include R = 1, the lowest mode alone does
not establish the positive correction of Eq. (49) at 95%
confidence — the ensemble mean 1.062 sits 0.4σ above
the spin-wave value 1.050, consistency rather than measurement. Seed stability at (kBT /J, ∆t) = (0.30, 0.02) is
thereby closed; what remains open for T4 is timestep convergence at high temperature, which requires the same
independent-seed ensemble at ∆t = 0.01 with matched
physical durations — the kBT /J = 0.10 half-timestep
control cannot bound discretization effects at kBT /J =
0.30.
F. T5: phase stiffness
Figure 1(e) and the released CSV table show the
connected helicity-modulus estimates. At kBT = 1.8
the stiffness is Υx ' 0.50 at all three sizes, reduced
from its T → 0 value J by spin-wave fluctuations. It
falls continuously through the established ordering region
kBTc/J ' 2.20: the product ΥxL takes the values 1.28,
1.13, and 1.12 at L = 8, 10, 12 and kBT = 2.20, consistent
with the critical finite-size behaviour Υx(Tc, L) ∝ L
−1
up to corrections, and not with a two-dimensional universal jump. Above Tc the estimates are consistent with
TABLE VI. Status of the five tests under the declared criteria.
“Passed*” denotes agreement within the stated window or
statistical limitation, reported rather than hidden.
Test Reference Status
T1 ratios Eq. (11); max rel. err
8.8 × 10−6
; ∆t shift 1.4 ×
10−6
passed
T2
anisotropy
Eq. (15); splitting rel.
dev. 2 × 10−4
passed
T3 relaxation
Eq. (23); rel. err 4 × 10−4
(L = 16) to 1.4% (L = 8,
fast-branch window)
passed*
T4 fluctuations
Eq. (32); all modes within
1.8σ; five-seed ensemble:
deficit not reproduced,
R = 1.0617 ± 0.0286,
consistent with small positive (softening) anharmonicity, Eq. (49)
passed
T5 stiffness Eq. (39); continuous vanishing, ΥxL ≈ const at
Tc, no jump
passed at stated
statistics
zero within block uncertainties; the small negative finitesample values are retained unclipped, as required. The
mean current hSxi /N remains at the 10−3
level or below,
serving as the declared sampling diagnostic. Larger lattices, longer runs, and disordered-start comparisons are
required before a precision estimate of Tc or of critical
amplitudes can be attempted; none is claimed.
G. Validation table
Table VI classifies the outcomes. Every test compares
one declared parameter set against an analytical reference without refitting. The agreement validates the implementation and its approximation regime; it does not
establish a physical substrate, and no rotor observable is
identified with a measured fundamental parameter.
XIII. LIMITATIONS AND CONCLUSION
We have developed five connected tests of a specified classical rotor model: scale-independent frequency
ratios, equal-magnitude directional dispersion, damped
relaxation, thermal fluctuations, and phase stiffness.
The analytical scope of each test is explicit. Harmonic identities are separated from nonlinear dynamics, long-wavelength asymptotes from finite-lattice expressions, and equilibrium formulas from finite-sample
estimates.
The protocol was executed for one declared configuration (Sec. XII). Harmonic frequencies, the equalmagnitude splitting, overdamped relaxation rates, and
9
FIG. 1. Summary of the executed validation suite for one declared configuration (I = J = ℓ = 1). (a) Measured harmonic
frequencies against the exact linearized dispersion at L = 24. (b) Equal-magnitude directional pair |n|
2 = 9. (c) Overdamped
decay rates against the exact linear slow rate and its large-L asymptote. (d) Thermal mode fluctuations against harmonic
equipartition with block uncertainties. (e) Connected helicity-modulus estimates at L = 8, 10, 12 with blocked uncertainties;
the dashed line marks the established kBTc/J ≃ 2.20. (f) Numerical summary. Underlying estimates and uncertainties are
released as CSV tables.
the continuous stiffness vanishing agree with their analytical references within stated uncertainties; thermal
fluctuations agree with harmonic equipartition across
kBT /J = 0.05–0.30: the five-configuration refinement
study and a five-seed ensemble at kBT /J = 0.30 did not
reproduce the earlier lowest-mode deficit, the ensemble
mean 1.0617 ± 0.0286 is consistent with the small positive spin-wave correction of Eq. (49), and no timestep
dependence was resolved at kBT /J = 0.10. The immediate next steps are the matched-duration half-timestep
independent-seed ensemble at kBT /J = 0.30, and the
larger-lattice stiffness campaign of Sec. VIII.
The programme advances when one declared dynamics passes independent checks without hidden refitting.
A physical FQCU interpretation requires an additional
empirical mapping that these model-level tests do not
provide.
ACKNOWLEDGMENTS
The author acknowledges the Tanfarid Vision Research
Institute.
All discoveries herein are by the mercy of Allah. This
knowledge is a trust.
[1] M. F. I. Chowdhury, “A Classical Rotor Realization for
Open Problem O1: Local Dynamics, Collective Order,
Thermodynamic Consistency, and Physical Matching in
the FQCU Programme,” companion manuscript (2026).
[2] X. Leoncini, A. D. Verga, and S. Ruffo, “Hamiltonian dynamics and the phase transition of the XY model,” Phys.
Rev. E 57, 6377 (1998), arXiv:cond-mat/9808019.
[3] K. Nam, W.-B. Baek, B. Kim, and S. J. Lee, “Coarsening
of two dimensional XY model with Hamiltonian dynamics:
Logarithmically divergent vortex mobility,” J. Stat. Mech.
(2012) P11023, arXiv:1211.1462.
[4] B. Leimkuhler and C. Matthews, “Rational construction
of stochastic numerical methods for molecular sampling,”
Appl. Math. Res. Express 2013, 34–56 (2013).
[5] A. P. Gottlob and M. Hasenbusch, “Critical behaviour of
the 3D XY-model: A Monte Carlo study,” Physica A 201,
593–613 (1993), arXiv:cond-mat/9305020.
