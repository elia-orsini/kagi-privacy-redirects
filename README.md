# Kagi Privacy Redirects

A collection of custom redirect rules for [Kagi Search](https://kagi.com) that replace popular websites with privacy‑friendly alternative frontends that bypass tracking, remove ads and paywalls.

These rules only affect **search result clicks** inside Kagi, not manually typed URLs.

## 🔧 How to Add the Rules

1. Go to Kagi Search **Settings** → **Search**/**Advanced** → **Open Redirects**.
2. Paste any rule you want and save.

## 📑 Index

- [Twitter](#1-twitter--nitter)
- [Medium](#2-medium--scribe)
- [Reddit](#3-reddit--redlib)
- [YouTube](#4-youtube--invidious)
- [NYTimes](#5-nytimes--archivetoday)
- [New Yorker](#6-new-yorker--archivetoday)
- [Washington Post](#6-washington-post--archivetoday)

## 📜 Redirect Rules

### 1. Twitter → Nitter

- **Original domain:** `x.com`
- **Redirects to:** `nitter.net`
- **Service:** [Nitter](https://nitter.net) – lightweight, privacy‑focused Twitter frontend
- **Rule:**
```text
^https?://(?:www\.)?x\.com|https://nitter.net
```

---

### 2. Medium → Scribe

- **Original domain:** `medium.com`
- **Redirects to:** `scribe.rawbit.ninja`
- **Service:** [Scribe](https://scribe.rawbit.ninja) – ad‑free, paywall‑free Medium reader
- **Rule:**
```text
^https?://(?:www\.)?medium\.com|https://scribe.rawbit.ninja
```

---

### 3. Reddit → Redlib

- **Original domain:** `reddit.com`
- **Redirects to:** `redlib.catsarch.com`
- **Service:** [Redlib](https://redlib.catsarch.com) – private, no‑tracking Reddit frontend
- **Rule:**
```text
^https?://(?:www\.)?reddit\.com|https://redlib.catsarch.com
```

---

### 4. YouTube → Invidious

- **Original domain:** `youtube.com` (any path, e.g. `/watch?v=...`)
- **Redirects to:** `invidious.nerdvpn.de` (same path)
- **Service:** [Invidious](https://invidious.nerdvpn.de) – alternative YouTube frontend without tracking
- **Rule:**
```text
^https?://(?:www\.)?youtube\.com|https://invidious.nerdvpn.de
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

### 6. Washington Post → Archive.today

- **Original domain:** `washingtonpost.com`
- **Redirects to:** `archive.ph` snapshot of the same article
- **Service:** [Archive.today](https://archive.ph) – cached copy, bypasses full paywall
- **Rule:**
```text
^https?://(?:www\.)?washingtonpost\.com/(.*)$|https://archive.ph/https://www.washingtonpost.com/$1
```
