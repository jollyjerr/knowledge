# Proofs

A _proof_ Is a verification of a _proposition_ by a chain of _logical deductions_ from a base set of _axioms_.

## Propositions

A Proposition is a statement that is either true or false.

-   Predicate
    
    A Proposition whose truth depends on the value of one or more variables
    
-   Quantifiers
    
    ∀ (“for all”) or ∃ (“there exists”). Always followed by a variable and then a predicate that typically involves that variable. The predicate may involve many quantifiers
    
-   Implication
    
    A proposition of the form `P => Q` read "P implies Q" or "if P. then Q". A proposition of the form P ⇔ Q is read “P if and only if Q”. (Sometimes “if and only if” is abbreviated “iff”.)
    

## Axioms

An axiom is a _proposition_ that is assumed to be true, because you believe it is somehow reasonable.

There is room for disagreement around axioms - so aim for two properties:

-   Consistency
    
    A set of axioms is consistent if no proposition can be proved both true and false.
    
-   Completeness
    
    A set of axioms is complete if every proposition can be proved or disproved.
    

“Must I prove this little fact or can I assume it?”

Unfortunately, there is no absolute answer. Just be upfront about what you’re assuming.

## Logical Deductions

Logical deductions or inference rules are used to combine axioms and true propositions in order to form more true propositions.

Modus Ponens is closely related to:

```bash
(P ^ (P => Q)) => Q
```

Both of these propositions are _tautologies_ because they are true for every setting of P and Q.