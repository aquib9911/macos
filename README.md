# Aquib · macOS

Live at **https://aquib9911.github.io/macos/**. Everything on the site can be changed from GitHub in the browser. No code, no software.

A portfolio that looks and moves like a Mac desktop: draggable project icons, glass windows, a magnifying dock, a Genie minimise, a CV window and a Downloads stack.

## The files

| File or folder | What it is |
|---|---|
| `index.html` | The whole site. **All the words, links and picture paths are in two lists near the top of the script: `SITE` and `PROJECTS`.** This is the file you edit. |
| `assets/` | The wallpaper, the dock icons, and any pictures or files you add |
| `README.md` | This guide |

After every change, the live site updates in 1 to 2 minutes. If you don't see it, refresh with **Ctrl + Shift + R** (Windows) or **Cmd + Shift + R** (Mac).

---

## Change text or links

1. Open `index.html` on GitHub and click the **pencil icon** (Edit).
2. Press **Ctrl + F** (Windows) or **Cmd + F** (Mac) and search for `const SITE`. Everything you'd want to change starts there.
3. Change the words inside the 'quotes'.
4. Click **Commit changes**.

Keep the quotes and the commas at the end of lines exactly as they are. To add something to a list (a skill, a job, a client), copy a whole line, paste it below, and change the words.

What's in `SITE`:

| Setting | What it changes |
|---|---|
| `name`, `email` | Your name and the address the **Mail** icon opens |
| `social` | The **Instagram** dock icon: `label` and `url` (your profile link) |
| `wallpaper`, `wallpaperBlur` | The background picture, and how blurred it is (`0` = sharp) |
| `cv` | The **CV** window: `intro`, `canDo`, `experience`, `clients`, `interests` |
| `bin` | The **Trash** window: `title`, `subtitle`, and `items` (each a picture `img` with a `caption`) |
| `downloads` | The files in the **Downloads** stack |
| `appAlerts` | The joke pop-ups for **Ae**, **Ps**, **Ai** and **Error** |

---

## Add or change a project (desktop icon)

Search for `const PROJECTS`. Each line is one icon on the desktop:

```js
{ id:'brand', title:'Brand Identity', client:'Client One', year:2025, x:14, y:16, colors:['#111','#f4f1ea'], pattern:'rings', type:['Art Direction','Logo','Typography'] },
```

- `id`: a short unique name, lowercase, no spaces
- `title`, `client`, `year`: shown on the icon and in its window
- `x`, `y`: where the icon sits, in % of the screen (`x:0` is the left edge, `y:0` the top). Phones use the same spots, stretched to fit the taller screen.
- `type`: the list shown next to **Type:** in the window
- `colors` and `pattern`: the drawn artwork used until you add a picture. Patterns: `rings`, `stripes`, `dots`, `split`, `sun`, `grad`, `grid`

Optional extras, added inside the `{ }` with a comma before each:

```js
img:'assets/brand-cover.jpg',
preview:['assets/brand-1.jpg', 'assets/brand-2.jpg', 'assets/brand-3.jpg'],
link:'https://your-project-link.com',
desc:['First paragraph about the project.', 'Second paragraph.']
```

- **img** is the icon picture and the thumbnail at the top of the window.
- **preview** is the picture grid inside the window, in the order you list them.
- **link** adds a "> Click here <" link.
- **desc** replaces the placeholder description.

To add a project, copy a whole line, paste it below, and change it. To remove one, delete its whole line.

---

## Add or change a picture

1. Open the `assets` folder in the repo.
2. Click **Add file → Upload files**.
3. Drag the picture in and click **Commit changes**.

Name pictures in lowercase with no spaces, for example `brand-cover.jpg`. JPG, PNG or WebP all work. Keep each picture under about 1 MB so the site stays fast.

To **replace** a picture, upload a new file with the **same name**. GitHub replaces the old one. That's also how you change the wallpaper: upload a new `wallpaper.jpg`.

To **delete** a picture, open it in the `assets` folder, click the **⋯** menu, then **Delete file**.

---

## Dock icons

Each dock icon is a picture in `assets/`. To swap one, upload a square PNG (256 × 256 works well) with the **same name**:

| Dock icon | File |
|---|---|
| After Effects, Photoshop, Illustrator | `aftereffects.png`, `photoshop.png`, `illustrator.png` |
| CV | `notes.png` |
| Error | `error.png` |
| Gallery | `gallery.png` |
| Instagram, Mail | `instagram.png`, `mail.png` |
| Downloads, Trash | `downloads.png`, `trash.png` |

---

## Downloads stack

Clicking **Downloads** in the dock fans these files up out of the icon. Upload each file to `assets/`, then point to it in `downloads` inside `SITE`:

```js
{ name: 'CV.pdf', url: 'assets/CV.pdf' },
```

Files without a `url` just wiggle when clicked. Add or remove lines to change how many files show.

---

## If the site looks blank after an edit

A missing quote or comma in `index.html` stops the site from loading. Open the file, click **History**, and compare with the last version that worked, or click the earlier version and copy it back.
