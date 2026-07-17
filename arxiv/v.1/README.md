# arXiv v.1 Submission Bundle

This directory contains the `v.1` arXiv submission materials for the
`symbolic-logic` paper.

Working title:

- `Berkeley and Heiserman as an Unexhausted Architecture for Embodied Machine Intelligence`

## Primary files

- `main.tex`: LaTeX source for the paper
- `references.bib`: bibliography database
- `main.pdf`: locally compiled reference PDF
- `annotated-bibliography.md`: supporting source notes
- `berkeley-embodied-machine-intelligence-draft.md`: prose draft companion

## Local build

```bash
cd arxiv/v.1
pdflatex -interaction=nonstopmode -halt-on-error main.tex
bibtex main
pdflatex -interaction=nonstopmode -halt-on-error main.tex
pdflatex -interaction=nonstopmode -halt-on-error main.tex
```

## Submission package

For arXiv submission, upload source rather than PDF-only.

Current source bundle:

- `main.tex`
- `references.bib`
- `main.bbl`

If arXiv compiles cleanly from `main.tex` and `references.bib`, the local
`main.pdf` should be treated as a comparison artifact, not the upload format.

There is also a prepared archive at:

- `../berkeley-heiserman-arxiv.tar.gz`

Use that archive only if its contents still match the current paper files.

## Recommended arXiv metadata

Primary category:

- `cs.AI`

Reason:

- The paper argues for a still-live architecture of machine intelligence
  centered on logic, control, state organization, and embodied behavior.
  That fits arXiv's broad AI category well.

Secondary category:

- `cs.RO`

Reason:

- The manuscript is substantially about robots, embodied control, and
  behavior-organizing machine architectures, even though it is not framed as
  a narrow experimental robotics paper.

Optional alternative secondary:

- `cs.CY` if a later revision shifts more explicitly toward the societal
  implications of AI rather than the architecture of intelligent systems.

Recommended license:

- `arXiv.org perpetual, non-exclusive license 1.0`

Why:

- This is the safest default if later journal submission is likely, because
  it keeps the preprint available on arXiv while minimizing reuse
  complications.

Alternative:

- `CC BY 4.0` if broad reuse is desired and the eventual journal clearly
  permits preprints under that license.

Comments field draft:

- `16 pages. Preprint version under review for journal submission.`

Keywords for internal tracking:

- `embodied AI, machine intelligence, symbolic logic, robotics, cybernetics, Berkeley, Heiserman`

## arXiv submission requirements

- Upload source rather than PDF-only submission for this LaTeX manuscript.
- arXiv prefers `(La)TeX, AMS(La)TeX, PDFLaTeX`.
- arXiv does not accept a PDF generated from TeX as the submitted source
  format.
- If the submitter is new to arXiv or new to the chosen category,
  endorsement may be required.
- The selected license is irrevocable for that version.

## Submission checklist

1. Confirm the final title, author list, affiliations, and ORCIDs.
2. Confirm the abstract in `main.tex` is the one to submit.
3. Confirm the chosen primary category is `cs.AI`.
4. Confirm whether endorsement is needed for the submitting author.
5. Upload LaTeX source, bibliography, and generated bibliography output rather than PDF-only.
6. Preview arXiv's compiled PDF and compare it against local `main.pdf`.
7. Verify references, title metadata, and abstract metadata before final submission.
8. Re-check journal preprint compatibility on the day of submission if a journal target is already preferred.

## Journal shortlist

### Best current fit

`Minds and Machines`

- Publisher: Springer Nature
- Why it fits: strongest match for the paper in its current form, given the
  mix of symbolic logic, machine architecture, embodied intelligence, and
  conceptual comparison between Berkeley and Heiserman.
- What would help before submission: keep the argumentative core strong, make
  the contribution to current AI theory explicit, and tighten the novelty
  claim around architecture and embodiment.
- Preprint policy: Springer Nature states that posting preprints does not
  count as prior publication and does not jeopardize consideration.
- Current recommendation: top journal choice if the paper stays near its
  current balance.

### Strong embodied-behavior option

`Adaptive Behavior`

- Publisher: SAGE
- Why it fits: best option if the manuscript is revised further toward
  embodied, adaptive, robotic, and behavioral intelligence.
- What would help before submission: strengthen the adaptive-behavior
  framing, expand the Heiserman comparison, and add a more explicit section
  on present-day embodied-agent design.
- Preprint policy: the journal states that it accepts manuscripts posted as
  preprints.
- Current recommendation: strongest choice if the next revision becomes more
  explicitly embodied and behavior-theoretic.

### Robotics engineering option

`Robotics and Autonomous Systems`

- Publisher: Elsevier
- Why it fits: strongest engineering-side option, especially if the paper is
  reframed more directly as a robotics architecture contribution.
- What would help before submission: add a clearer bridge from Berkeley and
  Heiserman to current robot-control design and consider a more concrete
  research-agenda or prototype-architecture section.
- Preprint policy: the guide for authors states that preprint sharing does
  not count as prior publication.
- Current recommendation: good option only if the manuscript is pushed
  further toward engineering and robotics architecture.

### Wider AI discourse option

`AI & Society`

- Publisher: Springer Nature
- Why it fits: good destination if the paper is framed as an intervention in
  how AI should be conceived and designed, beyond statistical optimization.
- What would help before submission: make the relevance to present and future
  AI design more explicit and expand the discussion of which current AI
  assumptions the paper challenges.
- Preprint policy: covered by Springer Nature's preprint-friendly policy.
- Current recommendation: strong alternative if broader AI discourse reach is
  more important than a narrower architecture or behavior venue.

## Recommended path

- If the paper stays close to its current balance: submit to `Minds and
  Machines` after arXiv.
- If it deepens toward embodied behavior and adaptive architecture: submit to
  `Adaptive Behavior` after arXiv.
- If it is rewritten more aggressively toward robotics engineering: consider
  `Robotics and Autonomous Systems`.
- If the goal is a broader intervention in AI futures and design culture:
  consider `AI & Society`.

## Reference links

- arXiv submission guidelines: `https://info.arxiv.org/help/submit/index.html`
- arXiv license guidance: `https://info.arxiv.org/help/license/index.html`
- arXiv category taxonomy: `https://arxiv.org/category_taxonomy`
- arXiv endorsement guidance:
  `https://arxiv-org.atlassian.net/wiki/spaces/AUS/pages/6455344/How%2Bdo%2BI%2Bget%2Bendorsed?atl_f=content-tree`
- Minds and Machines: `https://link.springer.com/journal/11023`
- Springer Nature preprint policy:
  `https://www.springer.com/de/editorial-policies/preprint-sharing`
- Adaptive Behavior:
  `https://uk.sagepub.com/en-gb/eur/journal/adaptive-behavior`
- Adaptive Behavior author instructions:
  `https://journals.sagepub.com/author-instructions/adb`
- Robotics and Autonomous Systems:
  `https://www.sciencedirect.com/journal/robotics-and-autonomous-systems`
- Robotics and Autonomous Systems guide for authors:
  `https://www.sciencedirect.com/journal/robotics-and-autonomous-systems/publish/guide-for-authors`
- AI & Society: `https://link.springer.com/journal/146`

## Notes on local artifacts

The files `main.aux`, `main.blg`, `main.log`, and `main.out` are local build
artifacts. They are useful for compilation and troubleshooting, but they are
not part of the paper's intellectual content.
