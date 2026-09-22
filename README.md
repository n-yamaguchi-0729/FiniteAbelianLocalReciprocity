# Local class field theory in Lean 4.34.0

This repository is a thin submission interface for the finite norm-quotient
form of local class field theory proved in
[ClassFieldTheory](https://github.com/n-yamaguchi-0729/ClassFieldTheory/tree/01b4614ee76fa6f50e7f3ea3e1cff93b85693345).

The compared declaration is
`ClassFieldTheory.finiteAbelianLocalReciprocity_quotient`. For a finite
abelian extension `L / K` of a nonarchimedean local field, it states

```text
Kˣ / N_{L/K}(Lˣ) ≃ₜ* Gal(L/K).
```

The equivalence is an isomorphism of topological multiplicative groups. The
Challenge uses only Mathlib imports and gives concrete definitions of the
field norm, its image subgroup, and the quotient. `Solution.lean` imports the
proved declaration from the pinned CFT commit.

## Scope and the rest of the CFT development

The substantive CFT library separately proves:

- a continuous surjective finite Artin map with field-norm kernel in
  [`FiniteAbelianLocalReciprocity.lean`](https://github.com/n-yamaguchi-0729/ClassFieldTheory/blob/01b4614ee76fa6f50e7f3ea3e1cff93b85693345/Lean4/ClassFieldTheory/Theorems/LocalClassFieldTheory/FiniteAbelianLocalReciprocity.lean);
- a coherent family with norm kernels, tower compatibility, and arithmetic
  Frobenius normalization in
  [`FiniteAbelianLocalReciprocityFamilyArithmeticFrobenius.lean`](https://github.com/n-yamaguchi-0729/ClassFieldTheory/blob/01b4614ee76fa6f50e7f3ea3e1cff93b85693345/Lean4/ClassFieldTheory/Theorems/LocalClassFieldTheory/FiniteAbelianLocalReciprocityFamilyArithmeticFrobenius.lean);
- uniqueness of the normalized coherent family in
  [`FiniteAbelianLocalReciprocityFamilyExt.lean`](https://github.com/n-yamaguchi-0729/ClassFieldTheory/blob/01b4614ee76fa6f50e7f3ea3e1cff93b85693345/Lean4/ClassFieldTheory/Theorems/LocalClassFieldTheory/FiniteAbelianLocalReciprocityFamilyExt.lean);
- the local existence/classification theorem as an order isomorphism in
  [`FiniteAbelianLocalExistenceOrderIso.lean`](https://github.com/n-yamaguchi-0729/ClassFieldTheory/blob/01b4614ee76fa6f50e7f3ea3e1cff93b85693345/Lean4/ClassFieldTheory/Theorems/LocalClassFieldTheory/FiniteAbelianLocalExistenceOrderIso.lean);

## Files and verification

- `Challenge.lean`: the short Mathlib-only statement surface; its one `sorry`
  is the deliberate Comparator placeholder.
- `Solution.lean`: imports the proof from the exact pinned CFT commit.
- `comparator.json`: selects exactly one theorem.
- `formalization.yaml`: provenance, scope, source, and automation metadata.

The project uses Lean 4.34.0 and commits an exact dependency manifest. CI
builds both modules and runs the official full mechanical preflight at a
pinned revision. That check compares the declaration, audits its complete
source closure, and replays the proof with both Lean's kernel and NanoDa. The
one `sorry` in `Challenge.lean` is the deliberate statement placeholder;
`Solution.lean` imports the completed proof.

## Authorship and AI assistance

Astra GPT-6 Codex assisted with Lean development, statement review, and
preparation of this submission interface. Naganori Yamaguchi (山口永悟) is the
human author and responsible maintainer.

Licensed under Apache-2.0.
