# Vanshikasri Palanivel Rajan — Bharathanatyam Portfolio

Live site: [Netlify auto-deploys from GitHub `main` branch]  
GitHub repo: https://github.com/iampvr84/Dance-Portfolio  

---

## Folder Structure

```
bharathanatyam-portfolio/
├── index.html          ← Single page — the only file you edit
├── netlify.toml        ← Netlify config (do not touch)
├── README.md           ← This file
└── images/
    ├── hero/           ← Cover page photo
    │   └── First - cover page option 1 new.jpg   ✅ live
    └── gallery/        ← Gallery photos (slots 1–6)
        └── First - cover page option 1 new.jpg   ✅ slot 1 live
```

---

## How to Update the Site

1. Make changes to `index.html` (or add images to `images/`)
2. Open Git Bash inside the `bharathanatyam-portfolio` folder
3. Run these 3 commands:

```bash
git add .
git commit -m "describe what you changed"
git push
```

Netlify picks up the push automatically — live in ~1 minute.

---

## Page Sections

| # | Section ID | Description |
|---|-----------|-------------|
| 1 | `#cover` | Hero cover photo + name |
| 2 | `#about` | About Me — bio, portrait photo |
| 3 | `#journey` | Dance Journey Timeline |
| 4 | `#guru` | Guru & School |
| 5 | `#performances` | Performances & Achievements |
| 6 | `#videos` | YouTube video slots (4 slots) |
| 7 | `#gallery` | Photo Gallery (6 slots) |
| 8 | `#bharathanatyam` | Meaning of Bharathanatyam |

---

## Change Log

### 2026-04-12
- Deleted nested `Dance-Portfolio/` clone folder (was a duplicate)
- Added `README.md`

### Earlier (session 1)
- Built full single-page portfolio (`index.html`) from scratch
- 7 sections, smooth scroll navigation, scroll-reveal animations
- Google Fonts: Cormorant Garamond + Jost
- Color palette: teal + gold + cream
- YouTube embed system — paste any YouTube URL, no HTML editing needed
- Removed "Book a Performance" section entirely
- Set up GitHub repo (`iampvr84/Dance-Portfolio`) + Netlify auto-deploy
- Hero cover photo wired: `images/hero/First - cover page option 1 new.jpg`
- Gallery slot 1 wired: `images/gallery/First - cover page option 1 new.jpg`
- Cleaned sandbox (deleted old `pages/` folder, stale clones)

---

## Still To Do

- [ ] Upload portrait photo for About Me section
- [ ] Wire portrait photo into `index.html` (About section)
- [ ] Upload gallery photos for slots 2–6
- [ ] Wire gallery slots 2–6 into `index.html`
- [ ] Fill in Guru name & school name
- [ ] Fill in city / location
- [ ] Fill in awards and performance dates
- [ ] Add real YouTube video URLs to 4 video slots
- [ ] Update footer email address
- [ ] Review all `[bracketed]` placeholder text and replace

---

## Adding a New Photo (Permanent)

1. Copy the image file into `images/gallery/` (or `images/hero/` for cover)
2. Open `index.html`, find the gallery slot you want to replace
3. Replace the `<div class="photo-box">...</div>` block with:

```html
<img src="images/gallery/YOUR-FILENAME.jpg"
     alt="Description"
     style="width:100%;height:100%;object-fit:cover;object-position:center top;display:block;" />
```

4. Save, then push with the 3 git commands above.

---

## YouTube Videos (No HTML Editing Needed)

On the live website, go to the **Videos** section.  
Paste any YouTube URL into the input box and click **Embed**.  
Supported formats:
- `https://www.youtube.com/watch?v=XXXX`
- `https://youtu.be/XXXX`
- `https://www.youtube.com/shorts/XXXX`

> Note: These embeds are session-only (not saved permanently).  
> To make a video permanent, ask Claude to hardcode the embed into `index.html`.

---

## Tech Stack

- Plain HTML + CSS + JavaScript (no frameworks, no build tools)
- Google Fonts (Cormorant Garamond, Jost)
- IntersectionObserver for scroll animations
- Netlify hosting (free tier)
- GitHub for version control
