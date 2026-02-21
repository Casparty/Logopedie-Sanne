# Praktijk Stem & Klank – Static Website

A complete, ready-to-publish static website for a Belgian speech therapy practice.

## 📁 Files

```
/
├── index.html       ← Main HTML file (all pages/sections)
├── style.css        ← All CSS styling
└── README.md        ← This file
```

## 🚀 Hosting on GitHub Pages

### Step 1: Create a GitHub repository
1. Go to [github.com](https://github.com) and sign in (or create an account).
2. Click **New repository**.
3. Name it `stemklank-website` (or any name you prefer).
4. Keep it **Public**.
5. Click **Create repository**.

### Step 2: Upload the files
**Option A – via the GitHub web interface (simplest):**
1. In your new repo, click **Add file → Upload files**.
2. Drag and drop `index.html` and `style.css`.
3. Click **Commit changes**.

**Option B – via Git on your computer:**
```bash
git init
git add index.html style.css README.md
git commit -m "Initial commit: Stem & Klank website"
git branch -M main
git remote add origin https://github.com/YOURUSERNAME/stemklank-website.git
git push -u origin main
```

### Step 3: Enable GitHub Pages
1. In your repository, go to **Settings → Pages**.
2. Under **Source**, select **Deploy from a branch**.
3. Choose branch: `main`, folder: `/ (root)`.
4. Click **Save**.

### Step 4: Access your site
After 1–2 minutes your site will be live at:
```
https://YOURUSERNAME.github.io/stemklank-website/
```

---

## 🖼️ Replacing Image Placeholders

All image placeholders (the grey boxes with emoji) can be replaced with real photos:

1. Add your images to the repository (e.g., `/images/team-lien.jpg`).
2. Replace the `<div class="img-placeholder ...">` blocks in `index.html` with:
```html
<img src="images/team-lien.jpg" alt="Lien De Smedt, logopediste" class="team-photo" />
```
3. Add corresponding CSS in `style.css`:
```css
.team-photo {
  width: 100%;
  aspect-ratio: 3/4;
  object-fit: cover;
  border-radius: 20px 20px 0 0;
}
```

## 🗺️ Adding a Google Maps Embed

Replace the `.map-placeholder` div in the Contact section with:
```html
<iframe
  src="https://www.google.com/maps/embed?pb=YOUR_EMBED_CODE_HERE"
  width="100%"
  height="220"
  style="border:0; border-radius: 12px;"
  allowfullscreen=""
  loading="lazy"
  referrerpolicy="no-referrer-when-downgrade"
  title="Locatie Praktijk Stem & Klank">
</iframe>
```
Get your embed code at: **Google Maps → Share → Embed a map**.

## 📬 Activating the Contact Form

The contact form currently uses `action="#"` (no backend). To make it functional:

**Option A – Formspree (free, no backend needed):**
1. Sign up at [formspree.io](https://formspree.io).
2. Create a new form and get your endpoint URL.
3. Replace `action="#"` with `action="https://formspree.io/f/YOUR_FORM_ID"`.
4. Add `method="post"` (already present).

**Option B – Netlify Forms (if you migrate to Netlify hosting):**
Add `netlify` attribute to the form tag: `<form netlify ...>`.

## ✏️ Customising Content

- **Practice name, address, phone, email**: Search for `Stem & Klank`, `Kerkstraat 12`, `052 12 34 56`, `info@stemklank.be` and replace throughout `index.html`.
- **Therapist names and bios**: Edit the `<article class="team-card">` blocks in the Team section.
- **Colors**: Change CSS variables at the top of `style.css` (`:root { ... }`).
- **Logo**: Replace the `.logo-mark` div with an `<img>` tag pointing to your logo file.

## 📱 Responsive Breakpoints

| Breakpoint | Layout |
|---|---|
| > 960px | Full desktop layout |
| 720–960px | Stacked hero, single-column services |
| < 720px | Mobile nav, vertical steps |
| < 480px | All single-column grids |

## 🔒 Privacy & GDPR

Remember to:
- Add a real **Privacy Policy** page (link already exists in the footer and form).
- Add a **cookie banner** if you use analytics (e.g., Google Analytics).
- Ensure form data is processed in accordance with GDPR.

---

*Built with semantic HTML5, CSS custom properties, and vanilla JavaScript. No frameworks or dependencies required.*
