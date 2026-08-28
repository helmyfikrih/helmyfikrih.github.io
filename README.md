# helmyfikrih.github.io

Source blog & portfolio pribadi berbasis **Hexo**.

---

## Struktur Branch

- **`develop`** (atau `main`): Tempat source code Markdown, konfigurasi, dan assets.
- **`gh-pages`**: Tempat file static HTML hasil build (`hexo generate`) yang di-host langsung oleh GitHub Pages.

> **Catatan Penting:** Semua postingan portofolio dan tulisan Anda yang lengkap ada di branch **`develop`**. Kerjakan update di branch tersebut.

---

## Cara Menambah / Update Portfolio

### 1. Masuk ke Branch Kerja
```bash
git checkout develop
git pull origin develop
```

### 2. Buat File Post / Portofolio Baru

Buat file baru di folder `source/_posts/nama-project.md` atau gunakan command:
```bash
npx hexo new post "Nama Project"
```

Format Front-Matter di bagian atas file:
```markdown
---
title: Nama Project / Portfolio
date: 2026-08-28 10:00:00
categories:
  - WEB-APP
tags:
  - React
  - Node.js
cover: https://link-gambar-cover.jpg
---

Tulis deskripsi, tech stack, screenshot, dan link project di sini.
```

---

## Cara Menjalankan & Preview Lokal

1. Install dependensi (jika belum):
   ```bash
   npm install
   ```
2. Jalankan server lokal:
   ```bash
   npm run server
   ```
   Buka browser: `http://localhost:4000`

---

## Cara Build & Deploy ke GitHub Pages

Hexo sudah dikonfigurasi untuk langsung build dan push ke branch `gh-pages`:

```bash
# 1. Bersihkan build lama
npm run clean

# 2. Generate file statis & deploy langsung ke branch gh-pages
npm run deploy
```

> **Catatan:** `npm run deploy` akan menjalankan `hexo generate --deploy` yang otomatis mengupdate branch `gh-pages` di GitHub.

---

## Simpan Source Code

Setelah deploy, jangan lupa simpan perubahan markdown ke branch repo:
```bash
git add .
git commit -m "Add portfolio: Nama Project"
git push origin develop
```
