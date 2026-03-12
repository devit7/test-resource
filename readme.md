# ERP Resources

Repositori terpusat untuk **shared assets** yang digunakan oleh semua modul frontend ERP PT Sepanjang Pangan.

## Struktur Folder

```
erp-resources/
├── css/          # Global stylesheets, CSS variables, design tokens
├── fonts/        # Custom fonts (woff2, woff)
├── icons/        # Icon set (SVG, sprite)
└── image/        # Shared images (logo, brand assets, ilustrasi)
```

## Cara Menggunakan di Tiap Modul

Setiap modul frontend memiliki script `update-resources.sh`. Jalankan script tersebut untuk mengambil/memperbarui resources.

```bash
# Clone pertama kali / update ke versi terbaru
./update-resources.sh

# Pakai branch tertentu
./update-resources.sh --branch develop

# Pakai versi/tag tertentu (direkomendasikan untuk production)
./update-resources.sh --tag v1.2.0
```

## Versioning

Gunakan **semantic versioning** untuk merilis versi baru:

| Tag | Kapan digunakan |
|-----|----------------|
| `v1.0.0` | Rilis stabil, breaking changes |
| `v1.1.0` | Penambahan asset baru |
| `v1.0.1` | Perbaikan kecil, hotfix |

```bash
# Cara membuat tag baru
git tag -a v1.1.0 -m "Menambahkan icon set baru untuk modul inventory"
git push origin v1.1.0
```

## Kontribusi

1. Buat branch dari `main`: `git checkout -b feat/tambah-icon-inventory`
2. Tambahkan asset yang diperlukan
3. Buat Pull Request ke `main`
4. Setelah merge, buat tag versi baru

## Modul yang Menggunakan Repo Ini

| Modul | Repository |
|-------|-----------|
| Frontend Playground | `github.com/YOUR_ORG/frontend-playground` |
| Modul Inventory | `github.com/YOUR_ORG/erp-inventory` |
| Modul HR | `github.com/YOUR_ORG/erp-hr` |
| *(tambahkan modul lainnya)* | |
