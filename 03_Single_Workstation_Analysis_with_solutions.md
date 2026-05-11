---
layout: default
---

{% raw %}

# Analysis and Management of Production System — Lesson 3: Single Workstation Analysis

Prof. Giulia Bruno — Department of Management and Production Engineering — giulia.bruno@polito.it

# Deterministic vs Stochastic Models

- The simple throughput analysis of a serial factory with deterministic processing times was used to illustrate several system performance measures
- This approach does not yield accurate results when processing times are random
- The next models will include probabilistic behavior for the arrival process and processing times

# Variability

Definition: non-uniformity of a class of entities. It causes a departure from regularity and predictability of the system behaviour.

Sources: Machine failures, Material shortages, Operator unavailability, Different skill levels, Material handling, Product variety.

A random variable is characterized by: Type of distribution (Exponential, Normal, Poisson...), Mean value μ, Variance σ², Skewness, Kurtosis.

Coefficient of Variation (CV): c = σ/μ

Squared coefficient of variation (SCV): c² = σ²/μ²

Classification:
- Low variability (LV): c < 0.75
- Moderate variability (MV): 0.75 < c < 1.33
- High variability (HV): c ≥ 1.33

# Effect of variability

Example — Constant processing time t0=10 min, constant arrival rates: A=1/30 pcs/min, B=1/20 pcs/min, C=1/10 pcs/min, D<1/10 pcs/min.

Example — Constant processing time=10 min, variable arrival rate:
- Waiting time in queue = 3 min
- 6 units processing time = 65 min
- Mean waiting time = 3/65 = 0.046 min
- Inactivity time = 5 min = 7.7% of 65
- Utilization = 92.3%

- X = accepting long waiting times to obtain high utilization
- Y = accepting low machine utilization to obtain short waiting time
- Z = reducing variability to obtain both higher utilization AND short waiting times (optimal)

# Example: limited system (M/M/1/3)

Single machine, max 3 jobs accepted. λ=5 jobs/day, μ=4/day. Both times exponentially distributed.

**Diagram model:** states {0,1,2,3}. Upward transitions at rate λ·p_n, downward at rate μ·p_n. No arrivals at state 3.

**Balance equations:**
- λ p_0 = μ p_1
- λ p_1 = μ p_2
- λ p_2 = μ p_3
- p_0 + p_1 + p_2 + p_3 = 1

**Solution:** p_1=(λ/μ)p_0, p_2=(λ/μ)²p_0, p_3=(λ/μ)³p_0

p_0 = [1 + λ/μ + (λ/μ)² + (λ/μ)³]^(-1)

**(p_0, p_1, p_2, p_3) = (0.173, 0.217, 0.271, 0.339)**

WIP = 1×0.217 + 2×0.271 + 3×0.339 = **1.776 jobs**

**Comments:**
- Server idle time: 17.3%
- Lost jobs/day: λ×p_3 = 5×0.339 = 1.695
- TH = 5 - 1.695 = **3.305 jobs/day**
- CT = WIP/TH = 1.776/3.305 = **0.537 days**

# Effective arrival rate

When the system is finite, arriving jobs may be lost. The effective arrival rate is:

**λ_e = λ(1 - p_nmax)**

At steady-state: **TH = λ_e**. Little's Law must use λ_e (not λ).

# Queuing Systems

Defined in 1917 by Erlang. A queuing system includes:
1. Arrival process — single/batch, deterministic/stochastic
2. Production/service process — single/parallel machines
3. Queue — FCFS, LCFS, SIRIO; limited or unlimited

# Kendall Notation: A/B/c/K

- A = inter-arrival time distribution
- B = service time distribution
- c = number of servers
- K = max jobs (omit if infinite)

Common codes: M=Exponential, D=Deterministic, G=General, Ek=Erlang-k

Example: **M/M/1/3** — M/M/1 = M/M/1/∞ (K omitted when infinite)

# Infinite Capacity Model (M/M/1)

Exponential arrivals, exponential service, 1 server, unlimited queue.

Balance equations: λ p_n = μ p_{n+1} for all n; sum p_n = 1

Solution (geometric series, valid if u=λ/μ < 1):

**p_0 = 1 - u**

**p_n = (1-u) × u^n**

**Performance measures:**
- u = λ/μ (utilization, must be < 1)
- WIPs = u/(1-u)
- CTs = WIPs/λ = 1/(μ-λ)
- CTq = u/(1-u) × E[Ts]
- WIPq = u²/(1-u)
- TH = λ

Performance measures → infinity as u → 1.

**Example:** λ=4/hr, μ=5/hr, E[Ts]=0.2 hr → u=0.8, WIPs=4, CTs=1 hr, CTq=0.8 hr

**Exercise solution:** λ=2.875/hr, μ=3/hr, E[Ts]=0.333 hr → u=0.958, WIP=22.81, CT=7.934 hr, CTq=7.6 hr, WIPq=21.85

# Infinite Capacity Model (M/M/c)

c identical servers, each rate μ. Service rate when all busy = cμ.

**CTq(M/M/c) = (u^(sqrt(2c+2)-1)) / (c(1-u)) × E[Ts]**

When c=1, reduces to M/M/1.

# Non-identical service rates — M/M/2/4

Two machines: faster (rate μ), slower (rate γ), γ < μ. Max 4 jobs. States: {0, 1f, 1s, 2, 3, 4}.

Balance equations:
- λ p_0 = μ p_1f + γ p_1s
- λ p_1f + λ p_1s = (γ+μ) p_2
- λ p_2 = (γ+μ) p_3
- λ p_3 = (γ+μ) p_4
- p_0 + p_1f + p_1s + p_2 + p_3 + p_4 = 1

