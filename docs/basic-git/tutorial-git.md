---
sidebar_position: 1
---

# Dasar-Dasar Git

Git adalah sistem kontrol versi terdistribusi yang digunakan untuk melacak perubahan dalam kode sumber selama pengembangan perangkat lunak. Git memungkinkan beberapa pengembang bekerja secara bersamaan, melacak perubahan, dan berkolaborasi dengan lebih efektif.

## Instalasi Git

### Windows

Install dengan pengaturan default

Buka Git Bash untuk mulai menggunakan Git

### macOS

```
brew install git
```

### Linux (Debian/Ubuntu)

```
sudo apt update
sudo apt install git
```

Cek apakah Git sudah terinstall dengan menjalankan:

```
git --version
```

## Konfigurasi Awal Git

Sebelum mulai menggunakan Git, lakukan konfigurasi user agar semua commit yang dibuat memiliki identitas yang benar.

```
git config --global user.name "Nama Anda"
git config --global user.email "email@example.com"
```

Untuk melihat konfigurasi yang sudah diatur:

```
git config --list
```

### Perintah Dasar Git

Berikut adalah perintah dasar Git yang sering digunakan:

1.  Inisialisasi Repository

Membuat repository baru di dalam folder proyek.

```
git init
```

2.  Menambahkan File ke Staging Area

Menambahkan file ke staging area sebelum melakukan commit.

```
git add namafile
```

Atau untuk menambahkan semua file yang berubah:

```
git add .
```

3.  Commit Perubahan

Menyimpan perubahan ke dalam repository dengan pesan deskriptif.

```
git commit -m "Pesan commit"
```

4.  Melihat Status Repository

Melihat perubahan yang belum dikomit.

```
git status
```

5.  Melihat Riwayat Commit

Menampilkan daftar commit yang telah dilakukan.

```
git log
```

🔹 Menghubungkan ke Repository Remote

Untuk menghubungkan proyek ke repository di GitHub.

1.  Tambahkan Repository Remote

```
git remote add origin https://github.com/username/repository.git
```

2.  Mengunggah Perubahan ke Remote Repository

```
git push -u origin main
```

3.  Mengambil Perubahan dari Remote Repository

```
git pull origin main
```

🔹 Branching dan Merging

Branch digunakan untuk bekerja pada fitur baru tanpa mengganggu kode utama.

1.  Membuat Branch Baru

```
git branch nama-branch
```

2.  Berpindah ke Branch Lain

```
git checkout nama-branch
```

Atau dengan perintah lebih baru:

```
git switch nama-branch
```

3.  Menggabungkan Branch ke Main

```
git checkout main
git merge nama-branch
```

4.  Menghapus Branch

```
git branch -d nama-branch
```

🔹 Cloning Repository

Mengunduh repository dari remote ke lokal.

```
git clone https://github.com/username/repository.git
```

🔹 Git Ignore

Agar Git mengabaikan file tertentu, gunakan file .gitignore.

```
/node_modules
.env
*.log
```

🔹 Reset dan Revert

1.  Membatalkan Perubahan yang Belum Dikomit

```
git checkout -- namafile
```

2.  Menghapus Perubahan dari Staging Area

```
git reset namafile
```

3.  Menghapus Commit Terakhir

```
git reset --soft HEAD~1
```

4.  Membatalkan Commit Tanpa Menghapus Perubahan

```
git revert HEAD
```

Git adalah alat yang sangat berguna untuk pengembangan perangkat lunak dan kolaborasi. Dengan memahami perintah dasar ini, Anda bisa mulai menggunakan Git untuk mengelola proyek dengan lebih baik.
