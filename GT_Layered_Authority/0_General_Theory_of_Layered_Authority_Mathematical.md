# General Theory of Layered Authority
## Mathematical Spine for the Six-Layer Fixed Authority Cosmology


**Author:** Jeremy H. Carroll
**Version:** v1.0 Pre-Print
**Status:** publication spine
**Date:** May 2026

---

## Publication Main

> All files are available open-source on https://github.com/dbccpage/general_theory_of_finite_obstruction_calculus

> This file is the publication-facing spine extracted from the working tome. Full proofs are in `2_Layered_Authority_Proof_Archive.md`. 

---

# Abstract

This paper formalizes the six-layer fixed authority cosmology as a typed finite-authority stack. The central claim is not that all truth is finite, nor that every domain already has a known finite verifier. The central claim is narrower:

\[
\boxed{
\text{Operational authority exists only as terminalized, certified finite descent.}
}
\]

The governing normal form is the Kleisli composite

\[
\boxed{
\Pi^\sharp
=
\tau^\sharp
\circ_K
\operatorname{FOC}^\sharp
\circ_K
D^\sharp
\circ_K
\rho^\sharp
\circ_K
\mathcal R^\sharp
:
X\to \mathbb T+\mathbb F.
}
\]

A proposal is authority-bearing exactly when this composite returns an authority terminal:

\[
\boxed{
\mathsf{Auth}(x)
\iff
\exists t\in \mathbb T_{\mathsf{auth}},
\Pi^\sharp(x)=\mathsf{inl}(t).
}
\]

The six layers are not six sources of authority. They are six conserved obligations: finite obstruction, finite descent authority, certified representation transport, completion comparison, continuum shadow, and residual closure.

---

# 0. Governing Rule

The stack begins with the primitive rule:

\[
\boxed{
\text{Difference is primitive; sameness is certified zero-difference.}
}
\]

Thus identity, equivalence, transport, completion, and closure are never silently assumed. They must be certified inside a declared regime. Failure at any layer is not automatically disproof. It is one of:

- a typed refusal,
- an unresolved boundary,
- a non-authority terminal,
- a demand for fresh descent,
- or a licensed residual.

The operational slogan is:

\[
\boxed{
\text{No descent, no authority. No certificate, no transport. No terminal, no promotion.}
}
\]

---

# 1. The Base Arena: \(\mathbf{FAS}\)

Let \(\mathbf{FAS}\) denote the 2-category of finite authority systems.

## 1.1 Objects

Objects are finite authority pipelines

\[
\mathcal F
=
(
X,
\mathcal R,
\rho,
D,
V,
\tau,
\mathbb T,
\mathbb F,
\mathsf{Cert},
\mathsf{Ref}
).
\]

Here:

| Symbol | Role |
|---|---|
| \(X\) | proposal/input domain |
| \(\mathcal R\) | representation gate |
| \(\rho\) | routing map |
| \(D\) | finite descent compiler |
| \(V\) | verifier |
| \(\operatorname{FOC}\) | obstruction-calculus realization of \(V\), when available |
| \(\tau\) | terminalizer |
| \(\mathbb T\) | closed terminal outcomes |
| \(\mathbb F\) | typed refusals |
| \(\mathsf{Cert}\) | admissible certificates |
| \(\mathsf{Ref}\) | refusal semantics |

## 1.2 1-cells

A 1-cell

\[
F:\mathcal F\to\mathcal G
\]

is a lawful pipeline or representation morphism. If it claims to preserve authority, it must carry a descent-compatibility 2-cell:

\[
\boxed{
\chi_F:D_{\mathcal G}F\Rightarrow \bar F D_{\mathcal F}.
}
\]

No anonymous representation shift is authority-preserving. A lossy morphism must return a loss ledger:

\[
\mathsf{Loss}(F)
=
(
\mathsf{erased},
\mathsf{identified},
\mathsf{approximated},
\mathsf{unresolved}
).
\]

## 1.3 2-cells

A 2-cell is a certificate witness

\[
\alpha:F\Rightarrow G
\]

that preserves the relevant representation, descent, verification, and terminal semantics up to declared refinement or typed refusal.

The fundamental transport law is:

\[
\boxed{
\text{No pasted certificate, no authority transport.}
}
\]

---

# 2. The Exception Monad and Kleisli Pipeline

Authority stages are partial in ordinary language, but total in the exception/refusal monad

\[
M(Y)=Y+\mathbb F.
\]

Each stage is a Kleisli arrow:

\[
\mathcal R^\sharp:X\to \mathcal C+\mathbb F,
\]

\[
\rho^\sharp:\mathcal C\to\mathcal S+\mathbb F,
\]

\[
D^\sharp:\mathcal S\to\mathcal P+\mathbb F,
\]

\[
V^\sharp:\mathcal P\to\mathbb V+\mathbb F,
\]

\[
\tau^\sharp:\mathbb V\to\mathbb T+\mathbb F.
\]

The total terminal-preserving procedure is

\[
\boxed{
\Pi_S^\sharp
=
\tau^\sharp\circ_K V^\sharp\circ_KD^\sharp\circ_K\rho^\sharp\circ_K\mathcal R^\sharp.
}
\]

When \(V\) is realized by finite obstruction calculus, the strongest form is

\[
\boxed{
\Pi_S^\sharp
=
\tau^\sharp\circ_K\operatorname{FOC}^\sharp\circ_KD^\sharp\circ_K\rho^\sharp\circ_K\mathcal R^\sharp.
}
\]

---

# 3. Soundness Class

A system \(S\) belongs to \(\mathbf{AuthSys}_{\mathrm{sound}}\) iff it satisfies the anti-cheat axioms below.

## A0 — Finite operational signature

\(S\) has a finite input signature \(\mathcal P\), an admissible representation grammar \(\mathcal G\), and a finitely enumerable set of admissible representation morphisms \(\mathcal M\).

## A1 — Representation necessity

\[
\boxed{
\mathsf{Auth}_S(x)\Rightarrow\mathcal R(x)\downarrow.
}
\]

## A2 — Certified representation transport

Every authority-preserving representation change requires a typed morphism and a certificate \(\chi_F\).

## A3 — Finite replay requirement

\[
\boxed{
\mathsf{Promote}_S(x)
\Rightarrow
D(\rho(\mathcal R(x)))\downarrow
\wedge
V(D(\rho(\mathcal R(x))))\downarrow.
}
\]

## A4 — Weak terminal totality

Every completed verification attempt terminates into the closed terminal set \(\mathbb T\).

## A5 — Non-promotion of non-authority states

\[
\boxed{
\tau(V(D(\rho(\mathcal R(x)))))\notin\mathbb T_{\mathsf{auth}}
\Rightarrow
\neg\mathsf{Auth}_S(x).
}
\]

## A6 — Authority requires promotion path

\[
\boxed{
\mathsf{Auth}_S(x)\Rightarrow\mathsf{Promote}_S(x).
}
\]

## A7 — No shadow veto

\[
\boxed{
\exists t\in\mathbb T_{\mathsf{auth}},
\Pi_S^\sharp(x)=\mathsf{inl}(t)
\Rightarrow
\mathsf{Auth}_S(x).
}
\]

This axiom forbids a hidden post-terminal veto layer.

---

# 4. Authority Characterization Theorem

## Theorem 4.1

If \(S\in\mathbf{AuthSys}_{\mathrm{sound}}\), then

\[
\boxed{
\forall x,\quad
\mathsf{Auth}_S(x)
\iff
\exists t\in\mathbb T_{\mathsf{auth}},
\Pi_S^\sharp(x)=\mathsf{inl}(t).
}
\]

## Proof sketch

Necessity follows from A1, A3, A5, and A6: authority requires representation, finite descent, replayable verification, and an authority-bearing terminal. Sufficiency follows from A7: if the declared pipeline returns an authority terminal, the system must recognize it as authority.

Thus authority is not a property of a proposal, representation, completion, or continuum object by itself. Authority is the terminal status of the declared composite.

Full proof: see Proof Archive, Sections 11--18.

---

# 5. Homological Verifier Spine: Finite Obstruction Calculus

The local verifier is a finite obstruction calculus.

An obstruction packet is

\[
\mathcal M
=
(
\mathcal T,
\mathcal C,
\rho,
C^\bullet,
\omega,
p,
\mathcal K,
\Lambda
)
\]

