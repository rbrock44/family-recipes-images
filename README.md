# Family Recipes Images

> This repo's purpose is to hold all of the photos for my family recipes. <br/>
> [LIVE - Family Recipes Website](https://family-recipes.ryan-brock.com/)

---

## 📚 Table of Contents

- [What's My Purpose?](#-whats-my-purpose)
- [Structure](#-structure)
- [How to Add Photos](#-how-to-add-photos)
- [Technologies](#-technologies)
- [Getting Started (Local Setup)](#-getting-started-local-setup)

---

## 🧠 What's My Purpose?

This repo's purpose is to hold all of the photos for my family recipes. Each photo is a scanned/photographed recipe card that backs an entry on the [Family Recipes Website](https://family-recipes.ryan-brock.com/)/[Repo](https://github.com/rbrock44/family-recipes).

---

## 🗂 Structure

- All images live in [`recipes/`](./recipes).
- Each image is named with a 4-digit, zero-padded recipe number: `NNNN.jpg` (e.g. `0925.jpg`).
- That number ties the image to its matching recipe entry, `src/assets/recipes/NNNN.json`, in the [family-recipes](https://github.com/rbrock44/family-recipes) app repo.
- The app links to photos here via raw GitHub URLs, e.g.
  `https://raw.githubusercontent.com/rbrock44/family-recipes-images/master/recipes/0925.jpg`

There are no processing scripts in this repo — it's just image storage.

---

## 🚦 How to Add Photos

Recipe photos are processed on the app side, not here:

1. In the [family-recipes](https://github.com/rbrock44/family-recipes) repo, run its `recipes:from-images` script against a folder of photos:
   - `npm run recipes:from-images -- --folder ./photos --author "Ryan Brock"`
   - This reads each photo with Claude, writes the matching `NNNN.json` into that repo's `src/assets/recipes/`, and stages a cropped/aligned copy of each photo as `<folder>/processed/NNNN.jpg`.
2. Copy the staged images from `<folder>/processed/` into [`recipes/`](./recipes) in this repo.
3. Commit and push both repos (the recipe JSON in `family-recipes`, the photo here) so the links resolve.

---

## 🛠 Technologies

- Just plain image storage — no build tooling lives in this repo.

---

## 🚀 Getting Started (Local Setup)

- Clone [repo](https://github.com/rbrock44/family-recipes-images)
- Drop new recipe photos into `recipes/` following the `NNNN.jpg` naming above

---
