# skill: core/lift
**Signature** `arr : (a → b) → Sk a b`
**Semantics** The identity-on-objects functor `J: C → K` of the Freyd
category: embeds a pure function as an effect-free skill.
**Laws** `arr id = id`; `arr (g ∘ f) = arr f >>> arr g` (functoriality).
**Binding** Pure graph transforms (projection, relabel) enter GraphAtlas
pipelines only through `lift` — provenance-invisible by construction.
