# skills/ — Skills as Composable Algebra

A **skill** is a morphism in a symmetric premonoidal category **Sk**:
objects = **capabilities** (typed interfaces: precondition ⊢ postcondition),
morphisms = skills, `∘` = sequencing, `⊗` = parallel resource use.

Formally **Sk** is an (enriched) **Freyd category**: identity-on-objects
`J: C → K` from a cartesian category of pure values into a premonoidal
category of effectful skills (Atkey; Jacobs–Heunen–Hasuo: an Arrow is a
monoid in bifunctors `C^op × C → V`, i.e. a profunctor monoid). Strong
monads ⊂ Freyd ⊂ Arrows: escalate structure only when feedback demands it.

**Generation (Forge).** Fix a primitive-capability signature functor `F`.
The skill language is the initial algebra `μF ≅ F(μF)` (Lambek: the fixed
point is forced, not chosen); the composite library is the free monad `F*`;
behavior attaches by a GSOS law, making every skill library a **bialgebra**
— the same structure as AGENT.md, one level down. Atomic contracts are the
generators; everything else is a forced extension.

**Laws** (hold in every file below): associativity of `∘`; functoriality of
`lift`; `first` coherence (sliding, exchange); ⊗ interchange up to the
premonoidal centre. A skill that violates its laws is not a skill; it is a
side effect wearing a name.

Tree:
- core/       — lift, compose, parallel (the arrow triad)
- effects/    — Kleisli skills per monad
- observe/    — coalgebraic observation, modal interface
- optics/     — bidirectional skills (get/put, play/coplay, Tambara)
- federate/   — sheaf gluing, global sections, obstructions
- provenance/ — semiring annotation, ℕ[X] universality
- games/      — equilibrium skills, compositional agency
- forge/      — generation of skills from atomic contracts
