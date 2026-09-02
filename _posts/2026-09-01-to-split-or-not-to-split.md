---
title: 'To split or not to split'
date: 2026-09-01
tags:
  - math
---

"Anyon condensation" (or better, "gauging one-form symmetry". The reason is explained [here](https://arxiv.org/abs/2603.00245)) is a mathematical operation that relates different 3d topological quantum field theories (TQFTs).  When the condensed anyons are Abelian bosons, the effect on topological lines (equivalently, anyon types) is often described as a "three-step procedure":

1. Remove all lines that braid nontrivially with the condensed lines.
2. Arrange the remaining lines into orbits under fusion with the condensed lines. Lines in the same orbit are identified.
3. If a (non-Abelian) line is invariant under fusion with nontrivial condensed lines, it "splits" into multiple descendant lines.

I recently encountered an example where naively applying the rules, especially rule 3, leads to incorrect results (there is no problem with rules 1 and 2). The upshot is that if the condensed bosons form a cyclic group under fusion, then the procedure can be safely applied. Otherwise the procedure does not always work.

The example can be described in several different ways. Most compactly, it is the TQFT of the $\mathrm{Spin}(8)_{-2}$ Chern-Simons theory. To understand the source of the problem, it is more useful to think of it as the $\bZ_2\times \bZ_2$ orbifold of ${\rm SU}(2)_1$. Here "orbifold" means gauging a zero-form symmetry. ${\rm SU}(2)_1$ has a single nontrivial line, which is the semion line. The $\bZ_2\times \bZ_2$ symmetry fractionalizes, in such a way that the semion carries the two-dimensional projective representation. Gauging this symmetry leads to our example. This description is slightly ambiguous, as we have not specified what Dijkgraaf-Witten term is used, but that does not affect the discussion.

To understand what is going on, we do not need to know the full details of the gauged theory (or $\mathrm{Spin}(8)_{-2}$). All we need to know is the following subcategory of lines, which is isomorphic to ${\rm Rep}(Q_8)$ as fusion category. Let us denote the lines in this subcategory by $1, b_1, b_2, b_3$ and $s$. $b_1$ and $b_2$ are Abelian bosons, which generate the $\bZ_2\times \bZ_2$ group that can be condensed, $s$ is a non-Abelian anyon with quantum dimension 2. The most important fusion rules are:

$$ s\times s = 1+b_1+b_2+b_3$$

$s$ has quantum dimension $d_s=2$, and is invariant under fusion with any $b_i$. Since it has trivial braiding with $b_i$'s, this whole subcategory survives the condensation. Then applying rule 3 naively would mean that $s$ should split into 4 lines, each with quantum dimension $1/2$, which is clearly possible.

*To be continued.*


