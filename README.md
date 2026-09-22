# Local class field theory in Lean 4.34.0

This repository presents the finite norm-quotient form of local class field
theory proved in
[ClassFieldTheory](https://github.com/n-yamaguchi-0729/ClassFieldTheory/tree/01b4614ee76fa6f50e7f3ea3e1cff93b85693345).

The compared declaration is
`ClassFieldTheory.finiteAbelianLocalReciprocity_quotient`. For a finite
abelian extension `L / K` of a nonarchimedean local field, it states

```text
Kˣ / N_{L/K}(Lˣ) ≃ₜ* Gal(L/K).
```

Here `≃ₜ*` is an isomorphism of topological multiplicative groups. The
Mathlib-only Challenge defines the field norm, its image subgroup, and the
quotient; the Solution imports the completed proof from the pinned CFT commit.

## Additional proved results

The same CFT development also proves:

- a continuous surjective finite Artin map with field-norm kernel in
  [`FiniteAbelianLocalReciprocity.lean`](https://github.com/n-yamaguchi-0729/ClassFieldTheory/blob/01b4614ee76fa6f50e7f3ea3e1cff93b85693345/Lean4/ClassFieldTheory/Theorems/LocalClassFieldTheory/FiniteAbelianLocalReciprocity.lean);
- a coherent family with norm kernels, tower compatibility, and arithmetic
  Frobenius normalization in
  [`FiniteAbelianLocalReciprocityFamilyArithmeticFrobenius.lean`](https://github.com/n-yamaguchi-0729/ClassFieldTheory/blob/01b4614ee76fa6f50e7f3ea3e1cff93b85693345/Lean4/ClassFieldTheory/Theorems/LocalClassFieldTheory/FiniteAbelianLocalReciprocityFamilyArithmeticFrobenius.lean);
- uniqueness of the normalized coherent family in
  [`FiniteAbelianLocalReciprocityFamilyExt.lean`](https://github.com/n-yamaguchi-0729/ClassFieldTheory/blob/01b4614ee76fa6f50e7f3ea3e1cff93b85693345/Lean4/ClassFieldTheory/Theorems/LocalClassFieldTheory/FiniteAbelianLocalReciprocityFamilyExt.lean);
- the local existence/classification theorem as an order isomorphism in
  [`FiniteAbelianLocalExistenceOrderIso.lean`](https://github.com/n-yamaguchi-0729/ClassFieldTheory/blob/01b4614ee76fa6f50e7f3ea3e1cff93b85693345/Lean4/ClassFieldTheory/Theorems/LocalClassFieldTheory/FiniteAbelianLocalExistenceOrderIso.lean).

The theorem placeholder in `Challenge.lean` is deliberate; `Solution.lean`
imports the completed proof.

## Authorship

Astra GPT-6 Codex assisted with Lean development, statement review, and
preparation of this submission interface. Naganori Yamaguchi (山口永悟) is the
human author and responsible maintainer.

Licensed under Apache-2.0.
