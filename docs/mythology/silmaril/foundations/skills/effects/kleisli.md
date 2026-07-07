# skill: effects/kleisli
**Signature** `Sk_T a b := a → T b`, `T` a strong monad; composition `>=>`.
**Fibers** state `S⇒(−×S)` | nondet `P` | probability `D` | failure `−+E`
| control `(−→R)→R`.
**Semantics** Moggi: programs form the Kleisli category. Effects presented
as Lawvere theory (ops+eqs); **handler** = homomorphism from the free model
(Eilenberg–Moore). Handling is interpretation, not interception.
**Law** Handlers are total on the theory's operations; unhandled operation
= type error, not runtime surprise.
**Binding** Query retry (failure fiber), sampling walks (D), speculative
traversal (P) — one schema, semiring/monad swapped per fiber.
