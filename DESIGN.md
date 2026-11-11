---
name: Pearl Street
description: A family dental clinic site for Tamil Nadu built like a clinic's front desk: flat white tiles on a pale mint page, one action colour, one dark ink tile.
colors:
  page: "#EFF4F1"
  tile: "#FFFFFF"
  ink: "#11211D"
  text: "#33423E"
  muted: "#55645E"
  line: "#D5DFD9"
  line-strong: "#A9B9B0"
  on-ink: "#EAF1ED"
  on-ink-muted: "#B7C6BE"
  clay-brand: "#C2471A"
  clay-brand-deep: "#9A3611"
  clay-tint: "#FBE6DB"
  sage-brand: "#1B7F5F"
  sage-brand-deep: "#125C44"
  sage-tint: "#DCF1E8"
  mist-brand: "#2557C7"
  mist-brand-deep: "#1A3F96"
  mist-tint: "#E1E9FB"
  olive-brand: "#66701C"
  olive-brand-deep: "#4C5413"
  olive-tint: "#EDF0D6"
  whatsapp: "#0F7F3F"
  open-green: "#17924A"
  closed-red: "#C0392B"
  error-red: "#B3261E"
typography:
  display:
    fontFamily: "Catamaran, Mukta Malar, Nirmala UI, system-ui, sans-serif"
    fontSize: "clamp(2.15rem, 8.6vw, 3rem) on phones, up to 4.5rem on wide screens"
    fontWeight: 800
    lineHeight: 1.04
    letterSpacing: "-0.03em"
  headline:
    fontFamily: "Catamaran"
    fontSize: "clamp(1.9rem, 3.5vw, 2.85rem)"
    fontWeight: 800
    lineHeight: 1.1
    letterSpacing: "-0.02em"
  title:
    fontFamily: "Catamaran"
    fontSize: "1.28rem"
    fontWeight: 700
  tamil-subtitle:
    fontFamily: "Catamaran"
    fontSize: "clamp(1.05rem, 1.4vw, 1.2rem)"
    fontWeight: 700
  body:
    fontFamily: "Mukta Malar, Nirmala UI, Segoe UI, system-ui, sans-serif"
    fontSize: "1.09rem"
    lineHeight: 1.62
rounded:
  tile: "22px"
  control: "12px"
  icon: "14px"
spacing:
  gutter: "clamp(16px, 4vw, 40px)"
  gap: "clamp(10px, 1.2vw, 14px)"
  section: "clamp(56px, 7.5vw, 104px)"
  container: "1200px"
  tap: "48px"
---

# Design System: Pearl Street

## Overview

**Creative North Star: "The Front Desk."** A patient who walks into a clinic asks the same things at the counter: are you open, who is the dentist, where are you, can I get an appointment. Pearl Street answers those on the first phone screen, as tiles: a tile in the action colour with the live Open Now status and the phone number, a white tile with the dentist's name and degree, and the two buttons (Book a Visit, WhatsApp). Everything after that keeps the same language: flat white tiles on a pale mint page.

It is clearly not Northline (white page, navy ink, round shapes and squiggles, Baloo type, handwritten notes), not Signboard (cream paper, ink boards with mustard frames, condensed Anek Tamil) and not Ivory Lane (teal, serif).

**Key characteristics**
- Pale mint page (`page`), white tiles (`tile`) with 22px corners, deep green-black ink.
- Three surfaces only: white tile (content), action-colour tile (the answer or the thing to press), ink tile (emergency and footer).
- No shadows on the page. Only things that float above it (menus, the phone action bar, the WhatsApp button, the theme picker) get one soft offset shadow.
- Lists live inside one tile with hairline dividers; they are not grids of small cards.
- Rounded-rectangle controls (12px), square-ish icon holders (14px). No pills, no circles except portraits and the status dot.
- Catamaran for headings and Tamil, Mukta Malar for text. Both cover Tamil and English.

