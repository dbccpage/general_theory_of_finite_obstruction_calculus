---
title: "The General Theory of Finite Descent Authority"
subtitle: "Proof Archive"
source: "994_General Theory of Finite Descent Authority(3).md"
---

# The General Theory of Finite Descent Authority — Proof Archive

This file preserves the full proof material for the publication main. Backlog-form duplicate summaries have been removed where they were purely internal restatements.

# Part I — Core FDA Proofs

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

### Proof

Assume:

\[
p\in\mathcal P.
\]

This only states that \(p\) is a proposal object.

But \(\mathsf{Auth}(p)\) is not defined by membership in \(\mathcal P\). By the authority pipeline, authority is defined only after successful routing, sector-local realization, descent packaging, verification, and terminalization:

\[
\mathsf{Auth}(p)
=
\tau_s(V_s(D(s),\eta_s(p))),
\qquad s=\rho(p).
\]

Therefore, for \(\mathsf{Auth}(p)\) to hold, the following must all be available:

\[
\rho(p)\downarrow,
\]

\[
\eta_s(p)\downarrow,
\]

\[
D(s)\downarrow,
\]

\[
V_s(D(s),\eta_s(p))\downarrow,
\]

and:

\[
\tau_s(V_s(D(s),\eta_s(p)))\in\mathsf{Term}_{\mathsf{auth}}.
\]

But \(p\in\mathcal P\) alone implies none of these.

A proposal may fail routing:

\[
\rho(p)\uparrow.
\]

It may route but fail sector-local realization:

\[
\eta_s(p)\uparrow.
\]

It may realize but lack a descent packet:

\[
D(s)\uparrow.
\]

It may have a packet but fail verification:

\[
V_s(D(s),\eta_s(p))\in\mathsf{Fib}_{\mathsf{fail}}.
\]

It may verify only into refusal or bounded unknown:

\[
\tau_s(V_s(D(s),\eta_s(p)))
\in
\{
\mathsf{TypedRefusal},
\mathsf{BudgetUnknown},
\mathsf{CarrierFailure}
\}.
\]

Thus proposal membership does not entail authority.

Therefore:

\[
p\in\mathcal P \not\Rightarrow \mathsf{Auth}(p).
\]

\[
\blacksquare
\]

### Stronger Form

\[
\boxed{
\mathsf{Auth}(p)
\Rightarrow
p\in\mathcal P
\wedge
\rho(p)\downarrow
\wedge
\eta_s(p)\downarrow
\wedge
D(s)\downarrow
\wedge
V_s(D(s),\eta_s(p))\downarrow
\wedge
\tau_s(V_s(D(s),\eta_s(p)))\in\mathsf{Term}_{\mathsf{auth}}
}
\qquad s=\rho(p).
\]

But the converse fails:

\[
p\in\mathcal P
\not\Rightarrow
\mathsf{Auth}(p).
\]

A proposal is necessary input, not sufficient authority.

### Terminal Interpretation

A proposal can only become one of the following after terminalization:

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

Before that, it is just:

\[
p\in\mathcal P.
\]

That has no promotion force.

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

### Proof

By definition, operational authority is granted only on the domain where a finite descent packet exists:

\[
\operatorname{dom}(\mathsf{Auth})
=
\{p : s=\rho(p),\ D(s)\downarrow\}.
\]

Therefore, if:

\[
\mathsf{Auth}(p)
\]

holds, then \(p\) must belong to the domain of \(\mathsf{Auth}\). Hence:

\[
\mathsf{Auth}(p)
\Rightarrow
D(s)\downarrow.
\]

Taking the contrapositive gives:

\[
\neg D(s)\downarrow
\Rightarrow
\neg \mathsf{Auth}(p).
\]

So if no finite descent packet is available, the system has no finite operational authority to promote the proposed transition.

\[
\blacksquare
\]

### Typed Refusal Interpretation

The important point is that:

\[
\neg D(s)\downarrow
\]