with finite cochain complex

\[
\boxed{
C^0\xrightarrow{d_0}C^1\xrightarrow{d_1}C^2,
\qquad d_1d_0=0.
}
\]

Define:

\[
B^1=\operatorname{im}(d_0)
\]

\[
Q^1=C^1/B^1
\]

\[
\bar d_1:Q^1\to C^2,
\qquad
\bar d_1([x])=d_1x
\]

\[
H^1=\ker(\bar d_1)\cong\ker(d_1)/\operatorname{im}(d_0).
\]

The obstruction norm is

\[
\boxed{
\Phi([x])=
\inf_{\alpha\in C^0}\|x-d_0\alpha\|_{1,\omega}.
}
\]

Interpretation:

| Object | Meaning |
|---|---|
| \(B^1\) | exact repair image |
| \(Q^1\) | quotient obstruction space |
| \(\Phi\) | obstruction mass |
| \(\bar d_1\) | closure defect |
| \(H^1\) | closed non-exact residual sector |
| \(w=(x,y,c)\) | context-visible non-congruence witness |
| \(\mathcal K\) | replay certificate class |
| \(\Lambda\) | lift/refusal/budget discipline |

## Theorem 5.1 — Root Authority--Obstruction Factorization

For a FOC-refined sound system and a descended packet \(p(x)\in C^1\):

\[
\boxed{
[p(x)]=0\in Q^1\Rightarrow\mathsf{ExactAuthority}(x).
}
\]

\[
\boxed{
[p(x)]\neq0\in Q^1\Rightarrow\neg\mathsf{ExactAuthority}(x).
}
\]

Nonzero obstruction may still terminalize as survivor, licensed lift, hold, budget, open obstruction, or typed refusal. It does not authorize exactness.

Full proof: Proof Archive, Section 11.

---

# 6. FDA--FOC Refinement

Finite Descent Authority supplies the global authority doctrine:

\[
\boxed{
\mathsf{Auth}=\tau\circ V\circ D.
}
\]

FOC supplies the local verifier. The refinement is lawful only when the FDA packet is FOC-realized.

A descent packet is the dependent record

\[
P_s=(K_s,E_s,V_s,\tau_s,\Lambda_s).
\]

FOC realizes \(V_s\) when it supplies an obstruction packet

\[
\mathcal G_s=(K_s,\mathcal C_s,\rho_s,C_s^\bullet,E_s,\mathcal O_s,\mathcal K_s,\Lambda_s)
\]

with:

1. same carrier,
2. same candidate class,
3. replayable certificate adequacy,
4. extensional verifier agreement,
5. output-fiber preservation,
6. residual typing,
7. terminal compatibility.

## Theorem 6.1 — FDA--FOC Refinement

If every descended packet used by \(S\) is FOC-realized, then

\[
\boxed{
\tau_s^\sharp\circ_KV_s^\sharp
=
\tau_s^\sharp\circ_K\operatorname{FOC}_s^\sharp
}
\]

on all FOC-realized packets. Consequently,

\[
\boxed{
\mathsf{Auth}_S(x)
\iff
\exists t\in\mathbb T_{\mathsf{auth}},
(\tau^\sharp\circ_K\operatorname{FOC}^\sharp\circ_KD^\sharp\circ_K\rho^\sharp\circ_K\mathcal R^\sharp)(x)=\mathsf{inl}(t).
}
\]

Full proof: Proof Archive, Section 12.

---

# 7. The Six-Layer Doctrine Tower

The full tower is

\[
\boxed{
\mathsf{GTOC}
\xrightarrow{i_0}
\mathsf{GTFDA}
\xrightarrow{i_1}
\mathsf{GTMUR}
\xrightarrow{i_2}
\mathsf{GTOR}
\xrightarrow{i_3}
\mathsf{GTTC}
\xrightarrow{i_4}
\mathsf{GTTA}.
}
\]

Under the minimal no-identification doctrine,

\[
\boxed{
A\equiv B
\text{ only if }A\text{ and }B\text{ have the same type, inputs, outputs, failure terminals, and laws.}
}
\]

Therefore:

\[
\boxed{
N_{\mathrm{meta}}=6.
}
\]