## Colors

- **Page / Tile / Ink**: the page is tinted so white tiles separate from it without borders or shadows.
- **Action colour (theme)**: primary buttons, the Open Now tile, selected chips, the active step number, the bar above Tamil subtitles, focus outlines. Themes: `clay` (default, terracotta), `sage`, `mist`, `olive`. Each sets `--brand`, `--brand-deep` and `--brand-tint`. White text on `--brand` is 4.5:1 or better in all four.
- **Ink tile**: `ink` background with `on-ink` text, used for the emergency block, the Book tile in the quick actions and the footer.
- **WhatsApp green** is kept for WhatsApp only (icon, the form's send button, the floating button).

**Rules**
- One action colour. Nothing else fills a button except WhatsApp green on WhatsApp actions.
- Text is ink, text or muted on white and on the page; on the ink tile it is white, `on-ink` or `on-ink-muted`.

## Typography

- **Display** (hero headline): Catamaran 800, tight. The area name inside it takes the deep action colour.
- **Headline** (section headings): Catamaran 800. Each carries a Tamil subtitle in Catamaran 700 with a 44 × 5px action-colour bar above it that grows in when the heading comes into view.
- **Body**: Mukta Malar 400 at 1.09rem; intros up to 62ch.
- **Notes** (`.note`): short helper lines in the deep action colour with a small arrow. There is no handwriting face in this template.

## Layout

- The hero is one grid (`.desk`). Phone order: headline, status tile + dentist tile side by side, the two buttons, the paragraph, the trust lines, the photo. From 960px the copy sits on the page at the left and the photo tile stands at the right, with the status and dentist tiles under it.
- Quick actions are four tiles (2 × 2 on phones); the Book tile is the ink tile.
- Treatments, promises, facts, fees and FAQs are single tiles with divided rows. Doctors and first-visit steps are separate tiles because each is a real object.
- The gallery is a mosaic from 760px (first photo large) and a swipe row on phones.
- Section headings are left-aligned or centred; the FAQ and first-visit headings stick beside their lists on wide screens.

## Components

- **Buttons**: 50px (56px large), 12px corners, Catamaran 700. Primary = action colour; outline = white with a 2px inner line; on the ink tile primary is white and outline is a white line.
- **Chips**: white 54px tiles with a tinted icon square; selected fills with the action colour.
- **Open Now tile**: action colour, clock icon, status in Catamaran 800 with a pulsing white dot when open (hollow when closed), and a Call link with the number.
- **Dentist tile**: round portrait, name, degree, "Meet your dentist". With `specialists` on it becomes a team tile with the number of specialists.
- **Fields**: page-coloured fill, 54px, 12px corners; focus turns the field white with an action-colour border and tint halo.
- **Header**: sticky, page-coloured, hides on scroll down. Logo = action-colour tile holding a white dot, the clinic name, and the small "Dental Clinic" line under it. Phone menu is a tile dropdown.
- **Phone action bar**: a floating white tile with Book (filled), Call, WhatsApp, Directions.

## Motion

One authored moment: on load the front desk is laid out tile by tile (pure CSS, visible by default, off for reduced motion). After that only scroll moves things: the treatments strip slides with the scroll, treatment rows and chips ease in, portraits pop, heading bars grow, the step number lights up. The live dot on the Open Now tile is the only thing that moves on its own.

## Do's and Don'ts

**Do**
- Keep every block a tile, or sit it directly on the page. Nothing in between.
- Keep the first phone screen to: headline, the two tiles, the two buttons.
- Use `--brand-tint` for icon squares and soft panels; `--brand-deep` for coloured text.

**Don't**
- Add shadows, gradients, glass, borders-as-decoration or decorative shapes.
- Put a tile inside a tile.
- Add a second accent colour, handwriting, pills or circular buttons.
- Add testimonials, star ratings, review counts or before/after photos to any layout.
