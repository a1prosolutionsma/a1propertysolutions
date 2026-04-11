# A1 Property Solutions — Website README

## 📁 File Structure

```
a1-property/
├── index.html        ← Homepage
├── about.html        ← About / Mission / History / Social Media
├── pricing.html      ← Pricing tables + packages + FAQ
├── reviews.html      ← Customer reviews + leave-a-review CTAs
├── contact.html      ← Contact form + social links
├── styles.css        ← Shared styles (colors, nav, footer, buttons)
├── images/           ← Put all your photos here (create this folder)
│   ├── owner.jpg
│   ├── logo.png
│   └── og-home.jpg
└── README.md         ← This file
```

---

## 🚀 Quick Setup Checklist

Search each HTML file for these and fill them in:

| What to edit | What to search for |
|---|---|
| Phone number | `6173026160` |
| Facebook URL | `YOUR_PAGE` |
| Instagram URL | `YOUR_HANDLE` |
| Google Business URL | `YOUR_GOOGLE_BUSINESS` |
| Owner name | `[Your Name Here]` |
| Email address | `info@a1propertysolutions.com` |
| Your domain | `a1propertysolutions.com` |
| Owner bio | Look for `<!-- EDIT: write your own bio -->` |
| Review quotes | Look for `<!-- EDIT: replace with your actual reviews -->` |
| Prices | All pricing tables in `pricing.html` |

---

## 🖼️ How to Add Images to GitHub

### Step 1 — Create an `images` folder
In your GitHub repo, click **Add file → Create new file**, type `images/.gitkeep`, and commit.

### Step 2 — Upload photos
1. Click into the `images/` folder in your repo
2. Click **Add file → Upload files**
3. Drag and drop your photos (JPG or PNG)
4. Click **Commit changes**

### Step 3 — Use the images in your HTML

**Owner photo (about.html):**
Find the `<!-- EDIT: Replace with real photo -->` comment and replace the emoji placeholder div:
```html
<!-- BEFORE -->
<div class="owner-photo">👷</div>

<!-- AFTER -->
<div class="owner-photo">
  <img src="images/owner.jpg" alt="[Your Name] — Owner of A1 Property Solutions">
</div>
```

**About section photo (index.html):**
```html
<!-- BEFORE -->
<div class="about-visual">🏠</div>

<!-- AFTER -->
<div class="about-visual">
  <img src="images/truck-or-job-photo.jpg" alt="A1 Property Solutions team at work in Boston">
</div>
```

**Logo image (optional):**
If you have a logo file, replace the text logo in the nav:
```html
<!-- BEFORE -->
<a href="index.html" class="logo">A1 <span>Property</span> Solutions</a>

<!-- AFTER -->
<a href="index.html" class="logo">
  <img src="images/logo.png" alt="A1 Property Solutions">
</a>
```

---

## 📋 Recommended Photos to Add

| Photo | Where used | Tips |
|---|---|---|
| Owner headshot | `about.html` | Professional, good lighting, outdoors or job site works |
| Team/truck photo | `index.html` | Shows credibility and professionalism |
| Job before/afters | `reviews.html` | Great for trust |
| Logo (PNG, transparent bg) | All pages nav | Keep under 500px wide |
| `og-home.jpg` | Social share preview | 1200×630px ideal |

### 📐 Image Size Tips
- Keep all photos **under 500KB** for fast loading (use [squoosh.app](https://squoosh.app) to compress)
- Hero/OG images: **1200×630px**
- Portrait photos: **600×800px** max
- Always add descriptive `alt=""` text for SEO

---

## 🔧 Setting Up the Contact Form

The form in `contact.html` currently just shows a success message. To make it actually send emails:

### Option A: Formspree (Free, easiest)
1. Go to [formspree.io](https://formspree.io) and sign up
2. Create a new form — get your endpoint URL (looks like `https://formspree.io/f/abcdefgh`)
3. In `contact.html`, find the `<form>` tag and update it:
```html
<form id="contactForm" action="https://formspree.io/f/YOUR_ID" method="POST">
```
4. Remove `e.preventDefault()` from the JavaScript at the bottom of contact.html

### Option B: Netlify Forms (if hosting on Netlify)
Add the `netlify` attribute to your form tag:
```html
<form name="contact" netlify>
```
That's it — Netlify handles the rest.

---

## 🌐 Google Business Profile (Important for SEO!)

This is one of the highest-impact things you can do:
1. Go to [business.google.com](https://business.google.com)
2. Set up or claim your Google Business Profile
3. Add your phone, hours, service area, and photos
4. Once live, get your review link and add it to `reviews.html`

---

## 🗺️ Adding a Real Google Map

In `index.html`, find the `<!-- EDIT: Replace this with a real Google Maps embed -->` comment:
1. Go to [maps.google.com](https://maps.google.com)
2. Search your business name or address
3. Click **Share → Embed a map → Copy HTML**
4. Paste the `<iframe>` tag where the placeholder div is

---

## 🔍 SEO Quick Wins

- Fill in the `og:image` meta tags with real image URLs
- Add your business to [Google Business Profile](https://business.google.com)
- Get listed on [Yelp](https://biz.yelp.com), [Angi](https://www.angi.com), and [Thumbtack](https://www.thumbtack.com)
- Ask every satisfied customer for a Google review
- Add location-specific pages if you serve multiple distinct areas (e.g., `boston-handyman.html`, `cambridge-property-maintenance.html`)

---

## 🎨 Changing Colors

Open `styles.css` and edit the `:root` variables at the top:

```css
:root {
  --navy:       #0d1f3c;   /* Main dark color (nav, footer, headers) */
  --gold:       #e8a020;   /* Accent / CTA color */
  --gold-dark:  #c4861a;   /* Hover state for gold */
  ...
}
```

---

## 📞 Find & Replace Phone Number

To update the phone number across all files at once, search for `6173026160` and replace it with your number (digits only, no formatting — the display formatting is separate in the HTML text).

---

*Site built with plain HTML, CSS, and JavaScript — no frameworks needed. Host on GitHub Pages, Netlify, or any web host.*
