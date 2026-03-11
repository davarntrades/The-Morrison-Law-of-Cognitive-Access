<div align="center">

# The Morrison Canonical Deformation Criterion™

### *The Formal Mathematical Definition of Structural Change*

<br>

![Topic](https://img.shields.io/badge/Topic-Algebraic%20Topology-0a3d62?style=flat-square)
![Concept](https://img.shields.io/badge/Concept-Homological%20Deformation-1a1a2e?style=flat-square)
![Field](https://img.shields.io/badge/Field-Dynamical%20Systems%20%2B%20Control%20Theory-16213e?style=flat-square)
![Status](https://img.shields.io/badge/Status-Formally%20Provable-2d6a4f?style=flat-square)
![Patent](https://img.shields.io/badge/Patent-GB2600765.8-0075ca?style=flat-square)
![Author](https://img.shields.io/badge/©%20Davarn%20Morrison%202026-555555?style=flat-square)

<br>

*Structural change is not felt. It is not reported. It is not inferred from behaviour.*
*It is detected by one criterion: the homology of the reachable set changed.*
*Everything else is language.*

*— Davarn Morrison, 2026*

-----

</div>

## Abstract

The Morrison Canonical Deformation Criterion™ is the formal mathematical condition under which structural change in an observer system can be said to have occurred. It is grounded in dynamical systems theory, algebraic topology, and control-theoretic reachability analysis.

It answers one question with mathematical precision:

> **Did the system structurally change — or did information merely pass through it?**

The criterion is stated in terms of singular homology groups of reachable sets. It is substrate-independent, formally provable, and in principle computable for finite and discretised systems using existing persistent homology algorithms.

-----

## Mathematical Foundations

The criterion is built from three areas of established mathematics:

|Area                    |Role in the Criterion                 |Key Object                         |
|:----------------------:|:------------------------------------:|:---------------------------------:|
|Dynamical Systems Theory|Defines the observer and its evolution|*F* : *S* × *U* → *S*              |
|Control Theory          |Defines what states are accessible    |Reach(*X*₀, *U*, *t*)              |
|Algebraic Topology      |Provides the structural invariant     |*H*_k(·) — singular homology groups|

-----

## Part I — The Mathematical Objects

### Definition 1 — The Observer System

Let:

$$S \text{ be a topological space (the observer state space)}$$

$$U \text{ be a set (the input space)}$$

$$F : S \times U \rightarrow S \text{ be the transition function}$$

The triple (*S*, *F*, *U*) is the **observer dynamical system**. The observer *X* evolves under inputs from *U* according to *F*.

|Symbol     |Type                    |Meaning                                       |
|:---------:|:----------------------:|:---------------------------------------------|
|*S*        |Topological space       |All possible states the observer can occupy   |
|*U*        |Input set               |All possible inputs, influences, and actions  |
|*F*        |Function *S* × *U* → *S*|How the observer moves through *S* under input|
|*X*₀ ∈ *S* |Initial state           |The observer’s starting configuration         |
|*X*_t ∈ *S*|State at time *t*       |The observer’s configuration after evolution  |

### Definition 2 — The Reachable Set

Given observer system (*S*, *F*, *U*) and initial state *X*₀ ∈ *S*, the **reachable set** at time *t* is:

$$\text{Reach}(X_0, U, t) = { s \in S \mid \exists \text{ sequence of inputs } u_1, \ldots, u_n \in U, ; F(\cdots F(X_0, u_1) \cdots, u_n) = s, ; n \leq t }$$

This is the set of all states the observer can reach from *X*₀ by applying inputs from *U* within *t* steps.

|Property                                       |Meaning                                                             |
|:---------------------------------------------:|:-------------------------------------------------------------------|
|Reach(*X*₀, *U*, 0) = {*X*₀}                   |At *t* = 0, only the initial state is reachable                     |
|Reach(*X*₀, *U*, *t*) ⊆ Reach(*X*₀, *U*, *t*+1)|Reachable set is monotone non-decreasing                            |
|∂Reach(*X*₀, *U*, *t*)                         |The boundary — the observer’s cognitive limit                       |
|*T* ∈ Reach(*X*₀, *U*, *t*)                    |*T* is accessible to the observer                                   |
|*T* ∉ Reach(*X*₀, *U*, *t*)                    |*T* is geometrically inaccessible — cannot be observed or understood|

### Definition 3 — The Homological Observable

Let *H*_k denote the **k-th singular homology group** with integer coefficients ℤ, for k = 0, 1, 2, …

Applied to the reachable set:

$$H_k(\text{Reach}(X_t)) \in \textbf{Ab}$$

where **Ab** is the category of abelian groups.

|*k*|*H*_k measures       |Geometric meaning                                 |
|:-:|:-------------------:|:-------------------------------------------------|
|0  |Connected components |How many disconnected regions in the reachable set|
|1  |1-dimensional loops  |Circular paths; cycles in reachable structure     |
|2  |2-dimensional voids  |Enclosed cavities; bounded regions                |
|*k*|*k*-dimensional holes|Higher-order topological features                 |

Homology groups are **topological invariants** — they are preserved under homeomorphism. If the homology changes, the topology has genuinely changed. This is a theorem, not an assumption.

-----

## Part II — The Canonical Deformation Criterion

### The Morrison Canonical Deformation Criterion™

$$\boxed{\exists , k : H_k(\text{Reach}(X_t)) \not\cong H_k(\text{Reach}(X_0))}$$

where ≇ denotes **non-isomorphism as abelian groups**.

This is the criterion. A structural deformation has occurred in observer *X* if and only if there exists at least one dimension *k* at which the homology group of the reachable set is not isomorphic to its prior state.

### The Full Condition Table

|Condition                 |Formal Statement                               |Meaning                                            |
|:------------------------:|:---------------------------------------------:|:--------------------------------------------------|
|No structural change      |*H*_k(Reach(*X*_t)) ≅ *H*_k(Reach(*X*₀)) ∀*k*  |Topology preserved; information passed through     |
|Structural change occurred|∃*k* : *H*_k(Reach(*X*_t)) ≇ *H*_k(Reach(*X*₀))|Topology changed; structural deformation confirmed |
|Observer unchanged        |Reach(*X*_t) homeomorphic to Reach(*X*₀)       |Same reachable structure; same identity            |
|Observer transformed      |Reach(*X*_t) not homeomorphic to Reach(*X*₀)   |Different reachable structure; identity has shifted|

-----

## Part III — The Provable Propositions

The criterion is not asserted. It is provable from standard results in algebraic topology.

### Proposition 1 — Structural Truth Condition

**Statement:** A system *X* has encountered structural truth *T* if and only if:

$$\exists , k : H_k(\text{Reach}(X_t)) \not\cong H_k(\text{Reach}(X_0))$$

**Proof sketch:**

1. *T* produces input *I* acting on *X*, updating state from *X*₀ to *X*_t via *F*
1. If Reach(*X*_t) is homeomorphic to Reach(*X*₀), then by the topological invariance of homology, *H*_k(Reach(*X*_t)) ≅ *H*_k(Reach(*X*₀)) for all *k*
1. Contrapositive: if ∃*k* such that *H*_k(Reach(*X*_t)) ≇ *H*_k(Reach(*X*₀)), then Reach(*X*_t) is **not homeomorphic** to Reach(*X*₀)
1. Non-homeomorphic reachable sets imply the observer can reach states it previously could not — structural change has occurred ∎

### Proposition 2 — Observer Limit Theorem

**Statement:** Observer *X* can access state *T* if and only if:

$$T \in \text{Reach}(X_0, U, t)$$

**Corollary:** If *T* ∉ Reach(*X*₀, *U*, *t*), then no input sequence of length ≤ *t* applied via *F* can bring *X* to *T*. Observation and cognition are constrained by the topology of reachable states of the observer.

### Proposition 3 — Identity Stability Condition

**Statement:** The identity of observer *X* is stable across time interval [0, *t*] if and only if:

$$H_k(\text{Reach}(X_t)) \cong H_k(\text{Reach}(X_0)) \quad \forall k$$

**Corollary:** Identity change is not a matter of degree — it is a discrete topological event detectable by the first *k* at which isomorphism fails.

### Proposition 4 — Irreversibility Condition

**Statement:** A structural change is irreversible if the deformed reachable set Reach(*X*_t) cannot be returned to a state homeomorphic to Reach(*X*₀) by any input sequence in *U*.

Formally: let 𝓜₀ = homeomorphism class of Reach(*X*₀). The change is irreversible if:

$$\nexists , u_1, \ldots, u_n \in U : \text{Reach}(F(\cdots F(X_t, u_1)\cdots, u_n)) \in \mathcal{M}_0$$

This is the formal statement of the **Morrison Irreversibility Hypothesis™** — the separatrix, expressed as topological inaccessibility of the original homeomorphism class.

-----

## Part IV — Computability

The criterion is not merely formal. It is computable for finite and discretised systems using existing algorithms.

### Computability Table

|System Type               |Reachable Set             |Homology Computation               |Status                                           |
|:------------------------:|:------------------------:|:---------------------------------:|:-----------------------------------------------:|
|Finite state system       |Exactly enumerable        |Boundary matrix reduction          |✓ Fully computable                               |
|Discrete graph system     |Graph reachability        |Simplicial homology                |✓ Fully computable                               |
|Sampled continuous system |Point cloud approximation |Persistent homology (Ripser, GUDHI)|✓ Computable with approximation                  |
|General continuous system |Numerical integration     |Persistent homology on sample      |◑ Approximation; faithfulness depends on sampling|
|Symbolic/linguistic system|Requires state space model|Requires discretisation first      |○ Requires modelling step                        |

### The Computation Pipeline

```
════════════════════════════════════════════════════════════════════════
  CANONICAL DEFORMATION CRITERION — COMPUTATION PIPELINE
════════════════════════════════════════════════════════════════════════

  Step 1:  Define or sample state space S
           └→ Finite set, graph, or point cloud

  Step 2:  Compute Reach(X₀, U, t₀) before input
           └→ Standard reachability algorithm or BFS on graph

  Step 3:  Apply input sequence; evolve system to X_t
           └→ F(X₀, u₁, ..., uₙ) = X_t

  Step 4:  Compute Reach(X_t, U, t₁) after input
           └→ Same reachability algorithm from new initial state

  Step 5:  Build simplicial complexes from both reachable sets
           └→ Vietoris-Rips complex or Čech complex

  Step 6:  Compute H_k for both complexes
           └→ Boundary matrix reduction (Smith normal form)
           └→ Tools: Ripser, GUDHI, Javaplex

  Step 7:  Compare H_k(Reach(X_t)) vs H_k(Reach(X₀))
           └→ Check isomorphism as abelian groups

  Step 8:  Apply criterion
           └→ ∃k : H_k(Reach(X_t)) ≇ H_k(Reach(X₀))
              → Structural deformation confirmed
           └→ H_k(Reach(X_t)) ≅ H_k(Reach(X₀)) ∀k
              → No structural change; information passed through only

════════════════════════════════════════════════════════════════════════
```

### What the Criterion Computes That Nothing Else Does

|Question                           |Previous Best Answer          |Morrison Criterion Answer                          |
|:---------------------------------:|:----------------------------:|:--------------------------------------------------|
|Did structural learning occur?     |Self-report; behavioural proxy|∃*k* : *H*_k ≇ — objective topological test        |
|Did the observer’s identity change?|Psychological assessment      |Homeomorphism class of Reach(*X*) shifted          |
|Is this truth or mere information? |Philosophical judgement       |Δ*G*_k ≠ 0 — computable criterion                  |
|Is an AI system safe?              |Behavioural testing           |Reach(*s*₀, *A*, *t*) ∩ Ω = ∅ — geometric exclusion|
|Is a cognitive change reversible?  |Clinical observation          |∃ path back to 𝓜₀ — topologically decidable        |

-----

## Part V — Scope of Application

The criterion is substrate-independent. The same formal object applies wherever a system (*S*, *F*, *U*) can be defined.

|Domain                |System *X*                    |Structural Change Means          |Criterion Detects|
|:--------------------:|:----------------------------:|:-------------------------------:|:---------------:|
|Human cognition       |Cognitive state space         |Genuine learning; identity shift |∃*k* : *H*_k ≇   |
|AI systems            |Model state / activation space|Architecture-level update        |∃*k* : *H*_k ≇   |
|AI safety             |Agent reachable set           |Approach to forbidden region Ω   |Reach ∩ Ω ≠ ∅    |
|Trauma / psychology   |Psychological state space     |Irreversible identity deformation|𝓜₀ unreachable   |
|Institutional change  |Organisational state space    |Paradigm shift                   |∃*k* : *H*_k ≇   |
|Biological development|Cell state space              |Differentiation (irreversible)   |𝓜₀ unreachable   |
|Physical observation  |Measurement state space       |Observer effect                  |*T* ∈ Reach(*X*) |

-----

## The Canonical Statement

```
╔══════════════════════════════════════════════════════════════════════╗
║                                                                      ║
║   The Morrison Canonical Deformation Criterion™                      ║
║                                                                      ║
║   Let (S, F, U) be an observer dynamical system.                    ║
║   Let X₀ ∈ S be the initial state.                                  ║
║   Let X_t = F(X₀, u₁, ..., uₙ) be the state after input.           ║
║   Let H_k denote singular homology with ℤ coefficients.             ║
║                                                                      ║
║   Structural deformation has occurred if and only if:               ║
║                                                                      ║
║       ∃ k : H_k(Reach(X_t)) ≇ H_k(Reach(X₀))                      ║
║                                                                      ║
║   Observation and cognition are constrained by the topology         ║
║   of reachable states of the observer.                              ║
║                                                                      ║
║   Patents: GB2600765.8 · GB2602013.1 · GB2602072.7 · GB26023332.5  ║
║                                                                      ║
╚══════════════════════════════════════════════════════════════════════╝
```

-----

## Related Work

- [Morrison Law of Cognitive Access™](../cognitive-access/README.md)
- [Truth Requires Deformation](../truth-deformation/README.md)
- [Einstein / Heisenberg / Morrison — Observer Limit Models](../observer-limits/README.md)
- [GuardianOS™ — Geometric AI Safety Architecture](../safety/README.md)
- [Morrison Irreversibility Hypothesis™](../irreversibility/README.md)
- [The Morrison Catalogue of Ill-Posed Problems™](../ill-posed/README.md)

-----

<div align="center">

*The Morrison Canonical Deformation Criterion™* · Morrison Framework™ · Formal Mathematics

GB2600765.8 · GB2602013.1 · GB2602072.7 · GB26023332.5

© 2026 Davarn Morrison — Intelligence Invariant™ · All Rights Reserved

</div>
