#Day 1 - Version Control System

Task :
1. Penjelasan Distributed Version Control
2. buat repository sample (diluar tugas) yang berisi 3 file dengan isi yang berbeda
3. Buat 2 branch
- Staging
- Production
4. Cari 3 command git yang belum dijelaskan

#1. *Distributed Version Control System (DVCS)* adalah sistem kontrol versi yang memungkinkan setiap anggota tim memiliki salinan lengkap dari repositori. 
Setiap anggota tim dapat melakukan operasi seperti commit, branch, dan merge secara lokal tanpa memerlukan koneksi internet. 
Keuntungan dari DVCS adalah memungkinkan tim untuk bekerja secara terdistribusi dan independen, serta memungkinkan pengembang untuk bekerja secara offline. 
Beberapa contoh DVCS yang populer adalah Git, Mercurial, dan Bazaar.

#2. _Pertama-tama atur terlebih dulu untuk global github dengan Command :

_$ git config --global user.name "username pada github"

_$ git config --global user.email "email yang terdaftar di github"

![config username email github](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/6233ed32-9eb9-4237-b503-735bdd4df67d)

_Buat repository dengan Command : git init 

_Selanjutnya buat file dengan Command : touch file1 file2 file3

_Setelah membuat file lalu masukkan pada repository yang telah di buat tadi dengan command : git add file1 file2 file3.

_Selanjutnya check dengan Command : git status

![buat git init](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/d003d991-d67e-4c1d-a069-c542d23b030f)

_Setelah itu lanjutkan dengan Commit dengan Command : git command -m "tesar file"

_Lalu lanjutkan dengan masukkan Command : git remote add origin git@github.com:Drewsans/example.git

_Selanjutnya push master origin dengan Command : git push origin master

_Lalu buat isi file dengan Command :

- echo "file1" > file1

- echo "file2" > file2

- echo "file3" > file3

![git commit](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/d7fc4c9e-22c7-4375-8602-faa0112bfc56)

_
