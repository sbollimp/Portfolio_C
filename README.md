# Portfolio — Siri Chandana Bollimpalli

A single-page, self-contained portfolio website. Your photo is embedded directly in the HTML,
so the only two files you need to publish are `index.html` and your resume PDF.

## Files

| File | Purpose |
|---|---|
| `index.html` | The entire website (HTML + CSS + JS + your photo, all in one file) |
| `Siri_Chandana_Bollimpalli_Resume.pdf` | Powers the two "Download Resume" buttons |

Both files must sit in the **same folder** and the PDF filename must stay exactly as-is,
or the download buttons will 404.

---

## Publish on GitHub Pages (about 5 minutes)

Your site will end up at **https://sbollimp.github.io/Portfolio/**

1. Go to <https://github.com/new> (signed in as `sbollimp`).
2. Repository name: `Portfolio`. Set it to **Public**. Click **Create repository**.
3. On the new empty repo page, click **uploading an existing file**.
4. Drag in both `index.html` and `Siri_Chandana_Bollimpalli_Resume.pdf`.
5. Click **Commit changes**.
6. Go to **Settings** → **Pages** (left sidebar).
7. Under *Build and deployment* → *Source*, choose **Deploy from a branch**.
   Set branch to **main** and folder to **/ (root)**. Click **Save**.
8. Wait 1–2 minutes, refresh the Pages settings screen, and your live URL appears at the top.

### Want the shorter URL `https://sbollimp.github.io/` instead?

Name the repository **`sbollimp.github.io`** at step 2 instead of `Portfolio`.
Everything else is identical.

---

## Editing the site later

Open `index.html` in any text editor. Everything is plain HTML — no build step, no dependencies.

- **Add a job** — copy one whole `<article class="exp">…</article>` block in the Experience
  section and change the text. The two-letter badge is the `<span class="exp-mark">` value.
- **Point a project card at a repo** — find the card's `<a class="proj …" href="…">`. Change two things:
  1. the `href="https://github.com/sbollimp/…"` — where the click goes
  2. the `<span>sbollimp/…</span>` inside `.proj-repo` — the repo name shown at the bottom of the card

  Keep those two in sync or the card will display one repo and open another.
- **Add or remove a project** — copy or delete a whole `<a class="proj reveal">…</a>` block.
- **Add a skill** — add a `<span class="chip">Name</span>` inside the relevant `.chips` row.
- **Change the accent colour** — edit `--red:#e50914;` near the very top of the `<style>` block.
  Everything red on the page follows that one variable.
- **Swap the photo** — replace the giant `data:image/jpeg;base64,…` string in the hero `<img src="…">`.
  Easier alternative: put `profile.jpg` in the repo and change that `src` to `profile.jpg`.

After editing, commit the file back to GitHub — the live site updates within a minute.

---

## Things worth updating before you share it

- **Education dates** — your resume lists the Kennesaw State MS without a graduation year.
  Add it in the Education section for recruiter credibility.
- **Project repo links** — all five cards point at real repos. For reference:

  | Card | Links to |
  |---|---|
  | Clinical Document NLP Pipeline (featured) | `sbollimp/Clinical-NLP-Pipeline` |
  | Fraud & Anomaly Detection (featured) | `sbollimp/Fraud-Detection-Model_Zool` |
  | E-commerce Recommendation Engine (featured) | `sbollimp/E-Commerce-Recommendation-Engine` |
  | Demand Forecasting Benchmark | `sbollimp/Time-Series-Demand-Forecasting` |
  | MLOps Experiment Platform | `sbollimp/MLOps-Experiment-Platform` |

- **`Time-Series-Demand-Forecasting` root README** — the file at the repo root is the `data/` directory
  README, not the project README. Anyone landing on that repo sees a column schema instead of what the
  project does or how it performs. Move the real README to the root; it's the weakest of the five links
  purely because of this.
- **Email** — the site currently shows `chandanachowdary31@gmail.com`, but your resume PDF lists
  `siribollimpalli31@gmail.com`. Pick one and make both match.
- **Custom domain** (optional) — buy e.g. `siribollimpalli.com`, then in Settings → Pages →
  Custom domain, enter it and add the DNS records GitHub shows you.
