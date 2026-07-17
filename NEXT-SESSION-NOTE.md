# Next Session Note

Date: 2026-07-16

## Current state

The repository now contains:

- a Berkeley lineage analysis in [README.md](/home/cartheur/ame/aiventure/aiventure-github/monographs/knowledge-symbolic-logic/README.md)
- a focused note on Berkeley and embodied machine intelligence in [BERKELEY-EMBODIED-MACHINE-INTELLIGENCE.md](/home/cartheur/ame/aiventure/aiventure-github/monographs/knowledge-symbolic-logic/BERKELEY-EMBODIED-MACHINE-INTELLIGENCE.md)
- a build plan for a Berkeley-centered knowledge agent in [KNOWLEDGE-AGENT-PLAN.md](/home/cartheur/ame/aiventure/aiventure-github/monographs/knowledge-symbolic-logic/KNOWLEDGE-AGENT-PLAN.md)
- a paper draft and paper tooling in [paper/](</home/cartheur/ame/aiventure/aiventure-github/monographs/knowledge-symbolic-logic/paper>)

## Paper files

The paper folder currently includes:

- [paper/berkeley-embodied-machine-intelligence-draft.md](/home/cartheur/ame/aiventure/aiventure-github/monographs/knowledge-symbolic-logic/paper/berkeley-embodied-machine-intelligence-draft.md)
- [paper/annotated-bibliography.md](/home/cartheur/ame/aiventure/aiventure-github/monographs/knowledge-symbolic-logic/paper/annotated-bibliography.md)
- [paper/references.bib](/home/cartheur/ame/aiventure/aiventure-github/monographs/knowledge-symbolic-logic/paper/references.bib)
- [paper/main.tex](/home/cartheur/ame/aiventure/aiventure-github/monographs/knowledge-symbolic-logic/paper/main.tex)
- [paper/main.pdf](/home/cartheur/ame/aiventure/aiventure-github/monographs/knowledge-symbolic-logic/paper/main.pdf)

## What is already done

- The paper compiles successfully with bibliography.
- The current PDF is about Berkeley as a precursor to embodied machine intelligence.
- The literature review now reflects the five-band survey:
  - primary sources
  - immediate symbolic-logic context
  - cybernetics and control
  - behavior-based and embodied comparison
  - light historical interpretation
- Berkeley citations have been tightened around:
  - intelligent machines and machine architecture: `pp. 66--70`
  - algebra of states and events: `pp. 145--147`
  - robots, `Squee`, and the robot-animal material: `pp. 177--181`
- Heiserman comparison is anchored to the Alpha/Beta/Gamma discussion around `pp. 18--20` of `Heiserman-1981.pdf`.

## Working thesis

The current paper argues:

- Berkeley should not be read only as a symbolic logician applying Boolean methods to machinery.
- He should also be read as an early theorist of physically organized, temporally structured, behavior-governing machine intelligence.
- He is not yet adaptive in the Heiserman sense, but he is a bridge figure between algebraic logic and embodied machine behavior.

## Important caution

Do not overclaim that Berkeley ``invented embodied AI.'' The safer and stronger claim is:

- Berkeley is a precursor to embodied machine intelligence in a control-and-behavior sense.
- Heiserman represents a later move into adaptive, experiential, confidence-based creature intelligence.

## Best starting point next session

The user said they have a different, fuller approach in mind and will share it next session.

When the session resumes:

1. Ask for the fuller approach first.
2. Compare it against the current six-page `main.tex` structure before rewriting anything.
3. Decide whether to:
   - reshape the current paper around the new approach, or
   - preserve the current paper as a compact analytic core and build a second, fuller version on top of it.

## Most likely next tasks

- revise `paper/main.tex` around the user's fuller framing
- deepen the historiography section if needed
- add more exact page-level citations from Berkeley and Heiserman
- decide whether to introduce Wiener, Ashby, Walter, Brooks, or Braitenberg into the main body or keep them mostly in the literature review
- optionally commit the paper changes after the new direction is settled

## Practical reminder

If resuming from the TeX build:

- compile with `pdflatex`
- then `bibtex main` if bibliography changes
- then `pdflatex` twice

The last successful compiled output on 2026-07-16 was [paper/main.pdf](/home/cartheur/ame/aiventure/aiventure-github/monographs/knowledge-symbolic-logic/paper/main.pdf).

## Additions

- we want to reference https://arxiv.org/abs/2607.12115 as a use-case in support
- we do not want to relegate Berkeley and Hieserman as a historical curiousity, rather, as a powerful unknown and fully untested appraoch
- we want to imply that behavior-based coding is the foundational path toward a functional robotic "brain"
