# Valentines Project

## What this is
A single-page interactive Valentine's Day proposal web app for Tanvi. No frameworks, no build step — pure vanilla HTML/CSS/JS in one file (`index.html`).

## Stack
- Vanilla HTML5, CSS3, JavaScript
- Canvas API for particle effects
- No dependencies, no package.json

## Structure
- `index.html` — entire app (HTML + CSS + JS in one file)
- `background.jpg` — background image

## Key customization constants (top of `<script>`)
- `TITLE_TEXT` — main heading
- `NO_POPUP_LINES` — array of messages shown when "No" is clicked (cycles through them)
- `NO_TELEPORT_EVERY_MS` — how often the No button auto-moves (ms)
- `CONFETTI_COLORS` — particle colors for the celebration burst

## How the No button works
- Absolute positioned inside `.arena`
- Auto-teleports every `NO_TELEPORT_EVERY_MS`
- Also dodges on mousemove if cursor gets within 130px
- On touch: moves on touchstart to simulate evasiveness
- If somehow clicked, shows modal with escalating messages from `NO_POPUP_LINES`

## Particle system
- `burst()` spawns particles at random screen positions
- `step()` is the rAF loop — applies gravity (0.06), friction (0.99), fades by life
- `doYesCelebration()` orchestrates: hides UI, shows overlay, fires bursts

## Tone
Casual and funny. The copy is intentionally unhinged ("I suck", "LETS GOOOO"). Keep that energy when editing text.
