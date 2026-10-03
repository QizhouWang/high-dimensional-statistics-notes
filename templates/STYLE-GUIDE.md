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
