# skill: core/compose
**Signature** `(>>>) : Sk a b → Sk b c → Sk a c`
**Semantics** Morphism composition; in Kleisli fibers, `f >=> g = μ ∘ T g ∘ f`.
**Laws** Associativity; `arr id` unital. Postcondition of `f` must equal
precondition of `g` — type mismatch is refusal, not coercion.
**Binding** A GraphAtlas pipeline is a composite morphism; its provenance
is the ℕ[X] product of stage annotations (see provenance/semiring.md).
