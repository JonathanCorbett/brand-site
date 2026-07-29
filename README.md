# brand-site

Public. Front 1 — my own name.

One static page and the writing. This is the permanent distribution engine; it
is never sold and it survives every exit. The product brand is a separate repo
under a neutral name, and the two are deliberately not linked from here in a way
that makes the product look like a personal project.

## Structure

    index.html          the whole site — self-contained, no build step
    posts/              one file per piece, added as they're published

`index.html` inlines its own CSS and JS on purpose. No CDN, no external fonts, no
framework. It should still open from disk in ten years.

## Before this goes live

Five things need a human decision. Each is marked in the source with a `TODO`
comment, and the ones visible on the page carry a `.todo` class that draws a
dashed amber outline — so an unfinished item is impossible to miss in a browser.

| | What |
| - | ---- |
| 1 | **Domain.** Set it in the three meta tags at the top of `index.html`. |
| 2 | **Email list provider.** Point the form's `action` at a real endpoint, then delete `notWired()` and the `.todo` class on the form. |
| 3 | **LinkedIn / GitHub / email** links under *Elsewhere*. |
| 4 | **Read the lede aloud.** It is my positioning in three sentences and it should sound like me, not like a draft someone handed me. |
| 5 | **Delete the `.todo` CSS rule** once nothing on the page uses it. |

The subscribe form is deliberately inert until item 2 is done. A form that
accepts an address and drops it is worse than no form.

## What must never appear here

- The employer's name, its products, its customers, or its domain. The
  background is described as *"regulated, high-consequence software"* — that
  phrasing does the work without naming anything.
- Anything that reads as representing the employer. Everything published under
  my own name is read that way by default, so it stays patterns and principles,
  never specifics.
- A link to the product that frames it as a personal side project. Market the
  product *through* my name; never let the product's identity *be* my name.

## Publishing a piece

1. `posts/YYYY-MM-DD-slug.html`, same self-contained pattern.
2. Swap the `.empty` block in `index.html` for the `ul.plain` list — the markup
   is already there, commented out, newest first.
3. Commit with a message saying what the piece argues, not just its title.

Phase 0 gate is publishing piece #1. The site is scaffolded; the writing isn't.
