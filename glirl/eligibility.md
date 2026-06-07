GLIRL Eligibility (v0.1)

The Permission Calculus of the Civilisation‑Stack



1\. Purpose of Eligibility

Eligibility is the gatekeeper of the Civilisation‑Stack.



Where:



Invariants define what must never be violated



Operators define how reasoning occurs



Witnesses verify what happened



…the Eligibility System determines:



What is allowed to happen next.



Eligibility is the permission calculus that ensures:



actions are valid



transitions are safe



redeclarations are legitimate



figments collapse correctly



TRU issuance is justified



cross‑layer operations remain coherent



It is the front door to every state transition.



2\. The Eligibility Equation

Eligibility is defined as:



Code

ELIGIBLE(expr) := (expr → TRUE)

Where:



expr is a GLIRL expression



→ is Pure‑NOT contraction



TRUE is the canonical fixed‑point



If the expression reduces to TRUE, the action is permitted.

If not, the action is blocked.



Eligibility is binary, deterministic, and reproducible.



3\. Eligibility Inputs

Eligibility evaluates four categories of conditions:



Logical Conditions



Structural Conditions



Continuity Conditions



Cross‑Layer Conditions



These form the eligibility vector.



4\. Eligibility Operators

Eligibility uses a dedicated operator family:



4.1 ELIGIBLE

Code

ELIGIBLE(expr) := (expr → TRUE)

4.2 BLOCKED

Code

BLOCKED(expr) := NOT(ELIGIBLE(expr))

4.3 CONDITIONAL

Code

CONDITIONAL(a, b) := AND(a, b)

Meaning:

b is allowed only if a is true.



4.4 PERMITS

Code

PERMITS(precondition, action) := AND(precondition, action)

4.5 FORBIDS

Code

FORBIDS(precondition, action) := AND(precondition, NOT(action))

Eligibility is a structured decision system, not a boolean hack.



5\. Eligibility in Identity Evolution

Identity evolution requires:



continuity



meaningful transformation



invariant preservation



narrative coherence



Eligibility expression:



Code

ELIGIBLE(

&#x20;   AND(

&#x20;       CONTINUES(identity\_prev → identity\_next),

&#x20;       TRANSFORMS(identity\_prev → identity\_next)

&#x20;   )

)

If TRUE → identity evolves

If FALSE → evolution is blocked



6\. Eligibility in Redeclaration

Redeclaration is allowed only if:



Code

ELIGIBLE(

&#x20;   AND(

&#x20;       CONTINUES(prev → next),

&#x20;       TRANSFORMS(prev → next),

&#x20;       NOT(VIOLATES(next, core\_invariant)),

&#x20;       ARC(prev → next)

&#x20;   )

)

If any part fails → Redeclaration is rejected.



7\. Eligibility in TRU Issuance

TRU issuance requires:



valid contribution



invariant preservation



narrative alignment



witness verification



Eligibility expression:



Code

ELIGIBLE(

&#x20;   AND(

&#x20;       contributed,

&#x20;       invariant\_preserved,

&#x20;       narrative\_aligned

&#x20;   )

)

If TRUE → TRU issued

If FALSE → TRU blocked



8\. Eligibility in Arena Transitions

Arena transitions require:



preconditions



role compatibility



invariant preservation



narrative coherence



Eligibility expression:



Code

ELIGIBLE(

&#x20;   PERMITS(precondition, action)

)

If TRUE → transition allowed

If FALSE → transition blocked



9\. Eligibility in Figment Collapse

A figment collapses into an action only if:



Code

ELIGIBLE(

&#x20;   AND(

&#x20;       POSSIBLE(figment),

&#x20;       COMPATIBLE(figment, identity),

&#x20;       NOT(BREAKS\_ARC(figment, narrative)),

&#x20;       invariant\_preserved

&#x20;   )

)

If TRUE → figment becomes action

If FALSE → figment remains hypothetical



10\. Eligibility in Cross‑Layer Operations

10.1 LIFT Eligibility

Code

ELIGIBLE(

&#x20;   AND(

&#x20;       invariant\_preserved,

&#x20;       ALIGN(lower\_layer, higher\_layer)

&#x20;   )

)

10.2 GROUND Eligibility

Code

ELIGIBLE(

&#x20;   AND(

&#x20;       invariant\_preserved,

&#x20;       NOT(violates\_core)

&#x20;   )

)

Cross‑layer operations are the most strictly gated.



11\. Eligibility Failure Modes

When eligibility fails:



The action is blocked



The failure is recorded by the Witness Network



The identity vector is updated



The figment constellation is adjusted



The narrative arc is re‑evaluated



Eligibility failure is never silent.



12\. Eligibility and the Witness Network

Eligibility is always paired with witnessing:



Code

WITNESS(ELIGIBLE(expr))

Witnesses ensure:



the eligibility expression was correct



invariants were evaluated



no hidden state influenced the result



the outcome is reproducible



Eligibility + Witnessing = civilisation‑grade safety.



13\. Summary

Eligibility is:



the permission calculus



the gatekeeper of transitions



the validator of identity evolution



the arbiter of TRU issuance



the guardian of narrative coherence



the protector of invariants



It ensures that every action in the civilisation is:



valid



safe



coherent



witnessed



invariant‑preserving



Eligibility is how the civilisation says:



“This may happen.”

