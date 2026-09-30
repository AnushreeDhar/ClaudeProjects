# L'Arc des Pensées

Wisdom that rings when you touch it.

A single-page interactive piece that hangs ten philosophical quotes as beaded chains beneath the Arc de Triomphe. Each bead is a letter. Move your cursor or finger through the chains and they swing, collide and chime like a wind chime.

It is one self-contained `index.html`, with no build step and no dependencies apart from two Google Fonts.

## Features

- **The scene:** a night sky, the Paris skyline, the plaza, the Arc de Triomphe and the eternal flame beneath it, all drawn on canvas.
- **Beaded quotes:** the current quote hangs as chains of lettered beads. Beads glow where you have touched them.
- **Physics:** Verlet integration with stick, cloth and contact constraints. Sweep through the chains to disturb them. Click or tap to strum everything near the pointer.
- **Sound:** chimes are synthesized in the browser (tubular tones through a small convolution hall) and tuned to a pentatonic scale, so any cluster of strikes stays consonant. Audio starts after your first click or tap.
- **Ten quotes:** Socrates, Marcus Aurelius, Nietzsche, Camus, Kant, Seneca, Sartre, Aristotle, Heraclitus and Lao Tzu, each with its source.
- **Responsive:** a side-by-side layout on wide screens and a stacked layout on phones and tablets.
- **Accessible:** buttons have labels and visible focus, quote changes are announced through an `aria-live` region, and `prefers-reduced-motion` is respected.

## Controls

| Action | Input |
| --- | --- |
| Make the chains chime | Move the pointer through the letters |
| Strum nearby chains | Click or tap |
| Next or previous quote | The arrow buttons, or the left and right arrow keys |
| Toggle sound | The Sound button, or `M` |

## Run locally

Open `index.html` in any modern browser. No server is needed.

## Publish with GitHub Pages

1. Create a repository and add `index.html` and this `README.md` to the root.
2. Go to **Settings > Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, select `main` and `/ (root)`, then save.
4. The site goes live at `https://<username>.github.io/<repository>/`.

## Customise

| What | Where in `index.html` |
| --- | --- |
| Quotes, authors and sources | The `QUOTES` array in the script |
| Colours and fonts | The CSS variables in `:root` |
| Chime notes | The `SCALE` array (frequencies in Hz) |
| Layout breakpoint | The `@media (max-width: 1199px)` block |

## Tech

- Vanilla HTML, CSS and JavaScript
- Canvas 2D for the scene and the chains
- Web Audio API for the chimes
- Cormorant Garamond and Josefin Sans from Google Fonts, with system fallbacks when offline
