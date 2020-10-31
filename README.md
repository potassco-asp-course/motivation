# Motivation

This repository regroups slides motivating Answer Set Programming (ASP).
The original idea was to provide a first complete overview of all relevant topics
that are detailed in separate sections or repositories, respectively.

## Closed world assumption

- **Stable model semantics** can be seen as a logic for reasoning under the **Closed world assumption** (CWA)

- In interpretations following the spirit of "classical" logic, an unknown proposition can be true or false

- Unlike this, the simplest CWA-based approach, namely database systems, treat unknown information as false

  Just like at a bus stop, where a non-listed, and thus unknown timing, is interpreted as "false", in the sense that no
  bus is supposed to arrive

  Hence the CWA acts as a convention stating that only explicitly listed timings represent bus arrivals and all timings
  left open are supposed to be interpreted as non-arrivals

- Note how space effective this is because all negative information is left out

  And think of the many misunderstandings we all had because missing information was interpreted differently

  So this is a pretty "human" way, also referred to as *commonsense reasoning*

- *Stable model semantics* extends this idea to logic programs (as well as arbitrary formulas)

  To this end, it extends the requirement of "being given explicitly" in databases to "being provable" or better "being
  provably true"

  Hence it is not sufficient to claim that something is true, it must be provably so, that is, there has to be a
  justification, a certificate, or in logical terms a proof

  In the case of logic programs, this can be the existence of a fact in the program (just as with databases)
  or the existence of a rule that derives a proposition and whose prerequisites are also provable

  While this is hopefully clear for positive propositions, the question arises how to interpret negative ones..?

- As in databases, the application of the CWA to programs (or formulas) relies on the non-existence (or absence) of
  information

  A proposition is regarded to be false, if it cannot be proven (or justified or certified etc)

- Note that this reduces the number of possible interpretations satisfying a program (or a formula) considerably

  Now, true propositions must be justified

  Hence, unknown propositions cannot become true anymore (as in the above "classical" interpretation)
  because now they lack such a justification

  As a consequence, interpretations selected by the CWA mechanism in *stable model semantics* have usually much fewer true
  propositions and many more false propositions - just the very same phenomena as in databases

- Another thing that CWA brings about is that conclusions become tentative

  So if there is no evidence for a proposition, it is set to false

  In case you learn that it is true later on, and add it to your program, it changes it truth value from false to true

  Just as many things in live that draw upon assumption

  Examples include:
  - birds fly and penguins
  - your way home and a flat tire
  - your position in a soccer game and a missing teammate
  - etc

- Again, this is different from the "classical" approach, where conclusions never change their truth value
  upon the arrival of new information,

  simply because you cannot reason under assumptions in the first place

- Well, that's enough hand-waving for now :)