is not a mathematical failure of the engine. It is a domain failure for authority.

The system does not say:

\[
p \text{ is false}
\]

or:

\[
p \text{ is impossible}.
\]

It says:

\[
p \notin \operatorname{dom}(\mathsf{Auth}).
\]

So the correct terminal route is:

\[
\mathsf{TypedRefusal}
\]

or more specifically one of:

\[
\mathsf{CarrierFailure},
\quad
\mathsf{ObserverFailure},
\quad
\mathsf{CertificateMissing},
\quad
\mathsf{RollbackUnknown},
\quad
\mathsf{BudgetUnknown},
\quad
\mathsf{RealizationFailure}.
\]

Thus:

\[
\boxed{
\neg D
\text{ means no authority, not disproof.}
}
\]

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

### Proof

By FDA-2, operational authority is defined only where a finite descent packet exists:

\[
\mathsf{Auth}(p)
\Rightarrow
D(s)\downarrow.
\]

So assume:

\[
D(s)\downarrow.
\]

The packet \(D(s)\) is only a finite data object. It contains diagnostics, candidate evidence, rollback data, and evaluator state. But raw data is not a terminal route. Therefore:

\[
D(s) \not\Rightarrow \mathsf{Auth}(p).
\]

Next apply verification:

\[
V_s(D(s),\eta_s(p))
=
(R_p,O_p,\varepsilon_s).
\]

This produces a verified fiber over the proposal \(p\). But a verified fiber is still not an operational terminal state. It records what was checked, what obstruction remains, and what route is available. Therefore:

\[
V_s(D(s),\eta_s(p))
\not\Rightarrow
\mathsf{Auth}(p).
\]

Authority appears only after terminalization by the realized evaluator regime:

\[
\tau_s(R_p,O_p,\varepsilon_s).
\]

By definition, \(\tau_s\) maps verified fibers into terminal authority states. Hence:

\[
\mathsf{Auth}(p)
=
\tau_s(R_p,O_p,\varepsilon_s).
\]

Substituting the definition of \(V\):

\[
\mathsf{Auth}(p)
=
\tau_s(V_s(D(s),\eta_s(p))).
\]

Therefore:

\[
\boxed{
\mathsf{Auth}=\tau\circ V\circ D.
}
\]

\[
\blacksquare
\]

### Why \(\rho\), \(\eta\), and \(D\) Alone Do Not Authorize

Routing alone:

\[
\rho(p)
\]

only says that \(p\) has been assigned to a sector.

Realization alone:

\[
\eta_s(p)
\]

only says that \(p\) has been encoded into the sector-local finite system.

It does not say:

\[
p \text{ descends}.
\]

Descent packet alone:

\[
D(s)
\]

only says that the routed sector has auditable evaluator data.

It does not say:

\[
p \text{ is accepted}.
\]

Verification alone:

\[
V_s(D(s),\eta_s(p))
\]

only says that the proposal has a verified route/residual/error fiber.

It does not become operational authority until terminalized:

\[
\tau_s(R_p,O_p,\varepsilon_s).
\]

Thus:

\[
\boxed{
\rho \text{ routes, } \eta \text{ realizes, } D \text{ packages, } V \text{ verifies, } \tau \text{ authorizes.}
}
\]

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

### Proof

Assume:

\[
\mathsf{AuthPacket}(P_s)
\]

meaning \(P_s\) can authorize an operational route for state \(s\). Then \(P_s\) must support a terminal judgment of the form:

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
\mathsf{unknown},
\quad
\mathsf{refusal}.
\]

For such a terminal judgment to carry authority, the judgment must be finite, checkable, replayable, and scoped. Each packet component supplies one necessary part of that authority.

#### 1. Carrier Necessity

If \(K_s\) is missing, then there is no declared finite carrier:

\[
K_s\uparrow
\Rightarrow
\text{no carrier}.
\]

Without a carrier, the system cannot determine the state space, boundaries, cochains, observers, admissible supports, or representation in which the proposed transition is evaluated.

