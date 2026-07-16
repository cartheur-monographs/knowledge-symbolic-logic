# Knowledge Agent Plan

This plan describes how to turn this repository into a bounded knowledge agent focused on Edmund C. Berkeley, his lineage in symbolic logic, and his relation to early embodied machine intelligence.

## Goal

Build a domain-specific knowledge agent that can answer questions about:

- Berkeley's `Symbolic Logic and Intelligent Machines`
- the lineage `Boole -> Venn -> Shannon -> Berkeley`
- the contrast between Berkeley and mainstream formal-logic presentation such as Basson
- Berkeley's relevance to embodied machine intelligence in the broader sense later seen in David Heiserman's work

The agent should be a research assistant for this corpus, not a general-purpose AI explainer.

## Scope

The first version of the agent should stay inside the source set already present in this repo:

- `Berkeley--Symbolic logic and intelligent machines.pdf`
- `Boole--An Investigation of the Laws of Thought.pdf`
- `Boole--The mathematical analysis of logic.pdf`
- `Venn--SymbolicLogic.pdf`
- `Venn--The logic of chance.pdf`
- `Venn--The Principles of Empirical Or Inductive Logic.pdf`
- `Shannon--A symbolic analysis of relay and switching circuits.pdf`
- `Basson--Intro to symbolic logic.pdf`

Optional external context can be added later, but only when clearly labeled as secondary context.

## Product definition

The agent should be able to do four things well:

1. Answer source-grounded questions about Berkeley.
2. Explain influence and lineage across the corpus.
3. Compare Berkeley with Heiserman-style embodied or adaptive machine intelligence without collapsing them into the same thing.
4. Retrieve passages, concepts, and structured summaries with citations back to the corpus.

The agent should not pretend to be an expert in all of AI, robotics, logic, or cybernetics.

## Recommended repository structure

Add a lightweight structure around the PDFs:

- `src/`
  - original source PDFs
- `notes/`
  - human-written interpretive notes
- `chunks/`
  - extracted and normalized text chunks per source
- `metadata/`
  - source manifests, bibliographic data, concept tags
- `prompts/`
  - system prompts and agent instructions
- `evals/`
  - question sets and expected source-grounded answers

The current markdown analyses can later move into `notes/`, but that is not required immediately.

## Phase 1: Corpus preparation

Prepare the source material so the agent can retrieve from it reliably.

### Tasks

- Extract plain text from each PDF.
- Clean OCR noise where it materially harms retrieval.
- Split each source into stable chunks.
- Store chunk metadata with source name, section, approximate page range, and theme tags.

### Chunking guidance

Use chunks that are:

- large enough to preserve argument flow
- small enough to retrieve precise evidence

A good initial target is:

- `800` to `1500` words per chunk
- `100` to `200` words of overlap

For Berkeley specifically, special indexing should be added around these themes:

- intelligent machines
- inputs, outputs, storage, calculation, control
- Boolean algebra
- states and events
- robot examples
- programming and subroutines

## Phase 2: Concept map and ontology

Build a small domain ontology so the agent can reason consistently about repeated concepts.

### Core entities

- `Berkeley`
- `Boole`
- `Venn`
- `Shannon`
- `Basson`
- `Heiserman`

### Core concepts

- `symbolic logic`
- `Boolean algebra`
- `class logic`
- `statements`
- `relations`
- `intelligent machines`
- `control`
- `memory`
- `inputs`
- `outputs`
- `states`
- `events`
- `robot`
- `behavior`
- `adaptation`
- `embodiment`

### Relationships to encode

- `influenced_by`
- `extends`
- `contrasts_with`
- `applies_to`
- `embodies_in_hardware`
- `anticipates`
- `falls_short_of`

This ontology does not need to be complex. It just needs to make the agent's comparisons stable.

## Phase 3: Retrieval design

The most important capability is source-bounded retrieval.

### Retrieval strategy

Use hybrid retrieval if possible:

- lexical search for exact names and terms
- vector retrieval for semantic similarity

