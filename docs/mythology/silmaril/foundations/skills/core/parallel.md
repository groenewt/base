# skill: core/parallel
**Signature** `first : Sk a b → Sk (a ⊗ c) (b ⊗ c)`; derived `(***)`, `(&&&)`.
**Semantics** Premonoidal tensor: run on part of a structured capability,
thread the rest untouched. Full interchange `(f *** g) = (g' *** f')` holds
only in the centre (pure/commuting skills); effectful skills order.
**Laws** `first (arr f) = arr (f × id)`; sliding, association coherence.
**Binding** Federated fan-out across cluster nodes (trixie/graph/silmaril);
non-central skills serialize — the algebra records the causal order.
