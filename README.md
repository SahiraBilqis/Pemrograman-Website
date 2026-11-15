
# Pemrograman Web

## 1. Teknologi yang Digunakan

| Tugas | Teknologi |
|---|---|
| Tugas 2 | Node.js, Express.js, PostgreSQL, Neon, Prisma ORM |
| Tugas 3 | React, Vite, JavaScript, JSX, CSS |
| Pengujian | Postman, Hoppscotch, Prisma Studio |
| Version Control | Git dan GitHub |

## 2. Struktur Folder

```text
pemweb-expressjs-prisma/
├── tugas-2/
│   ├── controllers/
│   ├── prisma/
│   │   ├── migrations/
│   │   └── schema.prisma
│   ├── routes/
│   ├── screenshots/
│   ├── app.js
│   ├── seed.js
│   ├── package.json
│   └── package-lock.json
├── tugas-3-react/
│   ├── public/
│   ├── src/
│   │   ├── App.jsx
│   │   ├── App.css
│   │   ├── index.css
│   │   └── main.jsx
│   ├── index.html
│   ├── package.json
│   └── vite.config.js
└── README.md
```

## 3. Tugas 2 — Express.js dan Prisma ORM

Tugas 2 mengimplementasikan REST API Manajemen Produk menggunakan Express.js dan PostgreSQL melalui Prisma ORM.

Fitur:
- GET: Menampilkan daftar dan detail produk.
- POST: Menambahkan produk.
- PUT: Memperbarui produk.
- DELETE: Menghapus produk.
- Validasi input dan error handling.
- Integrasi PostgreSQL Neon dan Prisma Studio.

### Cara Menjalankan

```bash
git clone https://github.com/SahiraBilqis/pemweb-expressjs-prisma.git
cd pemweb-expressjs-prisma/tugas-2
npm install
```

Buat file `.env` berisi `DATABASE_URL` PostgreSQL Neon dan `PORT=3000`. Jangan mengunggah file `.env` ke GitHub.

```bash
npx prisma generate
npx prisma migrate deploy
node app.js
```

Server: `http://localhost:3000`

### Dokumentasi Pengujian Tugas 2

#### Week 9 — Express.js

**GET seluruh produk — 200 OK**

![GET Produk](tugas-2/screenshots/Screenshot%202026-11-01%20095930.png)

**GET produk berdasarkan ID — 200 OK**

![GET ID](tugas-2/screenshots/Screenshot%202026-11-01%20100007.png)

**GET produk tidak ditemukan — 404 Not Found**

![GET 404](tugas-2/screenshots/Screenshot%202026-11-01%20100033.png)

**POST produk baru — 201 Created**

![POST Request](tugas-2/screenshots/Screenshot%202026-11-01%20100121.png)

![POST Response](tugas-2/screenshots/Screenshot%202026-11-01%20100140.png)

#### Week 10 — PostgreSQL dan Prisma ORM

**Kondisi awal database (Before)**

![Database Before](tugas-2/screenshots/Screenshot%202026-11-06%20165241.png)

**PUT tanpa ID — 400 Bad Request**

![PUT Missing ID](tugas-2/screenshots/Screenshot%202026-11-06%20165327.png)

**PUT data tidak valid — 400 Bad Request**

![PUT Invalid](tugas-2/screenshots/Screenshot%202026-11-06%20165509.png)

**PUT berhasil — 200 OK**

![PUT Success](tugas-2/screenshots/Screenshot%202026-11-06%20165626.png)

**Database setelah update (After PUT)**

![After PUT](tugas-2/screenshots/Screenshot%202026-11-06%20165637.png)

**DELETE berhasil — 200 OK**

![DELETE Success](tugas-2/screenshots/Screenshot%202026-11-06%20165702.png)

**Database setelah penghapusan (After DELETE)**

![After DELETE](tugas-2/screenshots/Screenshot%202026-11-06%20165712.png)

---

## 4. Tugas 3 — Fundamental React

Tugas 3 mengimplementasikan aplikasi Manajemen Produk menggunakan React dan Vite sesuai materi Fundamental React.

Fitur:
- Menampilkan lima produk awal.
- Pencarian produk berdasarkan nama.
- Pop-up Tambah Produk.
- Pop-up Edit Produk.
- Pop-up konfirmasi Hapus Produk.
- Validasi nama dan harga.
- Pengelolaan tampilan menggunakan `useState`, JSX, event handler, dan conditional rendering.

### Cara Menjalankan

Dari direktori utama repository:

```bash
cd tugas-3-react
npm install
npm run dev
```

Aplikasi: `http://localhost:5173`

Data produk menggunakan React state sehingga perubahan tidak tersimpan secara permanen setelah refresh.

### Dokumentasi Pengujian Tugas 3

| Skenario | Hasil yang Diharapkan | Hasil Aktual |
|---|---|---|
| Membuka halaman utama | 5 produk ditampilkan | Sesuai |
| Mencari produk | Produk difilter sesuai nama | Sesuai |
| Menambah produk | Produk baru muncul | Sesuai |
| Mengedit produk | Data produk berubah | Sesuai |
| Menghapus produk | Produk terhapus setelah konfirmasi | Sesuai |
| Validasi form | Input tidak valid ditolak | Sesuai |

### Screenshot Pengujian

Tambahkan screenshot hasil pengujian React ke folder `tugas-3-react/screenshots/` agar dokumentasi dapat ditampilkan langsung di GitHub.

---

## 5. Pull Request dan Pengumpulan

Pengerjaan menggunakan Git dan GitHub dengan branch khusus untuk setiap perubahan.

| Pull Request | Keterangan |
|---|---|
| [PR #1 — Tugas 3](https://github.com/SahiraBilqis/pemweb-expressjs-prisma/pull/1) | Implementasi Manajemen Produk React |