**Helicopter example:** λ=3/day, μ=3/day (8h), γ=2/day (12h), nmax=4

Solution: p_0=0.288, p_1f=0.209, p_1s=0.118, p_2=0.196, p_3=0.118, p_4=0.071

Results:
- WIPs = **1.356**, WIPq = **0.259**
- λ_e = 3×(1-0.071) = 2.787
- CTs = **0.486 day**, CTq = **0.093 day**
- E[T] = 0.393 days = **9.4 hr**
- E[BS] = 1.097 → u = E[BS]/c = **54.85%**

**Simulation exercise solution:** μ=4 j/d, γ=2 j/d, λ=2 j/d, % lost=1.17%, utilization=32.67%

# Combination of Exponentials: Erlang-k Distribution

Sum of k independent identical exponential distributions.

- f(s) = k(ks)^(k-1) × e^(-(k/β)s) / (β^k × (k-1)!)
- E[X]=β, V[X]=β²/k, **C²[X] = 1/k**

As k increases, C² decreases → less variability than exponential (k=1).

# M/E2/1/3 — Erlang-2 Processing Time

Max 3 jobs, exponential arrivals (λ), Erlang-2 service (μ). Erlang-2 = 2 phases, each exponential with rate 2μ. State (n,i): n=jobs in system, i=phase.

Balance equations (node isolation):
- λ p_0 = 2μ p_12
- (λ+2μ) p_11 = λ p_0 + 2μ p_22
- (λ+2μ) p_12 = 2μ p_11
- (λ+2μ) p_21 = λ p_11 + 2μ p_32
- 2μ p_31 = λ p_21
- 2μ p_32 = λ p_22 + 2μ p_31
- p_0+p_11+p_12+p_21+p_22+p_31+p_32 = 1

Performance measures:
- WIPs = sum(n=1 to 3) n×(p_n1+p_n2)
- TH = λ_e = λ(1-p_31-p_32)
- CTs = WIPs/λ_e

**Exercise M/E3/1/2:** λ=3 j/h, μ=6 j/h, max 2 jobs.

Solution: p_0=0.557, p_11=0.127, p_12=0.108, p_13=0.093, p_21=0.021, p_22=0.039, p_23=0.055

Results: WIPs=0.558, WIPq=0.115, TH=2.655 j/h, CTs=0.21 hr, CTq=0.043 hr

**Exercise M/E3/1/3:** λ=4 j/h, μ=8 j/h, max 3 jobs. Given p=[0.5207, 0.1180, 0.1012, 0.0868, 0.0357, 0.0451, 0.0510, 0.0060, 0.0135, 0.0220]. Compute TH, WIP, WIPq, CT.

Excel tip for linear systems: =MMULT(MINVERSE(A), b) with Ctrl+Shift+Enter.

# General Service Distribution — M/G/1

Single server, exponential arrivals (λ), general service (mean 1/μ, variance σ_s²).

**Pollaczek-Khintchine (P-K) formula:**

WIPq = [(λ/μ)² + λ²σ_s²] / [2(1-λ/μ)]

CTq = WIPq/λ

Rewritten using C_s² = σ_s²/E[Ts]²:

**CTq(M/G/1) = ((1+C_s²)/2) × (u/(1-u)) × E[Ts]**

**CTq(M/G/1) = ((1+C_s²)/2) × CTq(M/M/1)**

When C_s²=1 (exponential): M/G/1 = M/M/1. When C_s² < 1: shorter queues. When C_s² > 1: longer queues.

# Approximation for G/G/1 — Kingman Formula (VUT Equation)

**CTq(G/G/1) ≈ ((C_a² + C_s²)/2) × (u/(1-u)) × E[Ts]**

**CTs(G/G/1) ≈ ((C_a² + C_s²)/2) × (u/(1-u)) × E[Ts] + E[Ts]**

When applied to M/M/1 or M/G/1 → exact (not approximation).

**Example 1:** λ=4/hr, μ=5/hr, u=0.8, C_a²=1, C_s²=1, E[Ts]=0.2 hr → CTq = 0.8 hr ✓

**Example 2:** λ=4/hr, μ=5/hr, u=0.8, C_a²=4, C_s²=0.25, E[Ts]=0.2 hr
- CTq = ((4+0.25)/2) × (0.8/0.2) × 0.2 = **1.7 hr** (>2× the exponential case)
- WIPq=6.8, CTs=1.9 hr, WIPs=7.6

**Exercise:** λ=2.875/hr, C_a=1, E[T]=20 min, C_s=2.5, u=0.9583
- CTq = ((1+6.25)/2) × (0.9583/0.0417) × 20 = **27.77 hrs**
- WIPq=80, CTs=28.1 hr, WIPs=81

# Approximation for G/G/c — Allen-Cunneen (Hall)

**CTq(G/G/c) ≈ ((C_a²+C_s²)/2) × CTq(M/M/c)**

CTq(M/M/c) = (u^(sqrt(2c+2)-2)/c) × CTq(M/M/1)

**CTq(G/G/c) ≈ ((C_a²+C_s²)/2) × (u^(sqrt(2c+2)-1)/(c(1-u))) × E[Ts]**

**Example G/G/2:** c=2, E[Ts]=24 min, u=0.8, C_a²=4, C_s²=0.25
- CTq(G/G/2) = ((4+0.25)/2) × ((0.8)^(sqrt(6)-1)/(2×0.2)) × 0.4 = **1.54 hr**

{% endraw %}