## 7.1 The six conserved roles

- **GTOC / Obstruction:** objects \(Q^1,\Phi,\Gamma,H^1,w,\mathcal K,\Lambda\); failure terminal `NoObstructionKernel`.
- **GTFDA / Authority:** terminalized finite descent \(\Pi^\sharp:X\to\mathbb T+\mathbb F\); failure terminal `NoAuthoritySemantics`.
- **GTMUR / Transport:** descent-compatible certificate \(\chi_F:D_BF\Rightarrow\bar FD_A\); failure terminal `TransportViolation`.
- **GTOR / Completion comparison:** comparison objects, limits, pullbacks, and weak-terminal envelopes; failure terminal `NoCompletionComparison`.
- **GTTC / Continuum shadow:** finite shadow tower \(\{A_\lambda,\pi_\lambda,\chi_{\lambda\mu}\}\); failure terminal `NoFiniteShadow`.
- **GTTA / Residual closure:** closure residue terminal \(\operatorname{Close}_\Lambda(X)\) and \(\mathsf{TypedAnomalon}_\Lambda(X)\); failure terminal `NoResidualTerminal`.

None of these roles may be deleted without losing a type-specific obligation.

---

# 8. Higher-Categorical Normal Form

There is a bicategory of doctrine stacks

\[
\mathbf{DocStack}_{\partial}
\]

whose objects are doctrine layers or stacks

\[
\mathcal D
=
(
\mathcal C,
\mathcal R,
\rho,
D,
V,
\tau,
\mathbb T,
\mathbb F,
\chi,
\Lambda
).
\]

A lawful 1-morphism

\[
F:\mathcal D\to\mathcal E
\]

may embed, refine, quotient, approximate, lift, or reinterpret. If it transports authority, it must exhibit

\[
\boxed{
\chi_F:D_{\mathcal E}F\Rightarrow\bar F D_{\mathcal D}.
}
\]

A 2-morphism

\[
\alpha:F\Rightarrow G
\]

is a certified comparison preserving terminalized descent. The core coherence condition is

\[
\boxed{
\tau_{\mathcal E}\operatorname{FOC}_{\mathcal E}D_{\mathcal E}F
\Rightarrow
\tau_{\mathcal E}\bar F\operatorname{FOC}_{\mathcal D}D_{\mathcal D}.
}
\]

## Theorem 8.1 — Higher-Categorical Normal Form

The six-layer tower admits the normal form

\[
\boxed{
\Pi^\sharp
=
\tau^\sharp\circ_K\operatorname{FOC}^\sharp\circ_KD^\sharp\circ_K\rho^\sharp\circ_K\mathcal R^\sharp.
}
\]

The upper layers do not alter this authority normal form. They add transport, comparison, continuum shadow, and residual closure obligations around it.

Full proof: Proof Archive, Section 30.

---

# 9. Dependent Type and HoTT Reading

The stack can be read as a proof-relevant dependent type theory for authority.

## 9.1 Authority as a dependent type

\[
\boxed{
\mathsf{Authority}(x)
:=
\Sigma(t:\mathbb T_{\mathsf{auth}})\bigl(\Pi^\sharp(x)=\mathsf{inl}(t)\bigr).
}
\]

An authority result is not merely a Boolean. It is a dependent pair \((t,\pi)\), where \(t\) is an authority terminal and \(\pi\) proves that the pipeline produced it.

## 9.2 Refusal as a dependent type

\[
\boxed{
\mathsf{Refuse}(x)
:=
\Sigma(\phi:\mathbb F)\bigl(\Pi^\sharp(x)=\mathsf{inr}(\phi)\bigr).
}
\]

Thus non-authority is not automatically contradiction. It is often an inhabited refusal type.

## 9.3 Descent packet as dependent record

\[
\boxed{
\mathsf{Packet}(s)
:=
\Sigma(K:\mathsf{Carrier}(s))
\Sigma(E:\mathsf{EvalClass}(K))
\Sigma(V:\mathsf{Verifier}(K,E))
\Sigma(\tau:\mathsf{Terminalizer}(V))
\mathsf{LiftDiscipline}(K,E,V,\tau).
}
\]

Deleting a field makes the packet ill-typed.