So no descent, obstruction, lift, or refusal can be scoped.

Therefore:

\[
K_s\uparrow\Rightarrow \neg\mathsf{AuthPacket}(P_s).
\]

#### 2. Evaluator / Candidate-Class Necessity

If \(E_s\) is missing, then there is no declared evaluator or admissible candidate class:

\[
E_s\uparrow
\Rightarrow
\text{no admissible candidate class}.
\]

Without \(E_s\), the system cannot determine:

\[
\mathcal A_s,
\quad
\Phi,
\quad
\Gamma,
\quad
\Xi,
\quad
\mathcal{NA},
\quad
\mathcal{RA},
\quad
R_{cl},
\]

or the descent relation governing promotion.

So a transition cannot be classified as descending, obstructive, inadmissible, or unknown.

Therefore:

\[
E_s\uparrow\Rightarrow \neg\mathsf{AuthPacket}(P_s).
\]

#### 3. Verification / Replay Necessity

If \(V_s\) is missing, then there is no replayable verification:

\[
V_s\uparrow
\Rightarrow
\text{no replay}.
\]

Without replay evidence, the packet cannot reconstruct why the route was accepted, rejected, lifted, held, or refused.

That collapses the distinction between:

\[
\text{certified judgment}
\]

and:

\[
\text{unverified assertion}.
\]

Authority requires replayability. Therefore:

\[
V_s\uparrow\Rightarrow \neg\mathsf{AuthPacket}(P_s).
\]

#### 4. Terminal-Semantics Necessity

If \(\tau_s\) is missing, then there are no terminal semantics:

\[
\tau_s\uparrow
\Rightarrow
\text{no terminal semantics}.
\]

Without \(\tau_s\), verification may produce data, but there is no declared route interpreting that data as:

\[
\mathsf{AcceptCertified},
\quad
\mathsf{RejectCertified},
\quad
\mathsf{LicensedLift},
\quad
\mathsf{BudgetUnknown},
\quad
\mathsf{TypedRefusal}.
\]

Thus the packet cannot distinguish acceptance from refusal, unknown, backtrack, or lift boundary.

Therefore:

\[
\tau_s\uparrow\Rightarrow \neg\mathsf{AuthPacket}(P_s).
\]

#### 5. Lift/Refusal Discipline Necessity

If \(\Lambda_s\) is missing, then there is no discipline for same-carrier failure:

\[
\Lambda_s\uparrow
\Rightarrow
\text{no lift/refusal discipline}.
\]

Without \(\Lambda_s\), the system cannot determine what happens when:

\[
\nexists o\in\mathcal A_s:
\mathsf{CertifiedDescent}(s,o).
\]

So a failed descent could be silently converted into an unlicensed lift, speculative extension, hidden assumption edge, or false acceptance.

The packet needs \(\Lambda_s\) to route same-carrier failure into:

\[
\mathsf{LicensedLift},
\quad
\mathsf{TypedRefusal},
\quad
\mathsf{BudgetUnknown},
\quad
\mathsf{CertifiedBacktrack}.
\]

Therefore:

\[
\Lambda_s\uparrow\Rightarrow \neg\mathsf{AuthPacket}(P_s).
\]

Since removing any component destroys one necessary condition for authority, all five are required:

\[
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
\Lambda_s\downarrow.
\]

Equivalently:

\[
\neg K_s
\vee
\neg E_s
\vee
\neg V_s
\vee
\neg\tau_s
\vee
\neg\Lambda_s
\Rightarrow
\neg\mathsf{AuthPacket}(P_s).
\]

\[
\blacksquare
\]

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

### Proof

Assume:

\[
\mathsf{Auth}(p).
\]

By FDA-3, authority factors through terminalization:

\[
\mathsf{Auth}(p)
=
\tau_s(V_s(D(s),\eta_s(p))).
\]

Therefore authority is produced as a terminal route:

