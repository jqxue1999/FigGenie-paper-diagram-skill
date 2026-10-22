# Reusable parts library (`assets/symbols/`)

3851 parts: icon 605, motif 2017, shape 280, device 949.
Each file is a standalone SVG in **print pt** (viewBox `0 0 W H`), wrapped in `<g data-symbol="name">`;
copy the inner `<g>` into a figure (`<g data-symbol="name" transform="translate(x,y)">…`) and recolour fills/strokes
by palette role. Colours are as drawn in the source paper. Parts with `provenance: corpus` were cut from
published figures (see `source` in index.json) and are style references only; `original` parts were drawn for this skill.

**The library is a reference, not a limit.** Draw any component the figure needs; match the stroke width,
corner radius and colour roles of the rest of the figure (references/style-rules.md, references/parts-styles.md).

**Mechanism parts** (2261, `subtype: "mechanism"` in index.json) were cut from mechanism figures (walkthroughs,
before/after sequences, state machines, comparisons, component anatomy). They carry a `family` (the drawing idiom,
155 consolidated families listed under `families` in index.json), a `theme`, a `variant` note and
`figure_kinds` (which figure groups the idiom serves). The `device` kind holds the narrative devices of such figures:
ghost copies, frame arrows, delta highlights, check/cross marks, pointers into slots, step badges, lane dividers …
Browse them by theme: `catalog-mech-structures.png`, `catalog-mech-annotations.png`, `catalog-mech-icons.png`, `catalog-mech-logic-time.png`, `catalog-mech-data-flow.png`, `catalog-mech-frames-change.png`, `catalog-mech-graphs.png`, `catalog-mech-steps-traces.png`, `catalog-mech-containers.png`, `catalog-mech-math-code.png`, `catalog-mech-other.png`; search index.json by family / tags / depicts.

**AI-venue parts** (998, `subtype: "ai"` in index.json) were cut from the Figure 1s of ICLR, ICML, NeurIPS, CVPR, ACL
and AAAI papers (references/ai/): the stock idioms of that family (an LLM, a Transformer block, a LoRA adapter, a token
strip, a diffusion chain, an agent loop, chat bubbles, benchmark cards, film strips of samples ...) and its devices (verdict
marks, zoom call-outs, tab titles, block arrows). Each carries a `family` (183 families: the ids of the AI tag vocabulary,
plus `new:<slug>` families the cutting agents opened, listed under `families` with `subtype: "ai"`), a `theme`, a `domain`
(the sub-field of the figure it came from: llm-nlp, multimodal, vision, agents, ml-core, audio, rl-robotics, generative, science-engineering, other), a `convention` (common / variant / own) and
`placeholders` (bitmaps of the source replaced by grey slots: a photo, an icon, a logo the paper supplied). Browse them by
theme: `catalog-ai-things-data.png`, `catalog-ai-things-models.png`, `catalog-ai-devices-arrows-colour.png`, `catalog-ai-things-agents.png`, `catalog-ai-things-charts-structures.png`, `catalog-ai-new-families.png`, `catalog-ai-devices-marks.png`, `catalog-ai-devices-titles-notes.png`, `catalog-ai-devices-layout.png`; search index.json by family / domain / tags / depicts.

Browse: `catalog-icon.png`, `catalog-motif.png`, `catalog-shape.png` (architecture parts); search: `index.json` (name, category, tags, depicts).

