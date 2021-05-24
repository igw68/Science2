# SNCF literature

# Important points in design

- Even a small change in design requires to redo all the proofs (abstraction is
  very helpful here)
- Continues verification during the design (early in V cycle)
- Apparently most of the faults in design in the railway context appear quite
  late in the development process, formal methods can help to find them much
  sooner.

## Efficient verification of railway infrastructure designs against standard regulations

FMSD'18
[Papers/railway-structure-verificaiton.pdf]

The paper talks about static properties of design, and not about verification.
They encode geometric properties of design (signal should be placed at the
entrance of each route), in Datalog.

## Industrial tools in Formal methods Railways

[Works/SNCF/biblio/railway-tools]

- Simulink
- UMC (UML based)
- UPPAAL
- Atelier B
- ProB (model checking)
- Event B (Rodin Platform) (Variables are states and events specify transitions)
  - The Use Event B for modeling, and then dischaege proofs to Atelier B, and MC
    to Pro B
- NuSMV
- SPIN
- CADP (verification of asynchrnous systems concurrent systems, simulation and
  verif on the fly, LOTOS language)
- FDR4 (CSP based tool )
- S3 of Systrel used for verification of interlocking systems

## Interlocking Formal Verification at Alstom Signalling

Systerel people + Alstom
[RSSRAIL'19]

- Classical approach of verification of interlocking systems relies on wide
  testing campaigns on virtual stations.
- It is difficult to deal with improvements and optimizations done over the years
- Most faults in the railway scenario are discovered late in the development of the project, so they
  are very costly.
- They use S3 and bounded model-checking to get "intimate conviction"
- For longer runs the try to find an inductive invariant.
- They speed-up SAT-solving by using lemmas

# Bibliographic Review of Formal Methods for Railway Systems

This document collects personal notes concerning a few selected papers on formal methods for railway systems.

**Disclaimer:** This bibliographic review is not exhaustive, far from it.

## Survey on Formal Methods and Tools in Railways: The ASTRail Approach

By A. Ferrari, M. H. ter Beek, F. Mazzanti, D. Basile, A. Fantechi, S. Gnesi, A. Piattino and D. Trentini.
In RSSRail 2019.
[ [doi](https://doi.org/10.1007/978-3-030-18744-6_15) ]

### Abstract

This paper presents the results of a short questionnaire (5 minutes) filled by 44 participants of the RSSRail 2017 conference.
The questionnaire was oriented to gather information about industrial railway projects,
and about the desired features of formal tools.

The results show that the most used tools are, as expected, those of the B family,
followed by an extensive list of about 40 tools, each one used by few respondents only.
The most desired features concern formal verification, maturity, learnability, quality of documentation,
and ease of integration in a CENELEC process.

### Some key points

The 44 respondents are balanced between academics and industrial practitioners.
A large percentage of respondents has several years of experience in railways and in formal methods.

#### Application domains

Mainly interlocking systems and automatic train distancing systems (ATP/ATC).

#### Phases of the process

Mainly specification and formal verification, but also model analysis and simulation, and to a lesser extent testing and code generation.

#### Tools

Tools belonging the B method family are the most used (by far).
Other tools include

- Industrial practitioners: SCADE, Matlab/Simulink/Stateflow
- Academics: Petri nets/CPN tools, Matlab/Simulink/Stateflow, NuSMV, SPIN.

#### Relevant features of tools

Mainly formal verification and modelling, and to a lesser extent simulation, traceability, test generation and code generation.

#### Relevant quality aspects of tools

Maturity (stable and industry-ready) comes first, followed by ease of learnability and quality of documentation.

Overall, the most relevant quality aspects are associated to the usability of the tool.

## On the Industrial Uptake of Formal Methods in the Railway Domain

By D. Basile, M. H. ter Beek, A. Fantechi, S. Gnesi, F. Mazzanti, A. Piattino, D. Trentini and A. Ferrari.
In IFM 2018.
[ [doi](https://doi.org/10.1007/978-3-319-98938-9_2) ]

## Adopting Formal Methods in an Industrial Setting: The Railways Case

By M. H. ter Beek, A. BorÃ€lv, A. Fantechi, A. Ferrari, S. Gnesi, C. LÃ¶fving and F. Mazzanti.
In FM 2019.
[ [doi](https://doi.org/10.1007/978-3-030-30942-8_46) ]

## Comparing formal tools for system design: a judgment study

By A. Ferrari, F. Mazzanti, D. Basile, M. H. ter Beek and A. Fantechi.
In ICSE 2020.
[ [doi](https://doi.org/10.1145/3377811.3380373) ]

Domnique: SF12
Gweundeline: bos de Fares
Franco: ingenieur
Jean-Batiste: european
Marc: la ou european, modelisation
Pierre Gautier: dir programme BIM, proj European

Aggressive optimizations
controle de commanders et signalisation
