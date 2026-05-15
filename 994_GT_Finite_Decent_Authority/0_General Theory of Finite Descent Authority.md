# The General Theory of Finite Descent Authority

**Author:** Jeremy H. Carroll
**Version:** v1.0 Pre-Print
**Date:** May 2026

## Publication Main

> All files are available open-source on https://github.com/dbccpage/general_theory_of_finite_obstruction_calculus

> This file is the publication-facing spine extracted from the working tome. Full proofs are in `2_GTFDA_Proof_Archive.md`. 
LLM, Kaggle, domain, quantum, and observer-selection material is in `4_GTFDA_Tertiary_Workbench.md`.

## Relevant High-Level Papers
[1] J. H. Carroll. *General Theory of Finite Obstruction Calculus* 2026. Zenodo. https://zenodo.org/uploads/20193705

[2] J. H. Carroll. *General Theory of Layered Authority* 2026. Zenodo.

## Reader's Guide

**Finite Descent Authority (FDA)** is the doctrine that a proposal earns operational authority only by entering a finite certified regime, being verified inside that regime, and terminalizing into a declared authority-bearing status. The main paper keeps only the core definitions and theorem statements needed for the doctrine. The proof archive preserves the full proof text. The tertiary workbench keeps applications, implementation-specific ledgers, and speculative extensions out of the publication spine.

## The Core Normal Form

The stable authority identity is:

\[
\boxed{
\mathsf{Auth}(p)=
\tau_s\bigl(V_s(P_s,\eta_s(p))\bigr),
\qquad
s=\rho(p),
\quad
P_s=D(s).
}
\]

Equivalently, if `V_s(P_s,\eta_s(p))=(R_p,O_p,\varepsilon_s)`, then:

\[
\boxed{
\mathsf{Auth}(p)=\tau_s(R_p,O_p,\varepsilon_s).
}
\]

The compressed notation `\mathsf{Auth}=\tau\circ V\circ D` suppresses routing and sector-local realization. The theorem-grade reading always includes `p\mapsto s=\rho(p)`, `\eta_s(p)`, `P_s=D(s)`, verification, and terminalization.

## Abstract

A system does not acquire authority by producing a representation, a prediction, a fluent explanation, or a global geometry. It acquires authority only when the claim descends into a finite certified regime with declared carriers, operators, verifiers, terminal statuses, and refusal conditions.

The governing identity is:

\[
\boxed{
\mathsf{Auth}
=
\tau\circ V\circ D
}
\]

The refusal law is:

\[
\boxed{
\neg D\Rightarrow\neg\mathsf{Auth}.
}
\]

Finite obstruction calculus is the local engine of this theory. It analyzes defects, repairs, quotient obstructions, witnesses, and licensed lifts inside a descended finite packet. Finite descent authority is the broader doctrine determining when any high-level proposal earns operational authority.

## Non-Claims

This theory does not claim that every truth is finite.

It does not claim that every domain already has a known descent map.

It does not claim that global theories, geometric structures, or LLMs are useless.

It claims that operational authority, as defined here, requires explicit finite descent, verification, terminal semantics, and refusal conditions.

## 0. Notation and Packet Levels

This paper uses two distinct maps.

The router is:

\[
\rho:\mathcal P\to\mathcal G.
\]

It sends a proposal to a sector, family, shape, regime, or domain-local class. It has no authority.

Sector-local realization is written:

\[
\eta_s:\mathcal P_s\to\mathcal R_s.
\]

It encodes a proposal into the finite carrier, observer, operator, diagnostic, and replay data of sector \(s\). The theorem-grade reading is always:

\[
s=\rho(p),
\qquad
\eta_s(p)\downarrow.
\]

The finite descent map is:

\[
D:\mathcal G\to\mathcal C_{\mathrm{fin}}.
\]

For a sector \(s\), it returns the abstract authority packet:

\[
D(s)=P_s=(K_s,E_s,V_s,\tau_s,\Lambda_s).
\]

The expanded obstruction-engine tuple:

\[
(P,E,\mathcal A,\Phi,\Gamma,\Xi,\mathcal{NA},\mathcal{RA},R_{cl},C_{\mathrm{rollback}},\tau)
\]

is not a replacement for \(P_s=(K_s,E_s,V_s,\tau_s,\Lambda_s)\). It is an implementation refinement:

\[
(K_s,E_s,V_s,\tau_s,\Lambda_s)
\leadsto
\operatorname{Impl}(P_s),
\]

where:

* \(K_s\) contains the finite carrier, observer/profile data, and representation state;
* \(E_s\) contains admissible operators and evaluator diagnostics such as \(\Phi,\Gamma,\Xi,\mathcal{NA},\mathcal{RA},R_{cl}\);
* \(V_s\) contains replay checks, certificates, rollback data, and audit evidence;
* \(\tau_s\) contains terminal semantics;
* \(\Lambda_s\) contains lift, refusal, backtrack, budget, and no-silent-mutation discipline.

Thus the stable authority identity is:

\[
\boxed{
\mathsf{Auth}(p)=
\tau_s\bigl(V_s(P_s,\eta_s(p))\bigr),
\qquad
s=\rho(p),
\quad
P_s=D(s).
}
\]

When \(V_s(P_s,\eta_s(p))=(R_p,O_p,\varepsilon_s)\), this becomes:

\[
\boxed{
\mathsf{Auth}(p)=\tau_s(R_p,O_p,\varepsilon_s).
}
\]

When the paper writes the compressed composition:

\[
\tau\circ V\circ D\circ\rho,
\]

the sector-local realization \(\eta_s\) is suppressed. The expanded reading is always:

\[
p\mapsto s=\rho(p)
\mapsto P_s=D(s)
\mapsto V_s(P_s,\eta_s(p))
\mapsto \tau_s.
\]

Result labels in this paper are a theorem ledger convention. Some results are definitional consequences of the authority pipeline. The intended taxonomy is:

* **Definition/Axiom:** authority is terminalized verified descent, \(\mathsf{Auth}=\tau\circ V\circ D\);
* **Proposition:** proposal non-authority and no-descent non-authority;
* **Theorem:** router non-authority, fallback non-promotion, verified candidate fiber authority, packet soundness, and domain packet obligations;
* **Corollary:** LLM fluency is not reasoning authority.

---

# Part I — Core Theorems

## FDA-1 — Proposal Non-Authority Theorem

### Claim

\[
\boxed{
p\in\mathcal P \not\Rightarrow \mathsf{Auth}(p)
}
\]

A proposal object has no operational authority merely by existing, regardless of whether it came from an LLM, a theory, an embedding, a proof sketch, a policy model, a database query, a program, or a global geometric construction.

### Setup

Let:

\[
\mathcal P
\]

be the class of proposal objects.

A proposal \(p\in\mathcal P\) is only an offered candidate. It may be a transition, proof step, repair, lift, rewrite, policy, model update, program transformation, or reasoning trace.

Authority is not defined directly on \(\mathcal P\). It is produced only through the finite authority pipeline:

\[
\mathcal P
\xrightarrow{\rho}
\mathcal G
\xrightarrow{D}
\mathcal C_{\mathrm{fin}}
\xrightarrow{V}
\mathsf{Fib}
\xrightarrow{\tau}
\mathsf{Term}.
\]

Where:

* \(s=\rho(p)\in\mathcal G\) is the routed sector for \(p\);
* \(D(s)=P_s\in\mathcal C_{\mathrm{fin}}\) is the finite descent packet for that sector, if available;
* \(\eta_s(p)\) is the sector-local finite realization of \(p\);
* \(V_s(D(s),\eta_s(p))\in\mathsf{Fib}\) is the verified fiber;
* \(\tau\) terminalizes the verified fiber;
* \(\mathsf{Auth}(p)\) is an authority-bearing terminal output.