## 9.4 HoTT relation

HoTT transports evidence along paths. FDA transports authority only along certified morphisms:

\[
\boxed{
\mathsf{TransportAuth}_F(x)\Rightarrow\chi_F(x)\downarrow.
}
\]

This is a stricter, finite, replayable analogue of transport. Univalence is not accepted as unrestricted authority transport. The admissible analogue is certified \(\chi\)-univalence: equivalence preserves authority only when equipped with a descent-compatible certificate.

Full discussion: Proof Archive, Sections 29 and 32.

---

# 10. Upper-Layer Non-Creation

No layer above GTFDA creates authority.

\[
\boxed{
L>\mathsf{GTFDA}
\Rightarrow
L\text{ may organize, transport, compare, complete, shadow, or expose residue, but may not create authority.}
}
\]

Equivalently:

\[
\boxed{
X\in L\not\Rightarrow\mathsf{Auth}(X).
}
\]

Authority may appear in an upper layer only when there is certified descent back to the finite authority normal form.

## 10.1 GTMUR

Representation does not authorize:

\[
\boxed{
\mathcal R(x)\not\Rightarrow\mathsf{Auth}(x).
}
\]

Transport requires \(\chi_F\). Loss requires a loss ledger.

## 10.2 GTOR

Completion does not authorize:

\[
\boxed{
X\in\operatorname{Comp}(\mathsf{GTMUR})
\not\Rightarrow
\mathsf{Auth}(X).
}
\]

Products, pullbacks, limits, comparison objects, and weak terminal envelopes require descent certificates before they become authority-bearing.

## 10.3 GTTC

Continuum coherence does not authorize:

\[
\boxed{
X\simeq\lim_{\lambda\in\Lambda}i_3(A_\lambda)
\not\Rightarrow
\mathsf{Auth}_{\mathsf{GTTC}}(X).
}
\]

Authority in GTTC requires a cofinal system of authorized finite shadows:

\[
\boxed{
\exists\Lambda_0\subseteq\Lambda\text{ cofinal such that }
\forall\lambda\in\Lambda_0,
\mathsf{Auth}_{\mathsf{GTOR}}(A_\lambda)\downarrow
\text{ and }
\chi_{\lambda\mu}\downarrow.
}
\]

## 10.4 GTTA

The anomalon is typed non-absorption, not origin:

\[
\boxed{
\mathsf{TypedAnomalon}_\Lambda(X)
\not\Rightarrow
\mathsf{OriginOfDifference}(X).
}
\]

A typed anomalon exists only after a licensed closure attempt:

\[
\boxed{
\operatorname{Close}_\Lambda(X)=\mathsf{NonAbsorb}(a)
\Rightarrow
\mathsf{TypedAnomalon}_\Lambda(X)=a.
}
\]

Full proofs: Proof Archive, Sections 20, 24, 28, and 31.

---

# 11. The Three Counts of \(N\)

The framework has three distinct finite counts.

## 11.1 Core pipeline count

\[
\boxed{
N_{\mathrm{FDA}}=5.
}
\]

This counts the operational authority stages:

\[
(\mathcal R,\rho,D,V,\tau).
\]

## 11.2 Meta-role count

\[
\boxed{
N_{\mathrm{meta}}=6.
}
\]

This counts the irreducible tower obligations:

\[
(\mathsf O,\mathsf A,\mathsf T,\mathsf C,\mathsf S,\mathsf R).
\]

## 11.3 Proof-certificate length

\[
\boxed{
N_{\mathrm{proof}}(\pi)=|\pi|.
}
\]

This counts a particular finite proof certificate, if such a certificate exists.

The key separation is:

\[
\boxed{
N_{\mathrm{meta}}\text{ counts the machine.}
}
\]

\[
\boxed{
N_{\mathrm{proof}}\text{ counts the certificate the machine verifies.}
}
\]

Full proof: Proof Archive, Section 27.

---

# 12. Main Theorem: Authority Conservation

## Theorem 12.1 — Authority Conservation

Let

\[
\mathcal S_6
=
(
\mathsf{GTOC},
\mathsf{GTFDA},
\mathsf{GTMUR},
\mathsf{GTOR},
\mathsf{GTTC},
\mathsf{GTTA}
)
\]