### Retrieval rules

- Prefer Berkeley first when the question is about Berkeley's own claims.
- Prefer Boole, Venn, Shannon, and Basson only when the user asks about influence, comparison, or background.
- Treat Heiserman as comparative context, not as part of the primary corpus, unless that corpus is explicitly extended.

### Ranking priorities

Rank passages higher when they:

- directly answer the question
- contain named authors or named concepts
- define a concept
- contain examples of machines, robots, control, states, or events
- offer explicit historical attribution

## Phase 4: Prompt design

The agent needs a strict system prompt to avoid drifting into generic AI chatter.

### Prompt requirements

- Stay inside the provided corpus unless the user explicitly requests external context.
- Distinguish between direct evidence and inference.
- When comparing Berkeley with later AI or robotics, state clearly that those are cross-period interpretations.
- Prefer citing Berkeley's wording and examples over modern restatements.
- Avoid flattening Berkeley into a generic "symbolic AI" figure.

### Voice

The voice should be:

- scholarly but readable
- explicit about uncertainty
- careful with chronology
- able to compare lineages without overstating influence

## Phase 5: Initial note set

Before building any UI, create a compact internal note library.

### Priority notes

- Berkeley as subject overview
- Boole's role in Berkeley's self-understanding
- Venn's influence on Berkeley
- Shannon as the logic-to-circuit bridge
- Basson as background rather than rival
- Berkeley and embodied machine intelligence
- Berkeley versus Heiserman

Some of this work has already begun in this repo and should be formalized into reusable notes.

## Phase 6: Evaluation

The agent should be tested with questions that stress retrieval discipline and historical accuracy.

### Evaluation categories

- direct factual questions
- influence questions
- comparison questions
- chronology questions
- interpretation questions

### Example evaluation prompts

- `How does Berkeley define an intelligent machine?`
- `Why is Venn a stronger influence on Berkeley than Basson?`
- `What role does Shannon play in Berkeley's machine theory?`
- `Is Berkeley a precursor to embodied AI?`
- `How does Berkeley differ from Heiserman on adaptation and learning?`

### Success criteria

The answer should:

- cite the correct source or sources
- avoid importing unsupported modern claims
- separate evidence from interpretation
- use chronology correctly

## Phase 7: Optional implementation path

A practical first implementation could be:

1. extract text from the PDFs
2. generate chunk files in JSON or Markdown
3. create a metadata manifest
4. build a simple retrieval script or notebook
5. test with a fixed evaluation set
6. refine prompts after observing failure modes

If later desired, the corpus can be placed behind:

- a local RAG prototype
- a notebook workflow
- a small API-backed research assistant

## Risks

The main risks are conceptual rather than technical.

### Risk 1: General-AI drift

The agent may start answering in terms of modern AI jargon instead of Berkeley's framework.

Mitigation:

- source-first retrieval
- prompt constraints
- evals emphasizing period-correct answers

### Risk 2: Overstated influence

The agent may exaggerate the relationships among Berkeley, Venn, Shannon, and Heiserman.

Mitigation:

- explicit `evidence` versus `inference` discipline
- chronology checks
- separate note files for direct citation and comparative interpretation

### Risk 3: OCR contamination

Poor OCR could make retrieval noisy.

Mitigation:

- manual correction of key sections
- high-value concept notes
- chunk-level summaries

## Immediate next steps

The best next sequence for this repo is:

1. create a `notes/` and `metadata/` layout
2. move or copy the current markdown analyses into `notes/`
3. extract Berkeley, Venn, Shannon, and Boole into chunked text
4. build a source manifest with dates and roles
5. write an initial system prompt for the knowledge agent
6. create a small `evals/` set of `20` to `30` questions

## Bottom line

It is absolutely possible to build a knowledge agent on this expertise, but the right product is a disciplined, source-bounded research agent.

Its strength will not come from pretending to know everything. It will come from knowing this corpus unusually well and answering with stable historical and conceptual precision.