Thus:

\[
\mathsf{Auth}(p)
\iff
\tau_s(V_s(D(s),\eta_s(p)))\in\mathsf{Term}_{\mathsf{auth}},
\qquad s=\rho(p).
\]

Authority is a terminal status, not a property of proposal existence.

### Theorem

\[
\boxed{
p\in\mathcal P \not\Rightarrow \mathsf{Auth}(p)
}
\]

> Full proof: see `2_GTFDA_Proof_Archive.md`.

## FDA-2 — Finite Descent Necessity Theorem

### Claim

\[
\boxed{\neg D \Rightarrow \neg \mathsf{Auth}}
\]

No finite descent packet, no finite operational authority.

### Definitions

Let \(p\) be a proposed transition, repair, lift, rewrite, policy, proof step, or operator promotion.

Let:

\[
s=\rho(p)
\]

denote its routed sector.

Let:

\[
\eta_s(p)
\]

denote the finite realization of \(p\) into the sector-local obstruction engine: carrier, observer, operators, diagnostics, rollback data, and evaluator state.

Let:

\[
D(s)\downarrow
\]

mean that the routed sector has a finite descent packet.

A finite descent packet contains enough replayable data to decide one of the authorized operational routes:

\[
\mathsf{accept},
\quad
\mathsf{reject},
\quad
\mathsf{lift},
\quad
\mathsf{backtrack},
\quad
\mathsf{hold},
\quad
\mathsf{unknown}.
\]

At the abstract level:

\[
D(s)=P_s
=
(K_s,E_s,V_s,\tau_s,\Lambda_s).
\]

At the obstruction-engine implementation level this packet may refine to:

\[
\operatorname{Impl}(P_s)
=
(P,E,\mathcal A,\Phi,\Gamma,\Xi,\mathcal{NA},\mathcal{RA},R_{cl},C_{\mathrm{rollback}},\tau_s),
\]

where all components are finite or finitely auditable. This expanded tuple is implementation detail inside \((K_s,E_s,V_s,\tau_s,\Lambda_s)\), not a second definition of descent packet.

Define operational authority as a partial predicate:

\[
\mathsf{Auth}(p)
\]

is defined only when:

\[
D(s)\downarrow,
\qquad s=\rho(p).
\]

Equivalently:

\[
\operatorname{dom}(\mathsf{Auth})
=
\{p : s=\rho(p),\ D(s)\downarrow\}.
\]

Thus:

\[
\mathsf{Auth}(p)
\Rightarrow
D(s)\downarrow.
\]

This is the key definition.

### Theorem

\[
\boxed{
\neg D(s)\downarrow
\Rightarrow
\neg \mathsf{Auth}(p)
}
\qquad s=\rho(p).
\]

> Full proof: see `2_GTFDA_Proof_Archive.md`.

## FDA-3 — Authority Factorization Theorem

### Claim

\[
\boxed{\mathsf{Auth}=\tau\circ V\circ D}
\]

More precisely:

\[
\mathsf{Auth}(p)=\tau_s(R_p,O_p,\varepsilon_s),
\qquad s=\rho(p)
\]

where:

\[
V_s(D(s),\eta_s(p))=(R_p,O_p,\varepsilon_s).
\]

### Objects

Let \(p\) be a proposed transition.

Let:

\[
s=\rho(p)
\]

be the routed sector of \(p\).

Let:

\[
\eta_s(p)
\]

be the finite realization of \(p\) inside the current carrier, observer, operator, and evaluator regime.

Let:

\[
D(s)
\]

be the finite descent packet, when available.

The descent packet contains the finite data needed to evaluate the proposal:

\[
D(s)=P_s
=
(K_s,E_s,V_s,\tau_s,\Lambda_s).
\]

