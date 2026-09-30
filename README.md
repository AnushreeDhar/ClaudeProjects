# Happy Birthday Madan

A single-page birthday site for **29 October**. It is one self-contained `index.html` with no build step and no dependencies.

## What's on the page

- **Cover:** a stacked "Happy Birthday, Madan" headline, a live countdown to 29 October and a throwback photo in an arch frame.
- **The Arc:** swipe sideways from the cover to an interactive canvas of the Arc de Triomphe. Philosophy quotes hang as beaded chains that chime when you move through them. Press `M` to toggle sound and use the arrow keys to change the quote.
- **Celebration section:** scroll down for skylines of Paris, Boston, New York and London, a Manchester United fan block, and a Formula 1 card.

## Run locally

Open `index.html` in any modern browser.

## Publish with GitHub Pages

1. Create a repository and add `index.html` and this `README.md` to the root.
2. Go to **Settings > Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, select `main` and `/ (root)`, then save.
4. The site goes live at `https://<username>.github.io/<repository>/`.

## Customise

| What | Where in `index.html` |
| --- | --- |
| Name and headline | The `<h1>` inside `.cover` |
| Birthday date and countdown | The `tick()` function (`new Date(y, 9, 29)`; months start at 0) |
| Photo | The `<img>` in `.arch`, a base64 data URI. Replace it with a file path if you prefer |
| Quotes on the Arc | The `QUOTES` array |
| Fixtures and players | The `.stage` block |

## Notes

- Skylines, the stadium and the F1 car are original inline SVG drawings. No club crests, logos or official photos are used.
- Fonts (Cormorant Garamond and Josefin Sans) load from Google Fonts and fall back to system fonts offline.
- The cover photo is embedded in the file. If the repository is public, the photo is public too.
