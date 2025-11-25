# PROJECT-1---MANAJEMEN-FILE-SERVER---MELINDA

# LANGKAH 1 BUAT STRUKTUR

# Masuk ke Direktori Home :
[Deskripsi gambar] (https://drive.google.com/file/d/1MbWZ_KZWqIGG9xw6thTVrw4gVjQ7OJ6A/view?usp=sharing)

~~~
cd
~~~

# Membuat Seluruh Struktur Folder :
[Deskripsi gambar] (https://drive.google.com/file/d/18dkp0P9LqVvXph2LGJAyTBNNB2fGrESa/view?usp=sharing) 

~~~
mkdir -p ~/Project_1/{Marketing,Engineering,HR}/{Documents,Archives}
~~~

Penjelasan : ini adalah cara untuk membuat seluruh struktur folder Project_1 dengan satu perintah saja. Struktur foldernya terdiri dari tiga folder besar yaitu Marketing, Engineering, dan HR, dan masing-masing memiliki subfolder Documents dan Archives.

# Masuk ke Direktori Project_1 :
[Deskripsi gambar] (https://drive.google.com/file/d/1qeXctf0LSeNAz9QnSoO1xKdYlCYozV05/view?usp=sharing)

~~~
cd Project_1
~~~

# Melihat ISI Setiap Folder/File :
[Deskripsi gambar] (https://drive.google.com/file/d/1xm5v78NlN_PMte-xHPPq6HLhPPyucAqS/view?usp=sharing)

~~~
ls
~~~

~~~
ls Marketing
~~~

~~~
ls Engineering
~~~

~~~
ls HR
~~~

Penjelasan :
- ls = Melihat isi Folder
- ls Marketing = Melihat isi file yang ada pada folder Marketing
- ls Engineering = Melihat isi file yang ada pada folder Engineering
- ls HR = Melihat isi file yang ada pada folder HR




# LANGKAH 2 - PINDAHKAN DAN SALIN FILE

# Memindahkan File tertentu ke Folder Archives :
[Deskripsi gambar] (https://drive.google.com/file/d/1FQjDF9yz9KBLRQzEhQOFJGjJvazL5_1N/view?usp=sharing) 

~~~
mv /home/melinda/tugas_proyek/document/file{1..10}.txt /home/melinda/Project_1/Marketing/Documents
~~~

Penjelasan :
- memindahkan file dari folder lama ke folder baru sebagai simulasi pengarsipan.

# Menyalin File :
[Deskripsi gambar] (https://drive.google.com/file/d/1DFntW2SI5yepqXxG7dCp50Yfn_oaH-ri/view?usp=sharing)

~~~
cp -R /home/melinda/Project_1/Marketing/Documents /home/melinda/Project_1/Marketing/Archives
~~~

Penjelasan :
- saya salin menggunakan cp, agar file tersebut tetap ada di lokasi lama sekaligus memiliki salinan di folder project.




# LANGKAH 3 - MENGATUR PERMISSION

# Membuat Akun Pengguna Departemen Marketing :
[Deskripsi gambar] (https://drive.google.com/file/d/1mEYHxNTJGDYarMK4M_OX4GIWBEpFntgM/view?usp=sharing)

~~~
sudo adduser admin_marketing
~~~

# Mengatur/Mengubah Kepemilikan Departemen Marketing :
[Deskripsi gambar] (https://drive.google.com/file/d/1AwJUnJliUbtTmm3l96Pjt6GHkmTr0GhN/view?usp=sharing)

~~~
sudo chown -R admin_marketing /home/melinda/Project_1/Marketing
~~~

# Mengubah Hak Akses Departemen Marketing :
[Deskripsi gambar] (https://drive.google.com/file/d/1inleeNjXfzo2-3NkPTxD89-mySFaIzF8/view?usp=sharing)

~~~
sudo chmod -R 700 /home/melinda/Project_1/Marketing
~~~

- Tambahan : Hak akses 700 berarti hanya pemilik (admin_marketing) yang dapat Baca, Tulis, dan Eksekusi.



# Membuat Akun Pengguna Departemen Engineering :
[Deskripsi gambar] (https://drive.google.com/file/d/1Sb12xa6GkxssV13CtcrjQjCVVJxVPoLE/view?usp=sharing)

~~~
sudo adduser admin_engineering
~~~

# Mengatur/Mengubah Kepemilikan Departemen Engineering :
[Deskripsi gambar] (https://drive.google.com/file/d/128vtkHo6AEwLBk-VixmKEPxSPYnxy6Fp/view?usp=sharing)

~~~
sudo chown -R admin_engineering /home/melinda/Project_1/Engineering
~~~

# Mengubah Hak Akses Departemen Enginering :
[Deskripsi gambar] (https://drive.google.com/file/d/1fJU7hWzPUUv82iZSAMfNmzzP3GTkq64A/view?usp=sharing)

~~~
sudo chmod -R 700 /home/melinda/Project_1/Engineering
~~~

- Tambahan : Hak akses 700 berarti hanya pemilik (admin_engineering) yang dapat Baca, Tulis, dan Eksekusi.



# Membuat Akun Pengguna Departemen HR :
[Deskripsi gambar] (https://drive.google.com/file/d/1F3r4mtjcEXSRreWZStLgCS0mDD4D-paJ/view?usp=sharing)

~~~
sudo adduser admin_hr
~~~

# Mengatur/Mengubah Kepemilikan Departemen HR :
[Deskripsi gambar] (https://drive.google.com/file/d/1h96rZiZ0fyBxojWftmgasoRtUIN15aGa/view?usp=sharing)

~~~
sudo chown -R admin_hr /home/melinda/Project_1/HR
~~~

# Mengubah Hak Akses Departemen HR :
[Deskripsi gambar] (https://drive.google.com/file/d/1qvke5AhD0Ud1Xma0QJci52n2ytiSr3FJ/view?usp=sharing)

~~~
sudo chmod -R 700 /home/melinda/Project_1/HR
~~~

- Tambahan : Hak akses 700 berarti hanya pemilik (admin_hr) yang dapat Baca, Tulis, dan Eksekusi.


# Verifikasi Hak Akses - Marketing (Izin Ditolak) :
[Deskripsi gambar] (https://drive.google.com/file/d/1ZJBj1cC68brOm0oJlZscYkAJbthXIjf9/view?usp=sharing)

~~~
cd Marketing
~~~

- Tambahan : Saya memverifikasi bahwa pengguna biasa (melinda) tidak bisa mengakses direktori departemen lain.

# Verifikasi Hak Akses - Marketing (Akses Berhasil) :
# Beralih Pengguna :
[Deskripsi gambar] (https://drive.google.com/file/d/1I6uzqpeRWq99yoVqDzhWG17kfLTk-GEa/view?usp=sharing)

~~~
su admin_marketing
~~~

# Masuk ke Direktori :
[Deskripsi gambar] (https://drive.google.com/file/d/1Bl8wIy3sMCSCoHt8r6kndqW5vVUOBLp6/view?usp=sharing)

~~~
cd Marketing
~~~

# Melihat ISI Direktori :
[Deskripsi gambar] (https://drive.google.com/file/d/1upx0fcPSB_yYY50U_uqC-XzeU9l1dutN/view?usp=sharing)

~~~
ls
~~~

- Tambahan : (menampilkan Archives Documents)

# Keluar dari Direktori :
[Deskripsi gambar] (https://drive.google.com/file/d/1YBAuKJlHojFFAgYHiylgh1mhEZzVyC0t/view?usp=sharing)

~~~
exit
~~~


# Verifikasi Hak Akses - Engineering (Izin Ditolak) :
[Deskripsi gambar] (https://drive.google.com/file/d/1vpuT8NcsFy6_iIhVr60RFGwcfyDPx5OM/view?usp=sharing)

~~~
cd Engineering
~~~

- Tambahan : Saya memverifikasi bahwa pengguna biasa (melinda) tidak bisa mengakses direktori departemen lain.

# Verifikasi Hak Akses - Engineering (Akses Berhasil) :
# Beralih Pengguna :
[Deskripsi gambar] (https://drive.google.com/file/d/1uzKXuRFePlE8PkpXBAttCMP_5Xp8vnH5/view?usp=sharing)
~~~
su admin_engineering
~~~

# Masuk ke Direktori :
[Deskripsi gambar] (https://drive.google.com/file/d/1AZoIqE-EGqYMeEsFBs3kOgwXgtubwUFy/view?usp=sharing)

~~~
cd Engineering
~~~

# Melihat ISI Direktori :
[Deskripsi gambar] (https://drive.google.com/file/d/1TyZ-4JarDkg2cNnklUddkD0UXE78rzY3/view?usp=sharing)

~~~
ls
~~~

- Tambahan : (menampilkan Archives Documents)

# Keluar dari Direktori :
[Deskripsi gambar] (https://drive.google.com/file/d/1V-K5d7dPiLCxJZAL-wzfaMDjowN9Pmjk/view?usp=sharing)

~~~
exit
~~~


# Verifikasi Hak Akses - HR (Izin Ditolak) :
[Deskripsi gambar] (https://drive.google.com/file/d/1Erk1RCqE0GkCFgjCIz6CLeBI4ix9CJ0b/view?usp=sharing)

~~~
cd HR
~~~

- Tambahan : Saya memverifikasi bahwa pengguna biasa (melinda) tidak bisa mengakses direktori departemen lain.

# Verifikasi Hak Akses - HR (Akses Berhasil) :
# Beralih Pengguna :
[Deskripsi gambar] (https://drive.google.com/file/d/1S42RUtVleV-e9q1T9Rg-edtUVsbhJASg/view?usp=sharing)
~~~
su admin_hr
~~~

# Masuk ke Direktori :
[Deskripsi gambar] (https://drive.google.com/file/d/1xXSVZAv49rMklQUeOte0Cj9_y7vh51QA/view?usp=sharing)

~~~
cd HR
~~~

# Melihat ISI Direktori :
[Deskripsi gambar] (https://drive.google.com/file/d/12Q7_jEY2UqPwtzMsTfW8n-a8ypvar6tn/view?usp=sharing)

~~~
ls
~~~

- Tambahan : (menampilkan Archives Documents)

# Keluar dari Direktori :
[Deskripsi gambar] (https://drive.google.com/file/d/1kWrOGexmZX4hQVh1pWPd9WDH6KYZ3jBW/view?usp=sharing)

~~~
exit
~~~




# LANGKAH 4 - CARI DAN FILTER

# Mencari Semua File PDF :
[Deskripsi gambar] (https://drive.google.com/file/d/1fsmv82w4Cmzsf2Djz6S8Wf3wXqKhyhLY/view?usp=sharing)

~~~
sudo find /home/melinda/tugas_proyek -type f -name "*.pdf" -mtime -7 > daftar_pdf.txt
~~~

Penjelasan :
- Saya menggunakan find untuk mencari semua file PDF (-name "*.pdf") di direktori /home/melinda/tugas_proyek dengan tipe file biasa (-type f) yang dimodifikasi dalam 7 hari terakhir (-mtime -7), dan mengarahkan hasilnya ke file daftar_pdf.txt.

# Memverifikasi File :
[Deskripsi gambar] (https://drive.google.com/file/d/1t0pDsi3k5E5DCFbpGdLQoFDfaiW3_hao/view?usp=sharing)

~~~
ls
~~~

# Menampilkan ISI File (daftar_pdf.txt) :
[Deskripsi gambar] (https://drive.google.com/file/d/1izoWZfgLbCQqWdpcCU5N7beYI_0AgfXb/view?usp=sharing)

~~~
cat daftar_pdf.txt
~~~

- Tambahan : Output menunjukkan daftar file PDF yang berhasil dicari.

