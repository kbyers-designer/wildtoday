# Wild Today — Daily Conservation Briefing

### briefing.wild-tomorrow.com

This is the GitHub Pages site for **Wild Today**, the daily conservation briefing from WildTomorrow by Katie Byers.

-----

## How to Update the Briefing Each Day

You only ever edit one file: **`index.html`**

Open it in any text editor (Notepad on Windows, TextEdit on Mac, or directly on GitHub). Here’s what to change:

-----

### 1. Update the Date and Story Count

Find this line near the top (it’s right below the masthead):

```html
<div class="date-banner-date">Tuesday, May 12, 2026</div>
<div class="date-banner-tag">8 stories today &nbsp;·&nbsp; By Katie Byers</div>
```

Change the date and the number of stories to match today.

-----

### 2. Replace the Story Text

Each story looks like this:

```html
<article class="story">
  <div class="story-number">1</div>
  <div class="story-body">
    <div class="story-tag">Oceans & International Law</div>
    <p class="story-text">Your story text goes here. Use <strong>bold text</strong> to highlight key names or facts.</p>
  </div>
</article>
```

- Change the **topic tag** (e.g. “Oceans & International Law”) to match your story.
- Replace the text inside `<p class="story-text">` with your new story.
- Use `<strong>word or phrase</strong>` around anything you want bolded.
- The numbers (1 through 8) are automatic — just leave them as-is.

-----

### 3. Add or Remove Stories

**To add a story:** Copy one full `<article class="story">` block (from `<article` to `</article>`) and paste it after the last one. Update the number and text.

**To remove a story:** Delete a full `<article class="story">` block and update the remaining numbers.

-----

### 4. Update the Archive

At the bottom of the file, find the archive section. It looks like this:

```html
<a class="archive-item" href="#">
  <div class="archive-item-date">May 12, 2026</div>
  <div class="archive-item-count">8</div>
  <div class="archive-item-label">stories · Current edition</div>
</a>
```

Each day, **add yesterday’s entry** by copying that block and pasting it below. Change the date and story count. Eventually you’ll link each one to a saved copy of that day’s page (see “Saving Past Editions” below).

Remove `· Current edition` from old entries.

-----

### 5. Update the Closing Note (Optional)

Near the bottom of the stories section you’ll find:

```html
<div class="closing-note">
  If you'd like a deeper dive...
</div>
```

You can leave this as-is every day or personalize it when relevant.

-----

## Saving Past Editions

To keep a real archive of each day’s briefing:

1. After you finish updating, **save a copy** of `index.html` and rename it with the date, like `2026-05-12.html`
1. Upload that file to GitHub alongside `index.html`
1. In the archive section, update the `href="#"` on that day’s entry to point to the saved file, like `href="2026-05-12.html"`

Visitors can then click any past date and read exactly what was published that day.

-----

## How to Upload Changes to GitHub

### Option A: Edit directly on GitHub (easiest)

1. Go to your repository on github.com
1. Click `index.html`
1. Click the pencil icon (Edit)
1. Make your changes
1. Scroll down and click **Commit changes**
1. The site updates in about 60 seconds

### Option B: Upload a new file

1. Go to your repository on github.com
1. Click **Add file → Upload files**
1. Drag your updated `index.html` onto the page
1. Click **Commit changes**

-----

## One-Time Setup: Connecting briefing.wild-tomorrow.com

Do this once and you never have to touch it again.

### Step 1: GitHub Pages

1. Go to your repository → **Settings → Pages**
1. Under “Source,” select `main` branch and `/ (root)` folder
1. Click Save
1. Under “Custom domain,” type `briefing.wild-tomorrow.com`
1. Click Save
1. Check “Enforce HTTPS” once it appears

### Step 2: Cloudflare DNS

1. Log into Cloudflare → your wild-tomorrow.com zone
1. Go to **DNS → Add Record**
1. Type: `CNAME`
1. Name: `briefing`
1. Target: `YOURGITHUBUSERNAME.github.io` (replace with your actual GitHub username)
1. Proxy status: **DNS only** (gray cloud, not orange) — GitHub Pages requires this
1. Click Save

Within a few minutes (sometimes up to an hour), `briefing.wild-tomorrow.com` will be live.

-----

## File Structure

```
/
├── index.html       ← The main page. Edit this every day.
├── README.md        ← This file. Instructions.
└── 2026-05-12.html  ← Example archived edition (add these over time)
```

-----

## Questions or Problems?

If something breaks or looks wrong, the safest fix is to re-download the last working version of `index.html` from GitHub’s commit history. Go to the file → click **History** → click any previous commit → click **Raw** → save that version.

-----

*Wild Today is part of WildTomorrow by Katie Byers. wildtomorrow.substack.com*
