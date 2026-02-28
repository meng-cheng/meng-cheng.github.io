---
title: "Trivializing group cohomology SPT phases"
date: 2026-02-26
permalink: /posts/2026/02/trivializing-group-cohomology-spt/
tags:
  - math
---

Phases of invertible topological quantum field theories with a global symmetry $G$ are known to be classified by (the Anderson dual of) cobordism. More precisely, for bosonic theories in $d$ spacetime dimensions, the group of invertible phases with unitary $G$ symmetry is $h^d(G)=(D\Omega^{\rm SO})_d(BG)$ ($D$ stands for the Anderson dual). An earlier attempt to the classification for $G$ is unitary is the group cohomology $\mathcal{H}^d(G, \mathrm{U}(1))$. 
It was noted in [arXiv:1403.1467](https://arxiv.org/abs/1403.1467) that in general the homomorphism from $\mathcal{H}^d(G, \mathrm{U}(1))$ to $h^d(G)$ is neither surjective nor injective. That is, on one hand there are "beyond group-cohomology" SPT phases, which exist in $d=4$ for $G=\mathbb{Z}_2^{\mathsf{T}}$ (anti-unitary $\mathbb{Z}_2$), and $d=5$ for $G=\mathbb{Z}_2$. On the other hand, the map can have nontrivial kernel: a nontrivial element of $\mathcal{H}^d(G, \mathrm{U}(1))$ may actually correspond to a trivial SPT phase. The latter phenomenon only occurs for $d\geq 7$, and the simplest group is $G=\mathbb{Z}_3\times \mathbb{Z}_3$. 

In this note we give a physical explanation of the minimal example with $G=\mathbb{Z}_3\times \mathbb{Z}_3$ in $d=7$.

This problem is best understood using the so-called decorated domain wall construction, which gives a physical interpretation of the Atiyah-Hirzebruch spectral sequence (AHSS) for cobordism. Let us briefly review AHSS in a slightly more general setup. Suppose the symmetry group sits in a short-exact sequence $1\rightarrow A \rightarrow G \rightarrow Q\rightarrow 1$ (so $G/A=Q$). Then the $E_2$ page of AHSS consists of

$$E_2^{p,q}=\mathcal{H}^p(G, h^q(BA)),$$

where $p,q$ are non-negative integers and $p+q=d$.

For the computation of $h^d(BG)$, we can just set $A=\mathbb{Z}_1$. The relevant groups of invertible phases in low dimensions up to $d=5$:

$$\begin{aligned}
    h^1 &=\mathbb{Z}_1,\\ h^2 &=\mathbb{Z}_1,\\ h^3&=\mathbb{Z},\\
    h^4&=\mathbb{Z}_1,\\
    h^5&=\mathbb{Z}_2.
\end{aligned}$$

There is a similar spectral sequence (London-Hochschild-Serre) for group cohomology, with the $E_2$ page given by

$$E_2^{p,q}=\mathcal{H}^p(G, \mathcal{H}^q(A, \mathrm{U}(1))).$$

If $G=A\times Q$ then the spectral sequence just reduces to the Künneth formula. For $G=\mathbb{Z}_3\times \mathbb{Z}_3$ we get

$$\mathcal{H}^7(\mathbb{Z}_3\times \mathbb{Z}_3, \mathrm{U}(1))=\mathbb{Z}_3^3.$$

Here one of the $\mathbb{Z}_3$ factor is given by $\mathcal{H}^2(\mathbb{Z}_3, \mathcal{H}^5(\mathbb{Z}_3,\mathrm{U}(1)))$.

Now we compute the corresponding term in the AHSS of cobordism: $\mathcal{H}^2(\mathbb{Z}_3, h^5(\mathbb{Z}_3))$.

First, we need to find $\Omega^{\rm SO}_5(\mathbb{Z}_3)$. We again use the AHSS. The nontrivial terms on the $E_2$ page has

$$\mathcal{H}^2(\mathbb{Z}_3, h^3)=\mathcal{H}^2(\mathbb{Z}_3, \mathbb{Z})=\mathbb{Z}_3, \quad \mathcal{H}^5(\mathbb{Z}_3, \mathrm{U}(1))=\mathbb{Z}_3.$$

The first term is the "beyond group-cohomology" SPTs. One can show that the $E_2$ page already converges to $E_\infty$, but interestingly, in this case there is nontrivial extension:

$$1\rightarrow \mathcal{H}^5(\mathbb{Z}_3, \mathrm{U}(1))\rightarrow h^5(\mathbb{Z}_3)\rightarrow\mathcal{H}^2(\mathbb{Z}_3, h^3)\rightarrow 1.$$

Therefore $h^5(\mathbb{Z}_3)=\mathbb{Z}_9$. In plain words, stacking three copies of the nontrivial "beyond cohomology" SPTs yields a nontrivial "within cohomology" SPT.

Using this fact, we can now compute the $E_2^{2,5}$ for $h^7(\mathbb{Z}_3^2)$:

$$\mathcal{H}^2(\mathbb{Z}_3, h^5(\mathbb{Z}_3)) = \mathcal{H}^2(\mathbb{Z}_3, \mathbb{Z}_9\times \mathbb{Z}_2) = \mathcal{H}^2(\mathbb{Z}_3, \mathbb{Z}_9)=\mathbb{Z}_3.$$

It is instructive to write down the cocycles explicitly. Denote the elements of $\mathbb{Z}_3$ by $a\in\{0,1,2\}$, and the generator of $h^5(\mathbb{Z}_3)$ by $x$. Then the 2-cocycle can be written as

$$\omega(a,b)=x^{n\frac{a+b-[a+b]_3}{3}}.$$

where we can take $n=0,1,2$. If $n=3$, $x^3$ is the generator of the group-cohomology SPTs, and $\omega(a,b)$ is a coboundary.

So the key fact is the nontrivial extension of $\mathbb{Z}_3$ SPTs in 5 dimensions. It can be further traced back to the following remarkable fact: take three copies of $(E_8)_1$ chiral CFTs. The $\mathbb{Z}_3$ cyclic permutation symmetry has a nontrivial 't Hooft anomaly.
