# helmyfikrih.github.io

Source code blog & online profile berbasis **Hexo**.

---

## 🚀 Alur Kerja / Deploy Otomatis (CI/CD)

Project ini sudah dilengkapi **GitHub Actions**. Kamu **tidak perlu build manual** di local.

Cukup edit/tambah konten markdown di branch **`main`**, lalu **push ke GitHub**. GitHub Actions akan otomatis melakukan:
1. Build Hexo (`hexo generate`)
2. Deploy hasil static HTML ke branch `gh-pages`

---

## 📝 Cara Tambah / Edit Portfolio

### 1. Tambah Post Baru
Buat file markdown baru di folder `source/_posts/nama-project.md`:

```markdown
---
title: Judul Project
date: 2026-08-28 12:00:00
categories:
  - WEB-APP
tags:
  - React
  - Node.js
cover: https://link-gambar-thumbnail.jpg
---

Deskripsi detail project, tantangan, dan teknologi yang digunakan.
```

### 2. Simpan dan Push ke GitHub
```bash
git add .
git commit -m "Add portfolio: Judul Project"
git push origin main
```
Dalam 1-2 menit, website di `https://helmyfikrih.github.io` otomatis terupdate.

---

## 💻 Menjalankan di Lokal (Opsional / Preview)

Jika ingin melihat tampilan sebelum push:

```bash
# Pastikan Node.js v18 terpasang
npm install

# Jalankan local server
npx hexo server
```
Buka di browser: `http://localhost:4000`

