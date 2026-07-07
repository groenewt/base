# skill: observe/coalgebra
**Signature** `obs : X → B X` for behavior functor `B`; skill = coalgebra hom.
**Semantics** Observation skills are morphisms into the final B-coalgebra;
equality of observed systems = bisimilarity, established coinductively.
Modal interface: coalgebraic modal logic (predicate liftings; Moss ∇) is
the query language canonically induced by `B` — modalities are measurements.
**Law** No skill may distinguish bisimilar states (observational univalence).
**Binding** GraphAtlas monitoring/lineage-watch skills observe; they never
read hidden state, because the conformance rule (AGENT.md §1) deleted it.
