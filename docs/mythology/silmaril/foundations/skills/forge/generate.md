# skill: forge/generate
**Signature** `forge : Signature F → (μF, F* ,λ) — language, library, law.`
**Semantics** Atomic contracts generate: initial algebra μF (Lambek forces
μF ≅ F(μF)); composite skills = terms of the free monad F*; attach behavior
functor B via GSOS law λ ⇒ the skill library is a **bialgebra**, and
bisimilarity of skills is a congruence: swap behaviorally-equal skills in
any pipeline, nothing observable changes.
**Law** COOK_LEMMA_00/01 discharged formally: every atom unique but
documented (generators), e2e reproduction via Yoneda from the atomic schema
base (density: every skill is a colimit of representable atomic probes).
**Binding** The Forge DSL triad F_math/F_lang/F_econ = three Lawvere-theory
presentations of one signature; skills/**/*.md above are its first unfolding.
