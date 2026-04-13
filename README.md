# How to publish your tick maps to GitHub Pages

This gives you a **free public URL** like `https://yourusername.github.io/tick-maps/`
that anyone can open in a browser. No server needed — GitHub hosts static HTML for free.

---

## Step-by-step (5 minutes)

### 1. Create a GitHub account (skip if you have one)
Go to [github.com/signup](https://github.com/signup) and create a free account.

### 2. Create a new repository
1. Click the **+** icon (top right) → **New repository**
2. Name it something like `tick-maps`
3. Set it to **Public**
4. Check **Add a README file**
5. Click **Create repository**

### 3. Upload your HTML files
1. In your new repo, click **Add file** → **Upload files**
2. Drag in your HTML files:
   - `tickborne_diseases_timeslider.html` → rename to `index.html` (this becomes the homepage)
   - `tick_species_map.html`
3. Click **Commit changes**

### 4. Enable GitHub Pages
1. Go to your repo's **Settings** tab (gear icon)
2. In the left sidebar, click **Pages**
3. Under **Source**, select:
   - Branch: **main**
   - Folder: **/ (root)**
4. Click **Save**
5. Wait 1–2 minutes

### 5. Access your live site
Your maps are now live at:
```
https://yourusername.github.io/tick-maps/
```
- Disease map (index.html): `https://yourusername.github.io/tick-maps/`
- Species map: `https://yourusername.github.io/tick-maps/tick_species_map.html`

Share these URLs anywhere — Google Docs, email, Slack, social media.

---

## Updating the maps later

When CDC releases new data:
1. Re-run the R scripts (they auto-download the latest CDC files)
2. In your GitHub repo, click **Add file** → **Upload files**
3. Upload the new HTML files (same filenames → they overwrite)
4. Click **Commit changes**
5. GitHub Pages updates automatically in ~1 minute

---

## Embedding in Google Docs

Once your GitHub Pages URL is live:
- **Insert → Link**: Paste the URL directly in your document
- **Insert → Image**: Take a screenshot of the map and insert it,
  then add the URL as a hyperlink on the image

---

## Alternative: Netlify (even faster, no account needed)

1. Go to [app.netlify.com/drop](https://app.netlify.com/drop)
2. Put your HTML files in a folder
3. Drag the folder onto the page
4. Instant URL (e.g., `https://cool-tick-map-abc123.netlify.app`)

Note: Without a Netlify account, the URL expires after 1 hour.
With a free account, it's permanent.

---

## File structure for your repo

```
tick-maps/
├── index.html                          ← Disease map with time slider (main page)
├── tick_species_map.html               ← Tick species distribution
├── README.md                           ← This file
├── disease_timeslider.R                ← R code to regenerate disease map
├── species_map.R                       ← R code to regenerate species map
└── AllTBD2022_Public.xlsx              ← CDC source data (optional)
```
