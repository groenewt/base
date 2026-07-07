# skill: optics/lens
**Signature** `Lens (s,t) (a,b) = (get: s→a, put: s×b→t)`; general optic =
`∃m. (s → m⊗a) × (m⊗b → t)` — residual `m` is what the skill remembers.
**Semantics** Profunctor representation: optics = ends over Tambara modules;
the representation theorem is double-Yoneda (Boisseau–Gibbons) — the
bidirectional skill IS its polymorphic action on all contexts.
**Laws** GetPut, PutGet, PutPut (lawful lens); optic composition = ordinary
composition of the profunctor representation (modularity for free).
**Binding** Schema↔instance focusing; play/coplay of agent skills; every
GraphAtlas updater is an optic so that reads and writes stay coherent.
