# macos

A portfolio website that looks and moves like a macOS desktop.

- Draggable desktop icons for each project, with marquee multi-select
- Project windows that zoom open from their icon, with drag, close, zoom and a Genie minimise into the dock
- Liquid Glass styling for windows, alerts, tooltips and the dock
- A magnifying dock with tooltips, bounce, running dots and minimised-window thumbnails
- A Notes-style CV window (About me / CV / Interests)
- Joke alert pop-ups for the After Effects, Photoshop, Illustrator and Error icons
- A Downloads stack that fans files up from the dock
- A Trash you can drag icons into and put them back from
- Works on phones and respects "reduce motion" and "reduce transparency"

One file, no build step and no libraries: open `index.html` in a browser, or host the folder anywhere (for example GitHub Pages).

## Editing

Everything you would change is near the top of the `<script>` in `index.html`:

- `SITE`: your name, email, social link, wallpaper, CV content, Downloads files and alert messages
- `PROJECTS`: each desktop icon's title, client, year, type, description, position (`x`/`y` in % of the screen), and optional `img`, `preview` images and `link`

Images live in `assets/`.

## Credits

App icons and the wallpaper belong to their respective owners (Apple, Adobe, Instagram) and are used here as placeholders.
