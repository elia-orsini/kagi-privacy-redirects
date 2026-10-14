# Kagi Privacy Redirects

A collection of custom redirect rules for [Kagi Search](https://kagi.com) that replace popular websites with privacy‑friendly alternative frontends that bypass tracking, remove ads and paywalls.

These rules only affect **search result clicks** inside Kagi, not manually typed URLs.

## 🔧 How to Add the Rules

1. Go to Kagi Search **Settings** → **Search**/**Advanced** → **Open Redirects**.
2. Paste any rule you want and save.

## 📑 Index

- [Medium](#1-medium--scribe)
- [Reddit](#2-reddit--redlib)
- [YouTube](#3-youtube--invidious)
- [Wikipedia](#4-wikipedia--wikiless)
- [NYTimes](#5-nytimes--archivetoday)
- [New Yorker](#6-new-yorker--archivetoday)
- [Washington Post](#7-washington-post--archivetoday)
- [Twitter (deprecated)](#8-twitter--nitter-deprecated)

## 📜 Redirect Rules

### 1. Medium → Scribe

- **Original domain:** `medium.com`
- **Redirects to:** `scribe.rawbit.ninja`
- **Service:** [Scribe](https://scribe.rawbit.ninja) – ad‑free, paywall‑free Medium reader
- **Rule:**
```text
^https?://(?:www\.)?medium\.com|https://scribe.rawbit.ninja
```

---

### 2. Reddit → Redlib

- **Original domain:** `reddit.com`
- **Redirects to:** `redlib.catsarch.com`
- **Service:** [Redlib](https://redlib.catsarch.com) – private, no‑tracking Reddit frontend
- **Rule:**
```text
^https?://(?:www\.)?reddit\.com|https://redlib.catsarch.com
```

---

### 3. YouTube → Invidious

- **Original domain:** `youtube.com` (any path, e.g. `/watch?v=...`)
- **Redirects to:** `invidious.nerdvpn.de` (same path)
- **Service:** [Invidious](https://invidious.nerdvpn.de) – alternative YouTube frontend without tracking
- **Rule:**
```text
^https?://(?:www\.)?youtube\.com|https://invidious.nerdvpn.de
```

---

### 4. Wikipedia → Wikiless

- **Original domain:** `wikipedia.org` (any language subdomain)
- **Redirects to:** `wikiless.tiekoetter.com`
- **Service:** [Wikiless](https://wikiless.tiekoetter.com) – privacy‑focused Wikipedia frontend
- **Rule:**
```text
^https?://(?:[\w-]+\.)*wikipedia\.org|wikiless.tiekoetter.com
```

---

### 5. NYTimes → Archive.today

- **Original domain:** `nytimes.com`
- **Redirects to:** `archive.ph` snapshot of the same article
- **Service:** [Archive.today](https://archive.ph) – cached copy, bypasses full paywall
- **Rule:**
```text
^https?://(?:www\.)?nytimes\.com/(.*)$|https://archive.ph/https://nytimes.com/$1
```

---

### 6. New Yorker → Archive.today

- **Original domain:** `newyorker.com`
- **Redirects to:** `archive.ph` snapshot of the same article
- **Service:** [Archive.today](https://archive.ph) – cached copy, bypasses full paywall
- **Rule:**
```text
^https?://(?:www\.)?newyorker\.com/(.*)$|https://archive.ph/https://www.newyorker.com/$1
```

---

### 7. Washington Post → Archive.today

- **Original domain:** `washingtonpost.com`
- **Redirects to:** `archive.ph` snapshot of the same article
- **Service:** [Archive.today](https://archive.ph) – cached copy, bypasses full paywall
- **Rule:**
```text
^https?://(?:www\.)?washingtonpost\.com/(.*)$|https://archive.ph/https://www.washingtonpost.com/$1
```

---

### 8. Twitter → Nitter (deprecated)

> **Deprecated:** Nitter instances are largely unreliable or offline. Kept for reference only.

- **Original domain:** `x.com`
- **Redirects to:** `nitter.net`
- **Service:** [Nitter](https://nitter.net) – lightweight, privacy‑focused Twitter frontend
- **Rule:**
```text
^https?://(?:www\.)?x\.com|https://nitter.net
```
