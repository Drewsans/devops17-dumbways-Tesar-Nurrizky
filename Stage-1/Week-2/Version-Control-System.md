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

_Setelah terbuat lalu refresh pada github repository example apakah data suddah masuk pada github atau belumnya.

![cap github example](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/008d6cf1-4e00-4aa3-92c5-4829993b689d)

#3. Buat 2 Branch dengan nama branch Staging dan Production

_Pertama-tama buatlah branch staging dengan Command : git branch staging

_setelah itu untuk pindah branch dengan Command : git checkout staging(dikarenakan saya ingin ke branch staging).

_Selanjutnya buat isi staging branch dengan Command : echo "Staging Branch" > file1

_Selanjutnya tambah kan ke file1 dengan Command : git add file1

_Setelah semua dilakukan Commit dengan Command berikut : git commit -m "Add changes to file1 in staging branch"

![git branch staging](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/6b744ed5-bf9a-41ac-8f00-9a15b0474a18)

_Pertama-tama buatlah branch production dengan Command : git branch production

_setelah itu untuk pindah branch dengan Command : git checkout production(dikarenakan saya ingin ke branch production).

_Selanjutnya buat isi production branch dengan Command : echo "production Branch" > file2

_Selanjutnya tambah kan ke file1 dengan Command : git add file2

_Setelah semua dilakukan Commit dengan Command berikut : git commit -m "Add changes to file2 in production branch"

![git branch production](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/0b0717c3-37c0-4fdc-9635-c6c9ff37eceb)

_Setelah terbuat branch staging lalu push branch dengan Command : git push origin staging

![git push staging](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/e1d2abfb-6a96-4476-b6f4-676c796d327f)

_Setelah terbuat branch production lalu push branch dengan Command : git push origin production

![git push production](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/696399fb-2ef7-4f5f-8cda-44b30902125d)

#4. Berikut adalah tiga perintah Git yang belum dijelaskan:

_git stash: perintah ini digunakan untuk menyimpan perubahan sementara pada direktori kerja tanpa melakukan commit. Perintah ini berguna ketika pengembang ingin beralih ke branch lain atau mengatasi konflik merge tanpa melakukan commit terlebih dahulu.


_git cherry-pick: perintah ini digunakan untuk memilih satu atau beberapa commit dari branch lain dan menerapkannya ke branch saat ini. Perintah ini berguna ketika pengembang ingin menerapkan perubahan tertentu dari branch lain tanpa harus menggabungkan seluruh branch.


_git rebase: perintah ini digunakan untuk mengubah sejarah commit dengan memindahkan commit ke branch lain atau menggabungkan beberapa commit menjadi satu commit. Perintah ini berguna ketika pengembang ingin membersihkan sejarah commit atau menghindari konflik merge yang terjadi ketika melakukan git merge.