The obstruction-engine implementation may refine this packet as:

\[
\operatorname{Impl}(P_s)
=
(P,E,\mathcal A,\Phi,\Gamma,\Xi,\mathcal{NA},\mathcal{RA},R_{cl},C_{\mathrm{rollback}},\tau_s).
\]

This is implementation detail inside the abstract packet, not a second packet definition.

But \(D\) alone does not authorize anything. It only supplies auditable data.

### Verification Map

Define the verification map:

\[
V_s(D(s),\eta_s(p))
=
(R_p,O_p,\varepsilon_s).
\]

Where:

* \(R_p\) is the verified route data;
* \(O_p\) is the verified obstruction / outcome data;
* \(\varepsilon_s\) is the certified error, exception, or residual boundary.

Possible route states include:

\[
\mathsf{accept},
\quad
\mathsf{reject},
\quad
\mathsf{lift},
\quad
\mathsf{backtrack},
\quad
\mathsf{hold},
\quad
\mathsf{unknown}.
\]

So \(V\) does not grant authority either. It verifies the fiber over \(p\). It answers what the descent packet certifies about \(p\), not whether the system may promote \(p\).

### Terminalization Map

Define:

\[
\tau_s
\]

as the terminalization map for sector \(s\).

It consumes the verified fiber:

\[
(R_p,O_p,\varepsilon_s)
\]

and returns an authority-bearing terminal state:

\[
\tau_s(R_p,O_p,\varepsilon_s)
\in
\mathsf{Terminal}_s.
\]

Examples:

\[
\mathsf{AcceptCertified},
\quad
\mathsf{RejectCertified},
\quad
\mathsf{LicensedLift},
\quad
\mathsf{CertifiedBacktrack},
\quad
\mathsf{Hold},
\quad
\mathsf{BudgetUnknown},
\quad
\mathsf{TypedRefusal}.
\]

This is the first stage where authority exists.

### Theorem

\[
\boxed{
\mathsf{Auth}(p)
=
\tau_s(V_s(D(s),\eta_s(p)))
}
\]

Equivalently, if:

\[
V_s(D(s),\eta_s(p))
=
(R_p,O_p,\varepsilon_s),
\]

then:

\[
\boxed{
\mathsf{Auth}(p)
=
\tau_s(R_p,O_p,\varepsilon_s).
}
\]

> Full proof: see `2_GTFDA_Proof_Archive.md`.

## FDA-4 — Descent Packet Soundness

### Claim

A descent packet:

\[
P_s=(K_s,E_s,V_s,\tau_s,\Lambda_s)
\]

is authority-bearing only if each component is declared and replayable:

\[
\boxed{
\mathsf{AuthPacket}(P_s)
\Rightarrow
\mathsf{DeclaredReplayable}(K_s,E_s,V_s,\tau_s,\Lambda_s).
}
\]

### Component Meanings

Let:

\[
P_s=(K_s,E_s,V_s,\tau_s,\Lambda_s)
\]

where:

| Component | Role |
|---|---|
| \(K_s\) | finite carrier / state space / representation |
| \(E_s\) | evaluator and admissible candidate class |
| \(V_s\) | verification/replay evidence |
| \(\tau_s\) | terminal route semantics |
| \(\Lambda_s\) | lift/refusal/backtrack discipline |

A packet is authority-bearing only if it can say:

```text
what finite system is being evaluated,
which candidates are admissible,
how the result can be replayed,
which terminal route was reached,
and what happens if same-carrier descent fails.
```

### Theorem

\[
\boxed{
\mathsf{AuthPacket}(P_s)
\Rightarrow
K_s\downarrow
\wedge
E_s\downarrow
\wedge
V_s\downarrow
\wedge
\tau_s\downarrow
\wedge
\Lambda_s\downarrow
}
\]

where \(X\downarrow\) means the component is declared, finite or finitely auditable, and replayable in the packet.

