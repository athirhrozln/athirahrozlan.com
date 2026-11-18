# DESIGN.md: athirahrozlan.com

Design direction for my portfolio site. Every choice has a one-line reason.

## Design read

Personal portfolio for two audiences: recruiters hiring for data and software roles (aviation and ESG companies in particular), and Malaysian SMEs looking for a freelancer.
Visual language: a calm, professional base with bold touches on the project cards and the main actions.

Dial: ENERGY 2 / RHYTHM 2 / MOTION 1

- **ENERGY 2:** a recruiter should trust it at a glance, and a client should still remember it.
- **RHYTHM 2:** the sections stay consistent so the page is easy to scan, with a few deliberate breaks (the project gallery, the contact box).
- **MOTION 1:** hover states only. Nobody should have to wait for animations to read a CV.

## Colour

Core palette: 2 colours + 1 accent. Neutrals don't count.

| Role | Value | Reason |
|---|---|---|
| Navy (core) | `#131B2A` | Header, logo, card outline and shadow. A serious, trustworthy base that ties every page element to the "ar" mark. |
| Off-white (background) | `#FAFAF8` | A warm off-white, softer than pure white for long reading. |
| Text | `#1B2433` headings, `#4A5568` body, `#5F6B7E` small labels | Every text colour passes WCAG AA (4.5:1). The small labels had failed at 3.7:1. |
| Accent | `#0369A1` | One blue for links and the role line. It replaces `#0EA5E9`, which failed contrast at 2.65:1. |

Status colours are functional, not decorative:

| Status | Colour pair | Contrast | Reason |
|---|---|---|---|
| In progress | `#B45309` on `#FEF3C7` | 4.5:1 | Amber means work that isn't finished yet. |
| Completed | `#047857` on `#D1FAE5` | 4.8:1 | Green means done. |

The WhatsApp button keeps the WhatsApp green `#25D366` so people recognise it at once. Its text is navy (8.7:1), because white text failed at 2:1.

## Typography

| Use | Typeface | Reason |
|---|---|---|
| Headings and logo | Bricolage Grotesque 700–800 | It has character and some warmth, which adds the "bold" side without being loud. |
| Body text and labels | Source Sans 3 400/600 | Built for reading. It stays clear at small sizes on a phone. |
| Monospace | None | Removed. Monospace labels were decoration ("terminal look"), not code. |

- Labels are in sentence case with normal letter spacing. No wide-tracked UPPERCASE labels.

## Shape and depth

- **Identity motif:** the "raised" card, a 1.5px navy border with a hard navy 4px offset shadow and no blur. It is used **only** on project cards and the WhatsApp button, because those are what I want people to click.
  - In-progress cards use an amber shadow so unfinished work stands out from completed work.
  - Every other element is flat. Not everything floats.
- **Radius:** cards 18px, buttons 10px, status badges fully round. The badges are the only pill shape, and they are small labels, not containers.

## Components

- **Status badge:** real status only ("In progress" or "Completed"). There is no pulsing dot; the colour and the word already say it.
- **Arrows:** `↗` only on links that leave the site (GitHub, LinkedIn, the paper, certificates), so people know a new tab opens. No decorative `→`.
- **Project thumbnails:** real screenshots when available. Until then, each illustration is labelled **"Illustration"** and contains no invented numbers.
- **Buttons and links:** specific wording that says what happens ("See my projects", "WhatsApp me"). No "Learn more" or "Get started".

## Accessibility (non-negotiable)

- All text passes WCAG AA contrast.
- Every link and button shows a clear focus outline when using the keyboard (Tab): 2px navy outline, offset 3px.
- `cursor: pointer` on every interactive element.
- No continuous animation. Hover movement switches off under `prefers-reduced-motion`.

## Copy

- No em dashes. Commas, full stops or brackets instead.
- No buzzwords ("seamless", "cutting-edge", "passionate").
- Facts with evidence: the published paper, certificates, real project names. No invented statistics.
