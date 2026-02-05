# Contributing to LithoBlocks Documentation

This documentation site is built with [Mintlify](https://mintlify.com). Follow these conventions so the docs stay consistent and deliver a great developer experience.

## File layout

- **Pages** are MDX (or Markdown) files. Navigation in `docs.json` references paths **without** file extension (e.g. `quickstart`, `guides/placeholders`).
- **Locations**:
  - Root: Get Started pages (`index.mdx`, `quickstart.mdx`, `connecting-slack.mdx`).
  - `guides/`: How-tos, reference, and explanation pages (e.g. `guides/templates-placeholders.mdx`).
  - `architecture/`: Optional explanation-style architecture docs.
  - `api-reference/`: API overview page; endpoint pages are **auto-generated** from `api-reference/openapi.json` (do not add manual endpoint MDX).
- Do **not** add nav entries pointing at the `docs/` folder; that folder is reference material only for structure and copy.

## Content types (Diátaxis)

Assign each page a single content type and structure it accordingly:

| Type | Goal | Structure | Use for |
|------|------|------------|---------|
| **Tutorial** | Learning by doing | Prerequisites → Steps → Next steps | First-run experience (e.g. quickstart). |
| **How-to** | Accomplish a task | Prerequisites → Task → Verify / Troubleshoot | "How do I add buttons?", "How do I use placeholders?" |
| **Reference** | Look up details | Scannable; properties, params, examples | Block types, directive syntax, API-like reference. |
| **Explanation** | Understand concepts | What / How / Why / When to use | Architecture, template processing, Slack flow. |

Use [Mintlify content templates](https://www.mintlify.com/docs/guides/content-templates) as the base; adapt using structure and copy from the reference material in `docs/`.

## MDX and components

- **Frontmatter**: Every page must have `title` and `description` (optional `icon`) for SEO and previews.
- **Structure**: Use **Steps** for sequential instructions, **Accordion** / **AccordionGroup** for optional detail, **Card** / **CardGroup** for "Next steps" and related links.
- **Code**: Use fenced code blocks with language labels; **CodeGroup** for multi-language examples. Keep snippets copy-paste friendly.
- **Emphasis**: Use **Note**, **Tip**, **Warning** callouts for prerequisites, gotchas, and best practices.
- **API-like reference**: Use **ParamField** / **ResponseField** for reference pages (block properties, directive options).
- **Linking**: Link between docs using Mintlify paths **without** `.md` (e.g. `/quickstart`, `/guides/placeholders`).

## Best practices

- **Prerequisites**: List only what's necessary; link to other docs (e.g. "Completed [Quickstart](/quickstart)").
- **One primary goal per page**: Avoid mixing tutorial and reference; split if needed.
- **Next steps / Related**: End tutorials and how-tos with clear links (Cards or a short list) to the next logical pages.
- **Assistant-friendly**: Clear headings and consistent structure help the Mintlify assistant answer questions in context.

## Reference material

The `docs/` folder contains internal reference (structure, topics, snippets). Use it to guide new MDX content; do **not** point Mintlify navigation at `docs/`. All published pages live at repo root or under `guides/` and `architecture/`.