> Full proof: see `2_GTFDA_Proof_Archive.md`.

## FDA-5 — Terminal Authority Theorem

### Claim

The authority-bearing object is not the answer alone, but the terminal pair:

\[
\boxed{
(\mathsf{Term},\ \text{derived output if any})
}
\]

An output without its terminal status has no reasoning authority.

### Setup

Let \(p\in\mathcal P\) be a proposal.

By FDA-1 through FDA-4, authority is produced only through the pipeline:

\[
\mathcal P
\xrightarrow{\rho}
\mathcal G
\xrightarrow{D}
\mathcal C_{\mathrm{fin}}
\xrightarrow{V}
\mathsf{Fib}
\xrightarrow{\tau}
\mathsf{Term}.
\]

Let terminalization produce:

\[
\tau_s(V_s(D(s),\eta_s(p)))=\mathsf{Term}_p,
\qquad s=\rho(p).
\]

Let the system optionally derive an output:

\[
y_p.
\]

Then the authority-bearing object is:

\[
\boxed{
A_p=(\mathsf{Term}_p,y_p)
}
\]

not \(y_p\) alone.

### Terminal Classes

The terminal status records what kind of authority the system has.

#### Certified Output Terminals

\[
\mathsf{UniqueRule}
\]

means the output is certified under a unique verifying rule in the declared carrier, operators, evaluator, and replay packet.

\[
\mathsf{UniqueOutput}
\]

means a nonunique rule fiber produced a unique output fiber under the declared equivalence relation and admissible candidate class.

These support answer-level use:

\[
(\mathsf{UniqueRule},y),
\qquad
(\mathsf{UniqueOutput},y).
\]

#### Non-Answer-Authorizing Terminals

The following terminals do not authorize answer-only promotion:

\[
\mathsf{NonUniqueOutput},
\quad
\mathsf{NoRule},
\quad
\mathsf{Budget},
\quad
\mathsf{Refused},
\quad
\mathsf{Lift}.
\]

Their meanings:

| Terminal | Meaning |
|---|---|
| \(\mathsf{NonUniqueOutput}\) | multiple certified outputs or continuations survive |
| \(\mathsf{NoRule}\) | no declared rule licenses the promotion |
| \(\mathsf{Budget}\) | verification did not terminate within declared finite budget |
| \(\mathsf{Refused}\) | the proposal is outside authority or violates evaluator discipline |
| \(\mathsf{Lift}\) | same-carrier authority failed; representation extension is required |

These may still produce a derived object \(y\), but \(y\) is not answer-authorized without the terminal tag.

### Theorem

\[
\boxed{
\mathsf{Auth}(p)
\Rightarrow
\exists \mathsf{Term}_p,\ y_p^{?}
\text{ such that }
\mathsf{AuthObj}(p)=(\mathsf{Term}_p,y_p^{?})
}
\]

and:

\[
\boxed{
y_p\not\Rightarrow \mathsf{Auth}(p)
}
\]

An answer alone is not authority.

> Full proof: see `2_GTFDA_Proof_Archive.md`.

---

# Part II — Relation to Finite Obstruction Calculus

## FDA/GT-1 — Obstruction Engine Inclusion Theorem

### Claim

\[
\boxed{
\mathsf{FiniteObstructionCalculus}
\subset
\mathsf{FiniteDescentAuthority}
}
\]

More precisely: every finite obstruction-calculus engine instance embeds into a finite descent authority packet:

\[
P=(K,E,V,\tau,\Lambda)
\]

where obstruction calculus supplies the internal defect, repair, quotient, witness, and lift machinery, but authority is granted only after terminalization.

### Setup

From the General Theory, theorem-grade obstruction claims begin only after finite data are declared: finite carrier, repair class, context/observer family, boundary maps \(d_0,d_1\) with \(d_1d_0=0\), gauge/norm, certificate regime, and finite operator/lift language or budget.