be a sound six-layer doctrine stack in \(\mathbf{DocStack}_{\partial}\). Then, for every proposal \(x\):

\[
\boxed{
\mathsf{Auth}(x)
\iff
\exists t\in\mathbb T_{\mathsf{auth}},
(\tau^\sharp\circ_K\operatorname{FOC}^\sharp\circ_KD^\sharp\circ_K\rho^\sharp\circ_K\mathcal R^\sharp)(x)=\mathsf{inl}(t).
}
\]

Moreover, any operation in \(\mathsf{GTMUR}\), \(\mathsf{GTOR}\), \(\mathsf{GTTC}\), or \(\mathsf{GTTA}\) preserves authority only by exhibiting a descent-compatible certificate back into this normal form.

## Proof sketch

1. A1--A7 give the authority characterization theorem.
2. The descent compiler supplies well-typed packets \(P_s=(K_s,E_s,V_s,\tau_s,\Lambda_s)\).
3. FOC realizes \(V\) on obstruction-realized packets.
4. \(Q^1\) separates exact authority from obstruction at the verification stage.
5. \(\chi_F\) is required for representation transport.
6. Completion, continuum, and closure layers are authority-noncreating by the upper-layer non-creation theorem.
7. Therefore all legitimate authority in the six-layer stack factors through the same finite terminal normal form.

Full proof dependencies: Proof Archive, Sections 11--34.

---

# 13. Publication Split

The strongest publication order is two papers plus a proof archive.

## Paper I — Layer Factorization and Authority Conservation

This paper should contain:

1. \(\mathbf{FAS}\) and \(\mathbf{DocStack}_{\partial}\),
2. the exception/Kleisli normal form,
3. A0--A7,
4. Authority Characterization,
5. the six meta-roles,
6. the upper-layer non-creation theorem,
7. Authority Conservation.

Its core formula is:

\[
\boxed{
\mathsf{Auth}
=
\tau\circ\operatorname{FOC}\circ D\circ\rho\circ\mathcal R.
}
\]

## Paper II — Finite Obstruction and Descent Authority

This paper should contain:

1. finite cochain packets,
2. \(Q^1=C^1/\operatorname{im}(d_0)\),
3. \(H^1=\ker(\bar d_1)\),
4. \(\Phi\) and certificates,
5. FOC realization of FDA verifier packets,
6. exact authority as zero obstruction,
7. nonzero obstruction as survivor/open/lift/refusal terminal.

Its core formula is:

\[
\boxed{
[p]=0\in Q^1
\iff
\mathsf{ExactAuthority}(p)
}
\]

on descended, FOC-realized packets.

## Companion — Proof Archive

The proof archive should hold all long lemmas, applications, caveats, and future proof targets. That keeps the main paper readable.

---

# 14. Non-Claims

This spine does not claim:

1. that every truth is finite;
2. that every domain already has a known descent map;
3. that global geometry, completion, or continuum structure is useless;
4. that the anomalon is the origin of difference;
5. that representation, completion, or coherence creates authority;
6. that unsolved mathematical problems have already been solved;
7. that a proof certificate exists before it is produced.

It claims only:

\[
\boxed{
\text{Operational authority, as defined here, requires representation, routing, finite descent, verification, terminalization, and certified transport where applicable.}
}
\]

---

# 15. Closing Normal Form

The complete spine fits on one line:

\[
\boxed{
\begin{gathered}
\mathbf{FAS}\text{ supplies the arena;}\\
\operatorname{FOC}\text{ supplies the finite homological verifier;}\\
\mathbf{DocStack}_{\partial}\text{ supplies the higher-categorical tower;}\\
\mathsf{Authority}(x)=\Sigma(t:\mathbb T_{\mathsf{auth}})(\Pi^\sharp(x)=\mathsf{inl}(t))\text{ supplies the HoTT/dependent-type reading;}\\
\mathsf{GTMUR},\mathsf{GTOR},\mathsf{GTTC},\mathsf{GTTA}\text{ organize without creating authority.}
\end{gathered}
}
\]

\[
\boxed{
\text{There may be many worlds, representations, completions, and residues. But authority must descend.}
}
\]
