# Puaan Eco Tours

Website for **Puaan Eco Tours**, a safari company based in Narok, Kenya, founded in 2025 by Kamwaro Ole Saruni Andrew (Kenya Tour Guide, Silver Grade).

> *experience it*

A fast, plain HTML and CSS site. No frameworks, no build step, no database. Edit a file, push it, and the site updates.

- **Live site:** `https://your-domain-here`
- **Hosting:** Vercel (deploys automatically from this repo)

---

## Pages

| File | Page |
|---|---|
| `index.html` | Home: hero, featured safaris, about teaser, booking call to action |
| `about.html` | About us and management |
| `safaris.html` | All six safaris as cards |
| `safari-kenya-classic-8-days.html` | Kenya Classic Safari (8 days) |
| `safari-migration-safari-9-days.html` | Tailored Safari: Migration Time (9 days) |
| `safari-rift-valley-challenge.html` | The Rift Valley Challenge (9 days) |
| `safari-kobe-tortoise-rift-valley-west-to-east.html` | Kobe Tortoise Rift Valley Challenge: West to East (8 days) |
| `safari-kenya-tanzania-10-days.html` | East African Moment: Kenya and Tanzania (10 days) |
| `safari-all-about-elephants.html` | All About Elephants (10 days) |
| `gallery.html` | Photo gallery |
| `contact.html` | Booking request form, contact details, directions |

## Folder structure

```
puaan-site/
├── index.html
├── about.html
├── safaris.html
├── safari-*.html        (one page per safari)
├── gallery.html
├── contact.html
├── style.css            (all styling, shared by every page)
├── README.md
└── images/
    ├── logo.png
    ├── hero.jpg
    ├── about.jpg
    ├── gallery-01.jpg ... gallery-12.jpg
    └── <safari-name>.jpg   (one per safari)
```

---

## How to edit

Open any `.html` file in a text editor (VS Code is ideal), change the text between the tags, save, and push.

### Change text, prices or an itinerary day
Open the page and find the text. Each itinerary day is one line like this:

```html
<li><b>Day 3</b>Full-day game drives in Samburu National Reserve.</li>
```

Edit the sentence only. Leave the tags (`<li>`, `<b>`) as they are.

### Change a color or font size
Everything is in `style.css`. The brand colors are at the top, under `:root`:

```css
--bg:#120d09;    /* page background */
--sun:#e8731a;   /* sunset orange (buttons) */
--gold:#e2a93b;  /* gold (accents) */
```

Change a value there and it changes on every page.

### Change the contact details
The phone number, WhatsApp link and email appear in the **footer** of every page and on `contact.html`. Use your editor's find and replace across all files:

- Phone: `+254 711 240430`
- WhatsApp: `https://wa.me/254711240430` (number in international format, no `+` or spaces)
- Email: `puaankenyasafaris@gmail.com`

### Change the nav or footer
The header menu and footer are repeated on each page, so a change means editing all pages. Use find and replace to do it in one go.

### Add a new safari
1. Copy an existing `safari-*.html` file and rename it, for example `safari-my-new-safari.html`.
2. Edit the title, description, banner text and the list of days.
3. Add a photo called `my-new-safari.jpg` (the same name as the page, without `safari-`) to `images/`.
4. In `safaris.html`, copy one `<a class="card" ...>` block and change its link, title, duration and route. Do the same in `index.html` if you want it featured.

### Add more gallery photos
In `gallery.html`, copy one `<figure>...</figure>` line, change the number in the file name, and write a short description in the `alt="..."` part. Then add the matching photo to `images/`.

---

## Images: read this first

A wrong file name is the most common reason a picture doesn't show.

- The name in the HTML must match the file **exactly**, including the extension.
- `.jpg` and `.jpeg` count as **different** names. This site uses `.jpg`.
- Names are **case-sensitive** on Vercel. Use lowercase, with `-` instead of spaces.
- If you have a `.png`, `.webp` or `.jfif`, convert it to JPG first (for example at squoosh.app).
- Keep photos under about 300 KB each. Large photos make the site slow.
- Wide photos work best: about 1600 px wide for banners, any size for gallery and cards.

The page tells the browser where to look. If an image is missing, the page still works. It falls back to a sunset gradient.

---

## Booking form

`contact.html` has a booking request form. Visitors fill it in and click **Send on WhatsApp**, which opens WhatsApp with their details already typed. There is no server, so nothing is stored on the website. If you want it to send email instead, a form service such as Formspree or Web3Forms can be added.

Each safari page also has a **Book on WhatsApp** button that pre-fills that safari's name.

---

## Run it on your computer

No installation needed. Double-click `index.html` and it opens in your browser. For auto-refresh while editing, use the **Live Server** extension in VS Code.

## Deploy

1. Make your changes.
2. Commit and push:
   ```bash
   git add .
   git commit -m "Describe your change"
   git push
   ```
3. Vercel rebuilds the site automatically. It's usually live in under a minute.

If a change doesn't appear, hard-refresh the browser (Ctrl+F5).

### Domain
The domain is managed in the Vercel dashboard, under the project's **Domains** tab.

---

## Tech notes

- Plain HTML5 and CSS, no JavaScript framework. One small script powers the booking form.
- Fonts: Fraunces and Hanken Grotesk, loaded from Google Fonts.
- Responsive: works on phones, tablets and desktops.
- Accessible basics: visible keyboard focus, image descriptions, and reduced-motion support.

## Credits and notes

- Photos belong to their owners. Only use photos you have permission to publish.
- &copy; 2026 Puaan Eco Tours. All rights reserved.
