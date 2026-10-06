# Chandana Bollimpalli — Portfolio

One self-contained file: `index.html`. CSS, JavaScript, and the profile photo are all inlined, so there's nothing else to copy or link.

## Run locally
Double-click `index.html`, or serve it (e.g. `python3 -m http.server`) and open it at `localhost`.

## Add it to a live GitHub Pages site
1. Copy `index.html` into your repo — at the repo root if this is the whole site, or into a subfolder (e.g. `/portfolio`) if it's joining an existing site.
2. Commit and push.
3. If it's at the repo root and GitHub Pages is already enabled on that repo, it goes live at your existing Pages URL automatically. If it's in a subfolder, it's reachable at `<your-pages-url>/portfolio/`.

## What's in it
- **Home** — profile hero with photo, headline, and quick-skim tags.
- **Experience** — expandable "now streaming" cards for Palo Alto Networks and CyberArk.
- **Projects** — two cards that link out to their GitHub repos in a new tab:
  - Advanced SIEM & Threat Detection Lab → github.com/sbollimp/Advanced-SIEM-Threat-Detection-Lab
  - Open-Source SIEM with SOAR Automation → github.com/sbollimp/Open-Source-SIEM-with-SOAR-Automation
- **Education** — Kennesaw State University, M.S. Information Technology.
- **Skills** — tool chips grouped by category.
- **Contact** — email and phone with one-click copy.

## Motion
Scroll-reveal fade/slide-ins, a staggered hero entrance, a slow pan on the photo, hover lift on job/project cards, and an animated nav underline. Everything is gated behind `prefers-reduced-motion` and degrades gracefully with JavaScript off (nothing stays permanently hidden).

## What's editable
Open `index.html` in any text editor — it's plain HTML/CSS/JS top to bottom:
- Copy and resume content: in the HTML markup, inside each `<section>`.
- Colors, type, spacing, motion timings: the `<style>` block near the top — tokens are set once under `:root`.
- Nav scroll-spy, mobile menu, scroll-reveal, copy-to-clipboard: the `<script>` block near the bottom.
- Photo: find `<img ... src="data:image/jpeg;base64,...">` in the Home section and replace the `src` with a new image (either a new base64 data URI, or swap it for a relative path like `src="photo.jpg"` if you'd rather keep the image as a separate file).
- Project links: the two repo URLs are the `href` on each `<a class="project-card">` in the Projects section.

## Also available
A split version (`index.html` + `style.css` + `script.js` + `assets/chandana.jpg` as separate files) is available if you'd rather edit styles/scripts/image independently — just ask.
