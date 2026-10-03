# Lecture formatting standards

Use `assets/lecture.css` for every lecture. Start with `templates/lecture.html` and adjust the relative stylesheet path for the destination.

## Typography

- Text: Arial, with Helvetica Neue and Chinese font fallbacks. Do not introduce a separate font for individual text blocks.
- Body: 17 px, line height 1.85; 16 px on small screens.
- Notes, examples, and footnotes: 14 px, line height 1.8.
- Section headings: 25 px; subsection headings: 19 px.
- Text weights: 400 regular and 600 emphasis/headings.
- Inline emphasis stays inline, including inside notes.
- Mathematical notation: native MathML; use fraction and radical elements instead of plain-text approximations. Math fonts may differ for mathematical glyphs.

## Structure

- Use numbered sections with stable anchors and a matching contents list.
- No banner, title page, or introductory metadata unless requested.
- Keep the user's conceptual framework and causal order; improve phrasing without introducing a new framework.
- Default to English and concise paragraphs.
- Put short examples immediately after the concept using `.sidenote`, without a title or reference number unless requested.
- Footnotes use superscript links and appear immediately below the relevant passage, with a return link.
- Use `.figure-pair` for paired images and `figure`/`figcaption` for figures.
- Avoid adding boxes and bold text merely for decoration.

## Update workflow

Edit and verify local files by default. Do not commit, push, or publish unless the user explicitly requests synchronization for that update.

## Semantic colors

Keep these mappings consistent across all notes:

| Content | Class | Color |
| --- | --- | --- |
| Setting and goal | `topic-setting` | Blue, `#195cb5` |
| Definitions | `topic-definition` | Teal, `#087b49` |
| Proofs | `topic-proof` | Purple, `#883fb0` |
| Examples | `topic-example` | Brown-orange, `#b45108` |

Wrap content in `<div class="topic topic-proof">…</div>` (substitute the type).
Color the heading and left rule; keep paragraphs in the common text color.
Short examples retain the small-note layout: `<aside class="sidenote topic-example">…</aside>`.
Always retain text labels: color is an additional cue, not the only distinction.

## Theorems and proofs

- Theorems use `topic topic-theorem` and proofs use `topic topic-proof`; both share the purple proof color.
- Give the theorem a number and label its explanation “Proof of Theorem N” so the relationship is explicit.
- Examples inside a proof retain the orange example color.
- Put further explanations in nearby `.sidenote.footnotes` with linked reference numbers.
- Connect consecutive lectures using `.page-navigation` at the end of each page.
- When publishing a stylesheet change, update the shared CSS version query on both lecture pages to avoid stale browser caches.
