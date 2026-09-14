# 📚 Catatan Belajar: Version Control, Git, GitHub & Markdown

Rangkuman materi dasar tentang Version Control System (VCS), perintah-perintah Git, cara menghubungkan repository ke GitHub, dan sintaks dasar Markdown.

## Daftar Isi
1. [Version Control & Git](#1-version-control--git)
2. [Dasar-Dasar Perintah Git](#2-dasar-dasar-perintah-git)
3. [GitHub & Remote Repository](#3-github--remote-repository)
4. [Sintaks Dasar Markdown](#4-sintaks-dasar-markdown-md)

---

## 1. Version Control & Git

**Version Control** adalah praktik pelacakan dan pengelolaan perubahan file dari waktu ke waktu.

### Jenis VCS
| Jenis | Contoh |
|---|---|
| VCS Lokal | RCS |
| VCS Terpusat / Client-Server | CVS, Subversion |
| VCS Terdistribusi / Peer-to-Peer | Git, Mercurial |

### Kegunaan Utama Git
- Pelacakan riwayat perubahan (melihat siapa, kapan, dan alasan perubahan).
- Kolaborasi jarak jauh tanpa saling menimpa kode.
- Fitur **Branching** (pencabangan) dan **Merging** (penggabungan).

---

## 2. Dasar-Dasar Perintah Git

### Inisialisasi & Konfigurasi
```bash
git config --global user.name "Nama Anda"
git config --global user.email "email@contoh.com"
git config --global init.defaultBranch main
git init   # Mengubah folder saat ini menjadi repository Git lokal
```

### Status File & Staging Area
Status file di Git terdiri dari: `untracked`, `unmodified`, `modified`, `staged`.

```bash
git status      # Memeriksa status file di repository
git add <file>  # Menambahkan file ke staging area
git add .       # Menambahkan semua file yang berubah
```

`.gitignore` adalah file untuk mencantumkan daftar file/folder yang ingin diabaikan Git.

### Commit & Riwayat
```bash
git commit -m "pesan commit"   # Menyimpan snapshot perubahan dengan pesan khusus
git log                        # Melihat riwayat commit
git log --oneline              # Melihat riwayat commit secara ringkas
```

### Pembatalan (Reset)
```bash
git reset                # Membatalkan penambahan file ke staging area
git reset HEAD~1          # Membatalkan commit terakhir (perubahan file tetap ada)
git reset --hard HEAD~1   # Membatalkan commit terakhir dan menghapus perubahannya
```

---

## 3. GitHub & Remote Repository

**GitHub** adalah platform berbasis web untuk meng-hosting repository Git.

### Menghubungkan Repository Lokal ke GitHub
```bash
git remote add origin <URL_REPOSITORY_GITHUB>
git push -u origin main   # Mem-push commit lokal ke remote GitHub
git clone <URL>           # Mengkloning repository yang ada di GitHub ke lokal
git pull                  # Mendownload dan menggabungkan perubahan dari remote ke branch lokal
```

---

## 4. Sintaks Dasar Markdown (.md)

### Heading / Judul
```markdown
# Judul 1
## Judul 2
### Judul 3
```

### Format Teks
```markdown
**Teks Bold/Tebal**
*Teks Miring/Italic*
~~Teks Dicoret/Strikethrough~~
```

### List / Daftar
```markdown
1. Pertama
2. Kedua

- Baris 1
- Baris 2
```

### Tautan & Gambar
```markdown
[Teks Link](URL)
![Alt Teks](URL_Gambar)
```

### Blok Source Code
````markdown
```html
<h1>Hello World</h1>
```
````
