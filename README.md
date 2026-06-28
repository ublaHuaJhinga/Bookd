# Bookd

Basically, serializd for math and physics textbooks. I find it incredibly overwhelming to finish a complete book in one go and have concluded that assuming parts of books as seasons of a show helps tremendously by reducing your goals from something that feels unsurmountable.

---

## Overview

Bookd is a single-page web app designed for:

- Tracking **technical books** (math / physics / similar)
- Breaking books into **explicit blocks**
- Logging progress incrementally rather than per-book
- Keeping a lightweight **reading diary**

No frameworks, no build tools, no backend required (optional cloud sync available).

---

## Features

- Block-based tracking
- Progress visualization
- Reading diary (ratings + notes)
- Editable block structure
- Local-first usage
- Optional JSONBin sync

---

## Project Structure

Single file:

```
bookd.html
```

Contains HTML, CSS, and JavaScript.

---

## Usage

### Run locally

Open `bookd.html` in any browser.

### Add books

Edit:

```js
const BOOKS = [...]
```

Each entry:

```js
{
  id: 'example-id',
  title: 'Book Title',
  author: 'Author',
  subject: 'Category',
  level: 1,
  blocks: [
    { id: 'b1', label: 'Ch. 1–3', title: 'Topic' }
  ]
}
```

---

## Optional Sync (JSONBin)

1. Create account at https://jsonbin.io
2. Create API key
3. Create a bin with:

```json
{ "logs": {} }
```

4. Enter API key and Bin ID in settings

---

## Design Notes

- Single source of truth: `BOOKS`
- State: `logs`
- Data-driven rendering

---

## Limitations

- No persistence without JSONBin
- No search/filter
- Manual book maintenance