\[
\mathsf{Term}_p
=
\tau_s(R_p,O_p,\varepsilon_s).
\]

If the terminal route derives an output, call it:

\[
y_p.
\]

Then the complete authority object is:

\[
(\mathsf{Term}_p,y_p).
\]

Now suppose one keeps only \(y_p\) and discards \(\mathsf{Term}_p\). Then the evaluator cannot distinguish:

\[
(\mathsf{UniqueRule},y_p)
\]

from:

\[
(\mathsf{NonUniqueOutput},y_p),
\quad
(\mathsf{NoRule},y_p),
\quad
(\mathsf{Budget},y_p),
\quad
(\mathsf{Refused},y_p),
\quad
(\mathsf{Lift},y_p).
\]

But these terminal states have different operational meanings. In particular:

\[
\mathsf{UniqueRule}
\]

authorizes certified use, while:

\[
\mathsf{Budget},
\mathsf{Refused},
\mathsf{Lift}
\]

do not authorize answer promotion.

Therefore \(y_p\) alone cannot carry authority, because identical or similar outputs may arise under different terminal statuses.

Thus the authority-bearing object is not:

\[
y_p
\]

but:

\[
\boxed{
(\mathsf{Term}_p,y_p^{?})
}
\]

where \(y_p^{?}\) may be absent when the terminal is refusal, unknown, or lift-required.

\[
\blacksquare
\]

### Consequence: Answer-Only Scoring Is Insufficient

Answer-only scoring evaluates:

\[
y_p
\]

but ignores:

\[
\mathsf{Term}_p.
\]

So it can falsely identify:

\[
(\mathsf{Budget},y)
\]

or:

\[
(\mathsf{NoRule},y)
\]

as equivalent to:

\[
(\mathsf{UniqueRule},y).
\]

That is the failure mode:

\[
\boxed{
\text{correct-looking answer}
\neq
\text{authorized reasoning}
}
\]

A model may output the right string while lacking:

* finite carrier realization;
* admissible operator class;
* descent packet;
* replay certificate;
* uniqueness proof;
* terminal semantics;
* lift/refusal discipline.

So the answer can be externally correct but internally unauthorized.

# Part II — FDA / Finite Obstruction Calculus Proofs

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

### Proof

Let:

\[
\mathcal M\in\mathsf{FiniteObstructionCalculus}.
\]

By the canonical finite boundary of the General Theory, \(\mathcal M\) must declare finite carrier data, repair class, context/observer family, boundary maps, gauge, certificate regime, and finite operator/lift language or budget.

Construct:

\[
P_{\mathcal M}=(K_{\mathcal M},E_{\mathcal M},V_{\mathcal M},\tau_{\mathcal M},\Lambda_{\mathcal M}).
\]

By construction:

* \(K_{\mathcal M}\) contains the finite carrier and cochain complex;
* \(E_{\mathcal M}\) contains \(\Phi,\Gamma,Q^1,H^1\), admissible repairs, and obstruction classifications;
* \(V_{\mathcal M}\) replays primal-dual certificates, repair witnesses, closure checks, and obstruction status;
* \(\tau_{\mathcal M}\) terminalizes verified obstruction data into authority-bearing statuses;
* \(\Lambda_{\mathcal M}\) handles context witnesses, licensed lifts, typed refusal, and budget boundaries.

Thus \(P_{\mathcal M}\) is a finite descent authority packet.

Therefore every finite obstruction-calculus instance has an image in finite descent authority:

\[
\iota(\mathcal M)=P_{\mathcal M}.
\]

So:

\[
\mathsf{FiniteObstructionCalculus}
\subset
\mathsf{FiniteDescentAuthority}.
\]

\[
\blacksquare
\]

### Important Boundary

The inclusion does not mean obstruction calculus alone authorizes outputs.

Obstruction calculus supplies:

\[
\text{defects, repairs, quotient obstruction, closure, witnesses, lifts.}
\]

Finite Descent Authority supplies the authority pipeline:

