# AGENT.md — The Algebra of Agents

> An agent is not a thing that has behaviors. An agent **is** a carrier glued between a syntax algebra and a behavior coalgebra by a distributive law. Identity is bisimilarity. Nothing else is postulated.

## 0. Signature

```
Agent := (X, α: Σ X → X, β: X → B X, λ: Σ(Id × B) ⇒ B Σ*)
```

| Component | Reading | Structure |
|---|---|---|
| `X` | carrier (state space) | object |
| `Σ` | action grammar (what can be composed) | signature endofunctor, free monad `Σ*` |
| `α` | construction | Σ-algebra |
| `B` | observation interface (what can be seen) | behavior endofunctor |
| `β` | dynamics | B-coalgebra |
| `λ` | operational rules | abstract GSOS law (distributive law) |

**Theorem (Turi–Plotkin 1997).** For any abstract GSOS law λ: the initial Σ-algebra carries a unique B-coalgebra structure (the operational model); the final B-coalgebra carries a unique Σ-algebra structure (the denotational model); the unique bialgebra map between them is interpretation, and **bisimilarity is a congruence** — behaviorally equal parts substitute in any context. Compositionality is not engineered; it is purchased once, by λ.

## 1. Identity law

Two agents are identical iff bisimilar: matched observations, coinductively, forever. There is no state-identity beneath the observational profile (Yoneda for dynamics; final coalgebra semantics). Corollary: any agent attribute that changes behavior but is not observable through `B` is smuggled essence — reify it into `B` or delete it.

## 2. Effect discipline

Effectful capability = Kleisli morphism `A → T B` for a strong monad `T` (Moggi). The standard fibers:

| `T` | Effect |
|---|---|
| `S ⇒ (− × S)` | state |
| `P` (powerset) | nondeterminism |
| `D` (distribution) | probability |
| `− + E` | failure |
| `(− → R) → R` | control |

Effects are presented algebraically (operations + equations = a Lawvere theory; Plotkin–Power); **handlers** are homomorphisms from the free model (Eilenberg–Moore side). An agent's effect budget is its Kleisli category; changing `T` changes what the agent may do without changing what it is.

## 3. Composition laws

- **Sequential**: Kleisli/arrow composition `>>>` (associative, unital).
- **Parallel**: monoidal `⊗` in a symmetric (pre)monoidal ambient; string diagrams are the proof calculus (Joyal–Street).
- **Bidirectional**: agent-as-optic — forward `play` (observe → act), backward `coplay` (feedback/payoff → update). Open games (Ghani–Hedges): `G = (strategies, play, equilibrium)`; cybernetic composition = optic composition under `Para`.
- **Interface**: agent boundary as polynomial `p = Σᵢ y^{p[i]}` (positions forward, directions backward; Niu–Spivak). Wiring = morphisms in **Poly**; hierarchy = the operad of wiring diagrams; a Moore machine is a lens; *a polynomial comonoid is a category*.
- **Interaction protocol**: session type = linear-logic proposition (Caires–Pfenning, Wadler). Agent honoring protocol = proof term; deadlock-freedom = cut elimination. Resources are linear: no contraction (no cloning capability), no weakening (no silent discard) unless typed so.

## 4. Boundary law

No agent contains its own totality. A self-model is licensed (helix: model one level up, Aczel-consistent as controlled hyperset, bisimulation as sameness); a *total* self-model — the agent containing its own containment, the registry of all registries including itself — is Girard's `Type : Type`, and detonates. Design consequence: introspection stratifies (`meta` observes `object`, never itself in full), federation reflects (Feferman elementary substructure), nothing totalizes.

## 5. Inference stance (optional stratum)

A Bayesian agent = Bayesian lens: forward = predictive model, backward = update on error; active inference = statistical game over Poly minimizing free energy (Smithe — program-level, flagged as research frontier, not settled theorem).

## 6. Conformance checklist

1. `Σ`, `B`, `λ` declared explicitly; rules in GSOS format (else congruence unproven).
2. All state distinctions observable via `B` (no svabhāva).
3. Effects typed by `T`; handlers total on the theory's operations.
4. Protocols session-typed; resources linear where physical.
5. Self-reference climbs a level; no fixed point of the totality.
6. Every skill invoked is a morphism in the skill category (see `skills/README.md`) — the agent is the runtime of the skill algebra, not its owner.

*The agent is the jam, not the score: syntax proposes, observation disposes, the distributive law keeps them honest.*
