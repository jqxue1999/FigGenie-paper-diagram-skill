# AI-venue exemplars (`assets/exemplars/ai/`)

Reference figures for the AI family (`meta.family: ai`): the Figure 1 of every designed paper figure of ICLR, ICML,
NeurIPS, CVPR, ACL and AAAI 2023-2026 that was not rated bad — 3,210 figures in three tiers, found with
`scripts/find_ai_exemplars.py` and chosen by the user before a figure is drawn (`references/ai/exemplar-retrieval.md`).
They are references for study: a drawer borrows the device that serves the figure at hand and keeps whatever that
figure needs that no exemplar shows; a figure that looks like none of them is the normal outcome.

```
cards.jsonl                    one retrieval card per figure (all tiers): paper title, authors, link, abstract, kinds
                               (primary first), variant, sub-field, tags, layout, what the figure holds, objects,
                               keywords; tier 1 adds the record's summary and lesson; `architecture: <type>` on the
                               86 whole-model figures of references/ai/model-architectures.md
figures/<id>/print.webp        the figure as printed (publisher PDF at 150 dpi, cropped to the ink)      tiers 1-2 *
figures/<id>/source.svg        the same region as SVG: text kept as <text> with its fonts and sizes, embedded fonts
                               dropped, bitmaps reduced to small stand-ins at their place; read it for how the
                               figure is built (sizes, colours, strokes, grouping, how pictures are framed)
figures/<id>/semantics.json    the deep semantic record (tier 1)
figures/<id>/manifest.json     provenance, attribution, tier, the card fields that matter when reading the figure
thumbs/<id>.webp               360 px wide, for the numbered candidate sheets (every figure)
vocab.json                     kinds with variants, sub-fields, arrangements, the tag vocabulary with definitions
SOURCES.md                     where the figures come from and their copyright
```

| tier | figures | files |
|---|---:|---|
| 1 — a deep semantic record | 336 | full pack: print, SVG, semantics, manifest |
| 2 — rated good by the user | 638 | full pack for the 422 whose vector figure matches the published picture, else card and thumbnail |
| 3 — the other designed figures (unrated, or rated ok, which the card says) | 2,236 | card and thumbnail; the SVG and a larger picture from the local corpus when it is present, else the gallery link |

\* 792 packs in all: tiers 1 and 2 as above, plus the 34 whole-model architecture figures of tier 3 (and two whose
vector comes from the arXiv source, `vector_from: arxiv-source` on the card). Figure ids are `<paper>_fig<N>`; `_g1`
marks a figure whose PDF extraction did not match the published picture.

Searching: `python3 scripts/find_ai_exemplars.py search --kind ... --subfield ... --tags ... --objects ... --text ...`
ranks the cards by kind, field, layout, content, tags and meaning (BM25 over objects, keywords, what the figure shows
and the paper's title and abstract); `sheet` draws a numbered candidate sheet for the user; `files` lists what to look
at and read for each pick; `card` prints one card; `vocab` the vocabulary. What each sub-field draws differently and
its exemplars: `references/ai/domains.md`; the eight kinds: `references/ai/kinds.md`.

Rebuild from the corpus with `python3 scripts/distill/build_ai_exemplars.py` (reads `ai-corpus/`, the gallery clone and
`ai-parts/architectures/selection.json`; re-runs only touch figures whose source changed; `--force` rebuilds). The
figures belong to their authors and publishers (`SOURCES.md`); each manifest carries the paper's link.