\[
\text{carrier} \to
\text{descent packet} \to
\text{verification} \to
\text{terminalization}.
\]

So the correct relation is:

\[
\boxed{
\text{Obstruction calculus is the engine inside the packet, not the terminal authority itself.}
}
\]

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

### Proof

Assume:

\[
V_s(r,x)=1.
\]

By the declared verifier contract, this means there exists a replayable exact repair witness:

\[
\alpha\in C^0_s
\]

such that:

\[
\omega_{r,x}=d_{0,s}\alpha.
\]

Therefore:

\[
\omega_{r,x}\in \operatorname{im}(d_{0,s})=B^1_s.
\]

Passing to the quotient:

\[
Q^1_s=C^1_s/\operatorname{im}(d_{0,s}),
\]

any element of \(\operatorname{im}(d_{0,s})\) represents the zero quotient class. Hence:

\[
[\omega_{r,x}]=0\in Q^1_s.
\]

Therefore:

\[
V_s(r,x)=1
\Rightarrow
[\omega_{r,x}]=0\in Q^1_s.
\]

\[
\blacksquare
\]

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

### Proof

By verifier contract:

\[
V_s(r,x)=1
\iff
A\wedge B\wedge C
\]

where:

\[
A := [\omega_{r,x}]=0\in Q^1_s,
\]

\[
B := d_{1,s}\omega_{r,x}=0,
\]

\[
C := \operatorname{adm}_{\Lambda_s}(r,x).
\]

Therefore:

\[
V_s(r,x)=0
\Rightarrow
\neg(A\wedge B\wedge C).
\]

By De Morgan's law:

\[
\neg(A\wedge B\wedge C)
\iff
\neg A\vee \neg B\vee \neg C.
\]

Substituting the definitions:

\[
\neg A
\iff
[\omega_{r,x}]\ne0\in Q^1_s,
\]

\[
\neg B
\iff
d_{1,s}\omega_{r,x}\ne0,
\]

\[
\neg C
\iff
\neg\operatorname{adm}_{\Lambda_s}(r,x).
\]

Thus:

\[
V_s(r,x)=0
\Rightarrow
[\omega_{r,x}]\ne0
\vee
d_{1,s}\omega_{r,x}\ne0
\vee
\neg\operatorname{adm}_{\Lambda_s}(r,x).
\]

\[
\blacksquare
\]

### Terminal Interpretation

The trichotomy maps directly to terminal routes:

| Failure | Obstruction meaning | Terminal route |
|---|---|---|
| \([\omega]\ne0\) | irreducible quotient obstruction | `OpenObstruction` / `Survivor` / `Lift` |
| \(d_1\omega\ne0\) | closure failure | `ClosureFailure` / `Refused` / `Lift` |
| \(\neg\operatorname{adm}_{\Lambda}\) | inadmissible candidate or missing license | `NoRule` / `Refused` / `Budget` |

This prevents vague failure labels.

No:

```text
solver failed
```

Only:

```text
quotient obstruction
closure failure
admissibility failure
```

or a separately terminalized infrastructure status such as:

```text
BudgetUnknown
ParserFailure
CarrierFailure
```

Those should be handled by \(\tau_s\), not collapsed into \(V_s=0\).

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

### Proof

Assume:

\[
\mathsf{AuthorityPreservingLift}(P_s\to P_{s^+}).
\]

We prove each required condition.

#### 1. Monicity of \(\iota_s\)

Suppose \(\iota_s\) is not monic.

Then there exist distinct old certified objects:

\[
a\neq b\in P_s
\]

such that:

\[
\iota_s(a)=\iota_s(b).
\]

These may be distinct carrier states, quotient classes, witnesses, certificates, terminal tags, or rollback traces.

If they collapse in the lifted packet, then the lifted packet cannot replay which old certified object was used. Therefore the lift has silently identified old authority-bearing data.

That violates authority preservation.

So:

\[
\mathsf{AuthorityPreservingLift}
\Rightarrow
\iota_s\ \mathrm{mono}.
\]

This is the skeleton-monicity idea: certified old structure must embed into the lifted system unless explicitly invalidated. The General Theory states that if a morphism claims to preserve certified data, its restriction to the invariant skeleton must be monic, and any non-preserved class must carry an explicit invalidation label.

#### 2. Retraction Condition \(\pi_s\circ\iota_s=\operatorname{id}\)

The lift must include a forgetful comparison:

\[
\pi_s:P_{s^+}\to P_s.
\]

Authority preservation requires that if old certified structure is included into the lifted packet and then forgotten back, it returns unchanged:

\[
\pi_s(\iota_s(a))=a
\]

for every old certified object \(a\in P_s\).

Otherwise, old data would be distorted by the lift/forget cycle:

\[
a\mapsto\iota_s(a)\mapsto\pi_s(\iota_s(a))\neq a.
\]

That would mean the lift changed old authority without a terminal invalidation. Again, silent mutation.

Therefore:

\[
\mathsf{AuthorityPreservingLift}
\Rightarrow
\pi_s\circ\iota_s=\operatorname{id}_{P_s}.
\]

This makes \(P_s\) a retract of its lifted comparison structure. The old packet is not merely embedded; it remains recoverable.

#### 3. Descent Condition \(\mu_{s^+}<\mu_s\)

A lift is not valid merely because it adds representation.

Without a strict decrease in a declared well-founded signature:

\[
\mu_{s^+}<\mu_s,
\]

the system could keep expanding representation forever while claiming progress.

That is not finite descent authority. It is unbounded structural growth.

The General Theory's termination hypothesis requires a finite well-founded signature \(\mu\) that strictly decreases at accepted steps; its lift contract machinery is also finite and replayable.

So an authority-preserving lift must reduce the declared lift/descent obligation:

\[
\mu_{s^+}<\mu_s.
\]

Important nuance: \(\mu\) need not mean raw carrier size. A lift may increase representation size while decreasing the declared obstruction obligation, witness rank, unresolved context defect, lift debt, or certified exhaustion measure. The theorem requires descent in the declared finite authority signature, not necessarily fewer nodes or smaller syntax.

Thus:

\[
\mathsf{AuthorityPreservingLift}
\Rightarrow
\mu_{s^+}<\mu_s.
\]

#### 4. No-Silent-Mutation

Finally, suppose no-silent-mutation fails.

Then some old certified object is:

* erased without logged invalidation;
* identified with another old object without explicit quotienting;
* reinterpreted under a new carrier without replay trail;
* made unreachable by the new verifier;
* or changed under terminal semantics without a terminal tag.

Then the lifted packet cannot preserve authority, because an auditor cannot determine whether the old certificate remains valid, was refined, was invalidated, or was refused.

Therefore:

\[
\mathsf{AuthorityPreservingLift}
\Rightarrow
\mathsf{NoSilentMutation}.
\]

The General Theory gives this condition explicitly: lift morphisms require logged factorization of identifications/erasures and skeleton monicity for preserved certified data.

### Conclusion

Combining the four necessary conditions:

\[
\mathsf{AuthorityPreservingLift}(P_s\to P_{s^+})
\Rightarrow
\iota_s\ \mathrm{mono}
\wedge
\pi_s\circ\iota_s=\operatorname{id}
\wedge
\mu_{s^+}<\mu_s
\wedge
\mathsf{NoSilentMutation}.
\]

\[
\blacksquare
\]

### Failure Table

| Missing condition | Failure mode |
|---|---|
| \(\iota_s\) not mono | old certified distinctions collapse |
| \(\pi_s\circ\iota_s\neq\operatorname{id}\) | old packet cannot be recovered after lift |
| \(\mu_{s^+}\not<\mu_s\) | lift is expansion without descent |
| No-silent-mutation fails | old authority is silently erased, rewritten, or reinterpreted |