| kind | category | count |
|---|---|---|
| device | agents | 9 |
| device | annotation | 8 |
| device | annotations | 3 |
| device | arrows | 26 |
| device | charts | 30 |
| device | circuit | 2 |
| device | claims | 1 |
| device | compute | 75 |
| device | concurrency | 2 |
| device | containers | 1 |
| device | control | 324 |
| device | data | 127 |
| device | dialogue | 1 |
| device | embeddings | 1 |
| device | evaluation | 3 |
| device | flow | 1 |
| device | frames | 1 |
| device | hardware | 27 |
| device | layout | 17 |
| device | legend | 10 |
| device | legends | 1 |
| device | loss | 1 |
| device | markers | 1 |
| device | math | 1 |
| device | memory | 41 |
| device | ml | 1 |
| device | models | 4 |
| device | network | 93 |
| device | notation | 1 |
| device | operations | 2 |
| device | people | 2 |
| device | probes | 1 |
| device | software | 1 |
| device | status | 83 |
| device | status-misc | 2 |
| device | tasks | 1 |
| device | time | 34 |
| device | titles | 1 |
| device | training | 7 |
| device | zoom | 2 |
| icon | agents | 1 |
| icon | circuit | 1 |
| icon | cloud-infra | 20 |
| icon | compute | 87 |
| icon | control | 13 |
| icon | data | 112 |
| icon | environments | 3 |
| icon | graphics | 1 |
| icon | graphs | 1 |
| icon | hardware | 65 |
| icon | markers | 1 |
| icon | memory | 10 |
| icon | memory-storage | 27 |
| icon | ml | 19 |
| icon | models | 11 |
| icon | network | 51 |
| icon | people | 38 |
| icon | robotics | 1 |
| icon | security | 20 |
| icon | software | 19 |
| icon | status | 41 |
| icon | status-misc | 58 |
| icon | time | 5 |
| motif | 3d-vision | 1 |
| motif | aesthetics | 1 |
| motif | agents | 95 |
| motif | analogy | 1 |
| motif | arrows | 3 |
| motif | attention | 5 |
| motif | audio | 2 |
| motif | biology | 1 |
| motif | charts | 50 |
| motif | circuit | 4 |
| motif | claims | 2 |
| motif | code | 4 |
| motif | codec | 1 |
| motif | compute | 160 |
| motif | conditions | 1 |
| motif | context | 1 |
| motif | contrastive | 1 |
| motif | control | 145 |
| motif | correspondence | 2 |
| motif | data | 473 |
| motif | derivation | 1 |
| motif | design-space | 2 |
| motif | dialogue | 2 |
| motif | diffusion | 1 |
| motif | distributions | 1 |
| motif | editing | 1 |
| motif | embedding | 1 |
| motif | embeddings | 7 |
| motif | encoders | 1 |
| motif | environment | 3 |
| motif | environments | 6 |
| motif | episodes | 1 |
| motif | errors | 1 |
| motif | evaluation | 58 |
| motif | evidence | 1 |
| motif | examples | 1 |
| motif | exchange | 1 |
| motif | explanation | 2 |
| motif | failures | 1 |
| motif | features | 1 |
| motif | flowchart | 1 |
| motif | formulas | 1 |
| motif | gates | 1 |
| motif | generation | 1 |
| motif | generative | 4 |
| motif | graphics | 1 |
| motif | graphs | 7 |
| motif | groups | 1 |
| motif | hardware | 70 |
| motif | images | 1 |
| motif | inputs | 1 |
| motif | labels | 2 |
| motif | latent | 4 |
| motif | layout | 13 |
| motif | legend | 1 |
| motif | legends | 2 |
| motif | limitations | 1 |
| motif | losses | 1 |
| motif | masking | 1 |
| motif | math | 3 |
| motif | matrices | 2 |
| motif | mechanisms | 2 |
| motif | memory | 127 |
| motif | merging | 1 |
| motif | meshes | 1 |
| motif | methods | 2 |
| motif | ml | 3 |
| motif | models | 201 |
| motif | modules | 2 |
| motif | motif | 180 |
| motif | narration | 1 |
| motif | network | 124 |
| motif | neurons | 1 |
| motif | noise | 1 |
| motif | objectives | 2 |
| motif | operations | 1 |
| motif | operators | 2 |
| motif | optimisation | 3 |
| motif | outputs | 2 |
| motif | patches | 1 |
| motif | people | 13 |
| motif | pipeline | 9 |
| motif | predictions | 1 |
| motif | probing | 1 |
| motif | programs | 1 |
| motif | prompts | 2 |
| motif | reasoning | 5 |
| motif | renders | 1 |
| motif | representations | 1 |
| motif | results | 1 |
| motif | retrieval | 3 |
| motif | samples | 1 |
| motif | scheduling | 2 |
| motif | scope | 1 |
| motif | scores | 2 |
| motif | search | 4 |
| motif | selection | 1 |
| motif | sequences | 1 |
| motif | sets | 1 |
| motif | software | 3 |
| motif | status | 37 |
| motif | status-misc | 2 |
| motif | storage | 1 |
| motif | task-maps | 1 |
| motif | tasks | 2 |
| motif | taxonomy | 3 |
| motif | tensors | 2 |
| motif | theory | 2 |
| motif | time | 31 |
| motif | tokenisation | 1 |
| motif | tokens | 2 |
| motif | tools | 2 |
| motif | traces | 1 |
| motif | training | 44 |
| motif | trajectories | 2 |
| motif | transfer | 1 |
| motif | trees | 1 |
| motif | validation | 1 |
| motif | verdicts | 1 |
| motif | video | 2 |
| motif | views | 1 |
| motif | zoom | 1 |
| shape | annotation | 1 |
| shape | charts | 1 |
| shape | compute | 6 |
| shape | control | 78 |
| shape | data | 16 |
| shape | hardware | 16 |
| shape | layout | 2 |
| shape | markers | 1 |
| shape | memory | 1 |
| shape | memory-storage | 1 |
| shape | models | 1 |
| shape | network | 7 |
| shape | shape | 125 |
| shape | status | 20 |
| shape | status-misc | 1 |
| shape | time | 3 |