A finite obstruction-calculus instance contains:

\[
C^0\xrightarrow{d_0}C^1\xrightarrow{d_1}C^2,
\qquad
d_1d_0=0.
\]

Exact repairs are:

\[
B^1=\operatorname{im}(d_0).
\]

Quotient obstruction is:

\[
Q^1=C^1/B^1.
\]

The quotient obstruction norm is:

\[
\Phi([x])=
\inf_{\alpha\in C^0}
|x-d_0\alpha|_{1,\omega}.
\]

Closure mass is:

\[
\Gamma([x])=|\overline d_1([x])|.
\]

The General Theory also defines the closure trichotomy:

\[
\mathsf{UniqueRule},\quad
\mathsf{Survivor},\quad
\mathsf{Open}.
\]

A survivor is closed non-exact quotient residue; an open obstruction requires repair, lift, refusal, or budget boundary.

### Embedding Into FDA Packet

Define a map:

\[
\iota:
\mathsf{FiniteObstructionCalculus}
\to
\mathsf{FiniteDescentAuthority}
\]

by sending an obstruction-calculus engine \(\mathcal M\) to the descent packet:

\[
\iota(\mathcal M)=P_{\mathcal M}=(K,E,V,\tau,\Lambda).
\]

#### 1. Carrier Component

Let:

\[
K_{\mathcal M}
=
(\mathcal T,\mathcal C,\rho,C^\bullet,\omega,p).
\]

This contains the finite term/state category, finite context category, context action, cochain complex, gauge, and profile map.

So:

\[
K \text{ supplies the finite obstruction carrier.}
\]

#### 2. Evaluator Component

Let:

\[
E_{\mathcal M}
=
(\Phi,\Gamma,Q^1,H^1,\mathsf{UniqueRule},\mathsf{Survivor},\mathsf{Open},\mathcal A).
\]

This contains quotient obstruction, closure mass, exact repair, closed residuals, open obstruction, and the admissible repair/operator class.

So:

\[
E \text{ supplies the obstruction evaluator.}
\]

#### 3. Verification Component

Let:

\[
V_{\mathcal M}
\]

be the replay verifier checking:

\[
d_1d_0=0,
\]

\[
x-d_0\alpha,
\]

\[
\Phi([x]),
\]

\[
\Gamma([x]),
\]

dual witness validity:

\[
d_0^*\varphi=0,
\qquad
|\varphi_d|\le\omega_d,
\]

and any claimed exact repair, survivor status, or open obstruction.

So:

\[
V \text{ supplies certificate replay.}
\]

#### 4. Terminalization Component

Let:

\[
\tau_{\mathcal M}
\]

map verified obstruction fibers to terminal statuses:

\[
\mathsf{UniqueRule},
\quad
\mathsf{Survivor},
\quad
\mathsf{Open},
\quad
\mathsf{NoRule},
\quad
\mathsf{Budget},
\quad
\mathsf{Refused},
\quad
\mathsf{Lift}.
\]

In FDA language, this becomes the authority route:

\[
\mathsf{AcceptCertified},
\quad
\mathsf{UniqueOutput},
\quad
\mathsf{NonUniqueOutput},
\quad
\mathsf{LicensedLift},
\quad
\mathsf{TypedRefusal},
\quad
\mathsf{BudgetUnknown}.
\]

So:

\[
\tau \text{ turns verified obstruction data into authority-bearing terminal status.}
\]

#### 5. Lift/Refusal Component

Let:

\[
\Lambda_{\mathcal M}
\]

be the licensed lift contract machinery.

In the General Theory, the lift trigger is context-visible non-congruence:

\[
x\sim y,
\qquad
\rho(c)x\not\sim\rho(c)y.
\]

A licensed lift requires witness, exhaustion, minimality, and lift contract; otherwise the valid result is typed refusal or budget unknown.

So:

\[
\Lambda \text{ supplies lift/refusal discipline.}
\]

