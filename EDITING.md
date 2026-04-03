# Berinba P&C Website — Editing Guide

A quick reference for updating the website content without needing to know HTML.

---

## How to Update the News Ticker

Open `index.html` and find the section that looks like this (around line 30–50):

```html
<span class="ticker-item"><span class="dot"></span>Term 2 Canteen Menu now available...</span>
```

**To add a new item:** Copy one of the existing `<span class="ticker-item">` lines and paste it in. Change the text between `</span>` and the closing `</span>`.

**Important:** The items are duplicated (you'll see them appear twice in the file). Always update **both copies** so the animation loops correctly.

**To remove an item:** Delete the full `<span class="ticker-item">...</span>` line — and its duplicate.

---

## How to Add or Update Events

Open `events.html`. Each event looks like this:

```html
<div class="event-card-full" data-category="community">
  <div class="event-date-box-lg">
    <span class="day">23</span>
    <span class="month">May</span>
    <span class="year">2026</span>
  </div>
  <div class="event-details">
    <h3>School Fun Run 2026 <span class="event-tag tag-community">Community</span></h3>
    <p>Description goes here.</p>
    <div class="event-meta-row">
      <span>🕙 10:00am – 11:30am</span>
      <span>📍 School Oval</span>
    </div>
  </div>
</div>
```

**Categories** — change `data-category` and the `event-tag` class to match:
- `meeting` / `tag-meeting` — blue
- `fundraiser` / `tag-fundraiser` — yellow
- `community` / `tag-community` — green
- `school` / `tag-school` — purple

---

## How to Update Committee Members

Open `committee.html`. Find a committee card and update the name and description:

```html
<div class="committee-card">
  <div class="committee-avatar">👤</div>
  <div class="committee-role">President</div>
  <h3>[President Name]</h3>   ← Change this
  <p>Description text.</p>    ← Change this
</div>
```

Replace `[President Name]` with the actual person's name.

---

## How to Add School Photos

On the home page (`index.html`), find the photo grid section:

```html
<div class="photo-item" title="Add your school photo here">🏫</div>
```

Replace the emoji placeholder with an actual `<img>` tag:

```html
<div class="photo-item">
  <img src="photos/your-photo.jpg" alt="Berinba students at the oval" style="width:100%;height:100%;object-fit:cover;">
</div>
```

Put your photo files in a `photos/` folder inside the website folder.

---

## How to Update Canteen Menu Prices

Open `canteen.html`. Find a menu item:

```html
<div class="menu-item">
  <span class="menu-item-name">Ham & Cheese Roll</span>
  <span class="menu-item-price">$3.50</span>   ← Change this
</div>
```

---

## How to Update Uniform Stock Sizes

Open `uniform.html`. Find a size tag and mark it as out of stock:

```html
<span class="size-tag">12</span>        ← in stock
<span class="size-tag out">14</span>    ← out of stock (strikethrough)
```

Add or remove the word `out` in the class to toggle stock status.

---

## Updating the Footer

The footer appears at the bottom of every page. You'll need to update it in all 5 files:
- `index.html`
- `committee.html`
- `canteen.html`
- `uniform.html`
- `events.html`

Find the `<footer>` section and update the principal name and phone number.

---

## Hosting the Website

This is a static website — no server needed. Options:

1. **GitHub Pages** — Free. Push the folder to a GitHub repo and enable Pages.
2. **Netlify** — Free. Drag and drop the folder at netlify.com.
3. **School server** — Ask the school IT coordinator if there's web hosting available.
4. **Local file** — Open `index.html` in any browser to preview the site.
