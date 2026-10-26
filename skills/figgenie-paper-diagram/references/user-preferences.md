# The user's own drawing habits (always on)

Learned while redrawing the method and threat-model figures of one of the user's papers (2026-10). These rules
apply to every figure this user asks for. Where they conflict with the corpus defaults, these win. The print
floors still apply (type ≥ 6 pt, canvas inside the column, contrast). A named style (`charon`, …) the user asks
for explicitly overrides the look rules in §1, but not the content rules in §4.

## 1. Avoid the "drawn by AI" look

The user rejected the first drafts because they looked AI-made, even though the layout and content were fine.
What caused it: pale tinted cards with a border around every module, many boxes that were all the same,
several font sizes, and boxes much larger than their text.

- Group a module with a **pale grey background and no border** (`#F1F1F1`, radius about 3.5 pt). Do not draw a
  tinted card with an outline around every group.
- Give an outline only to boxes that stand for one thing (a loss, a model part). Use white fill and a thin ink
  outline.
- A horizontal divider between lanes may be a little heavier (about 1 pt grey) so that the two lanes read as two.

## 2. Encoding

- **Trainable or frozen:** use the fire icon (trainable) and the snowflake icon (frozen). Put the icon **on the
  model icon**, not beside it, and align the icons of all models horizontally. Do not show it with fill colour
  (for example, blue for frozen); the user found that ugly.
- **Watermark carried in the weights:** a drop icon on the model, the same as in the paper's threat-model figure. When fire, snowflake
  and drop occur together, keep all three on the model and explain them in the legend.
- **Lines:** solid = forward pass, dashed = gradient update. Use one line width for the whole figure.
- **Losses:** every loss box has a red outline, and its gradient-update lines are red too. Use the same colour
  for all losses. Do not give one loss black lines and the others red lines.
- **Arrowheads:** choose a shape and size that do not merge with the line when two arrows meet at one box. Check
  the joins at 6× zoom.
- **Update routes:** route them around the outside of the figure, as in the original slides. The user rejected
  short arcs drawn straight out of the loss. When one loss updates two modules, draw **two separate lines** from
  the loss. Do not draw one line that splits.
- Line up parallel route groups horizontally, and make returning routes end on the same x.

## 3. Numbers, text and legend

- Circled numbers ①②③ go **on the losses**, so that the body text can call each one back. Make them black,
  like the black circled numbers in the text (`\lossnum`). Every number in the figure needs a call-back in the
  text.
- Use **one font size** for all labels (7 pt), at most one smaller size for sub/superscripts. Size each box to
  fill its text: no large box with small text in it.
- Centre an element vertically between its neighbours: the gap above and the gap below must be equal, and no
  box may touch a line.
- Put **one legend in the top-right corner**, holding both the icons and the line styles. Do not split the
  legend over two places. A legend replaces repeated labels such as "update" written on each line.
- Font: Carlito (metric-compatible with Calibri) with `text-rendering="geometricPrecision"` on the root. Without
  it the letter spacing in the PDF was uneven.
- No large empty corners. Fill an empty area with a short label that says what happens there (for example,
  "natively outputs watermarked logits").

## 4. Content

- Leave out any detail the reader does not need to follow the method (the user removed "Embedding E"). An
  unnecessary detail makes the figure harder to read.
- Every input must show where it comes from. For example, the anti-watermarked text, and the input of a
  regulariser such as L_norm from M.
- When reviewers did not understand what each loss optimises, show each loss as its own box with its own
  update route, so that the figure answers "this loss updates which part".
- The outputs must carry the property the method gives them. For example, the student's logits carry the drop,
  because the point is that the student natively outputs watermarked logits.

## 5. Consistency across the paper

- All figures of a paper share one set of icons, colours, line widths and font. A new figure reuses the helpers
  of an existing one. Ask whether the user has original slides (pptx) with
  icons; reuse those before drawing new ones.
- After redrawing one figure, check the other figures of the paper for the same style and offer to redraw them
  too.

## 6. Working with this user

- Show a rendered PNG after every round of changes. The user judges from the picture, not from a description.
- Ask decisions with AskUserQuestion, in Chinese.