### Theorem

\[
\boxed{
\mathsf{FiniteObstructionCalculus}
\subset
\mathsf{FiniteDescentAuthority}
}
\]

> Full proof: see `2_GTFDA_Proof_Archive.md`.

## FDA/GT-2 — Verification as Exactness Theorem

### Claim

\[
\boxed{
V_s(r,x)=1
\Rightarrow
[\omega_{r,x}]=0\in Q^1_s
}
\]

under the packet's declared obstruction encoding.

This connects replay verification to quotient exactness.

### Setup

Let the descent packet for sector \(s\) be:

\[
P_s=(K_s,E_s,V_s,\tau_s,\Lambda_s).
\]

Inside \(K_s\), the obstruction encoding declares a finite cochain complex:

\[
C^0_s \xrightarrow{d_{0,s}} C^1_s \xrightarrow{d_{1,s}} C^2_s,
\qquad
d_{1,s}d_{0,s}=0.
\]

Exact repair lives in:

\[
B^1_s=\operatorname{im}(d_{0,s}).
\]

Quotient obstruction is:

\[
Q^1_s=C^1_s/B^1_s.
\]

Given candidate \(r\) and input \(x\), let:

\[
\omega_{r,x}\in C^1_s
\]

be the residual defect cochain produced by replaying \(r\) on \(x\).

Define the verifier so that:

\[
V_s(r,x)=1
\]

only when replay produces an exact repair certificate:

\[
\exists \alpha\in C^0_s
\quad
\text{such that}
\quad
\omega_{r,x}=d_{0,s}\alpha.
\]

This matches the General Theory's core structure: exact repairs form \(\operatorname{im}(d_0)\), quotient obstruction is \(Q^1=C^1/\operatorname{im}(d_0)\), and exactness corresponds to zero quotient class.

> Full proof: see `2_GTFDA_Proof_Archive.md`.

## FDA/GT-3 — Failure Trichotomy Theorem

### Claim

\[
\boxed{
V_s(r,x)=0
\Rightarrow
[\omega_{r,x}]\ne0
\vee
d_{1,s}\omega_{r,x}\ne0
\vee
\neg\operatorname{adm}_{\Lambda_s}(r,x)
}
\]

Failed verification must be one of:

1. quotient obstruction;
2. closure failure;
3. admissibility failure.

### Setup

Use the same packet:

\[
P_s=(K_s,E_s,V_s,\tau_s,\Lambda_s).
\]

For candidate \(r\) and input \(x\), replay produces a residual:

\[
\omega_{r,x}\in C^1_s.
\]

The packet has three checks.

#### 1. Exactness Check

\[
[\omega_{r,x}]=0\in Q^1_s
\]

equivalently:

\[
\omega_{r,x}\in\operatorname{im}(d_{0,s}).
\]

#### 2. Closure Check

\[
d_{1,s}\omega_{r,x}=0.
\]

#### 3. Admissibility Check

\[
\operatorname{adm}_{\Lambda_s}(r,x).
\]

This means \(r\) is allowed under the packet's candidate class, lift/refusal discipline, side conditions, budget regime, and no-silent-mutation constraints.

The General Theory's closure trichotomy separates exact, survivor, and open obstruction by quotient mass and closure: exact means \(\Phi(q)=0\), survivor means nonzero but closed, and open means nonzero with nonzero closure defect. Open obstruction requires repair, lift, refusal, or budget boundary.

### Verifier Contract

Define \(V_s(r,x)=1\) iff all required packet checks pass:

\[
V_s(r,x)=1
\iff
\left(
[\omega_{r,x}]=0
\wedge
d_{1,s}\omega_{r,x}=0
\wedge
\operatorname{adm}_{\Lambda_s}(r,x)
\right).
\]

Strictly, if exactness holds then closure follows automatically because:

\[
\omega_{r,x}=d_{0,s}\alpha
\Rightarrow
d_{1,s}\omega_{r,x}
=
d_{1,s}d_{0,s}\alpha
=
0.
\]

But closure is still kept as an explicit diagnostic because malformed residuals, parser errors, projected residuals, or non-exact candidate traces may fail closure before exactness is resolved.

### Theorem

\[
\boxed{
V_s(r,x)=0
\Rightarrow
[\omega_{r,x}]\ne0
\vee
d_{1,s}\omega_{r,x}\ne0
\vee
\neg\operatorname{adm}_{\Lambda_s}(r,x)
}
\]

> Full proof: see `2_GTFDA_Proof_Archive.md`.

## FDA/GT-4 — Lift Authority Theorem

### Claim

A lift:

\[
P_s\to P_{s^+}
\]

is authority-preserving only if it satisfies:

\[
\iota_s\ \mathrm{mono}
\]

\[
\pi_s\circ\iota_s=\operatorname{id}
\]

\[
\mu_{s^+}<\mu_s
\]

plus no-silent-mutation.

This links Finite Descent Authority to the licensed lift machinery in the General Theory.

### Setup

Let:

\[
P_s=(K_s,E_s,V_s,\tau_s,\Lambda_s)
\]

be a descent packet.

A lift is a packet morphism:

\[
L_s:P_s\to P_{s^+}.
\]

It extends the finite carrier, evaluator, verifier, terminal semantics, or lift/refusal discipline because same-carrier descent is exhausted or insufficient.

Let:

\[
\iota_s:P_s\hookrightarrow P_{s^+}
\]

be the inclusion of old certified structure into the lifted packet.

Let:

\[
\pi_s:P_{s^+}\to P_s
\]

be the forgetful comparison back to the old packet.

Let:

\[
\mu_s
\]

be the finite descent signature for the packet state.

The General Theory requires lift contracts to include witness, exhaustion, minimality, extension, forgetful comparison, inclusion/projection maps, no-silent-mutation, and replayability. It also instantiates termination by a finite well-founded descent signature \(\mu\), and it requires no-silent-mutation through factorization and skeleton monicity.

### Definition: Authority-Preserving Lift

A lift:

\[
L_s:P_s\to P_{s^+}
\]

is authority-preserving iff every old certified terminal pair remains replayable and non-corrupted in the lifted packet.

Formally, for every old authority object:

\[
(\mathsf{Term}_s,y)
\]

certified by \(P_s\), the lifted packet either:

1. preserves it as the same certified object;
2. refines it into explicitly logged subcases;
3. invalidates it with an explicit terminal tag;
4. or refuses the lift.

It may not silently erase, reinterpret, or mutate old certified data.

### Theorem

\[
\boxed{
\mathsf{AuthorityPreservingLift}(P_s\to P_{s^+})
\Rightarrow
\iota_s\ \mathrm{mono}
\wedge
\pi_s\circ\iota_s=\operatorname{id}
\wedge
\mu_{s^+}<\mu_s
\wedge
\mathsf{NoSilentMutation}
}
\]

> Full proof: see `2_GTFDA_Proof_Archive.md`.

---

# Part III — Publication Boundary

The following material has been intentionally excluded from the publication main and moved to the tertiary workbench:

- LLM-specific corollaries and model-evaluation language;
- Kaggle trace geometry and submission certification material;
- domain-specific transfer and observability schemas;
- quantum packet examples;
- observer-capable FAS and MSS-N selection conjectures;
- backlog forms, internal ledgers, and implementation scaffolding.

This boundary keeps the main FDA paper mathematically legible: the publication claim is finite descent authority, not every application of the doctrine.

# Final Thesis

\[
\boxed{
\text{A proposal is input. A descent packet is machinery. A verifier is evidence. Terminalization is authority.}
}
\]

\[
\boxed{
\text{No finite descent packet, no operational authority.}
}
\]
