Day 3 - Application In Server

1. Perbandingan antara Monolith & Microservices
2. Deploy Aplikasi wayshub-frontend (NodeJS)
3. Deploy Golang & Python dengan menampilkan nama masing-masing



#1. Perbandingan antara Monolith & Microservices:
* Monolith
- Monolith adalah Arsitektur aplikasi yang dibangun sebagai satu kesatuan sistem yang besar dan biasanya memiliki satu basis kode.
- Monolith memiliki keuntungan dalam hal manajemen kode yang mudah dan pengurangan overhead kognitif, serta kemudahan dalam deployment karena semua fitur dirilis secara bersamaan.
- Monolith cocok digunakan pada awal pengembangan aplikasi.
- Monolith lebih mudah dalam hal debugging dan keamanan karena tidak ada interaksi antar modul.
- Monolith lebih mudah dalam hal manajemen teknologi karena tidak ada perubahan teknologi.

* Microservices
- Microservices adalah arsitektur aplikasi yang terdiri dari beberapa modul kecil yang independen satu sama lain dan memiliki basis kode yang terpisah.
- Microservices memiliki keuntungan dalam hal skalabilitas, fleksibilitas, dan kemampuan untuk melakukan deployment secara independen.
- Microservices cocok digunakan pada aplikasi yang sudah mapan dan membutuhkan skalabilitas.
- Microservices lebih sulit dalam hal debugging dan keamanan karena adanya interaksi antar modul melalui jaringan.
- Microservices lebih sulit dalam hal manajemen teknologi karena setiap modul dapat menggunakan teknologi yang berbeda.

#2. Deploy Wayshub-Frontend

- Pertama tama kita mengambil data dengan git atau clone repository dari wayshub=frontend
git clone https://github.com/dumbwaysdev/wayshub-frontend

![image](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/618564f1-df36-4e28-9c2c-c67af0d5a845)

- Cara melihat Node yang sedang digunakan :

![image](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/1b2ae9c2-ddae-46bb-a036-ee8feabbe23f)

- Jalankan Command : npm run build dan tunggu sebentar. dan check apakah sudah terbuat build dengan : ls.

![npm run build](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/a36ff54e-37d3-4b62-a245-53e5033db069)

![success npm run build](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/6cc7767e-3512-44fc-8ff8-b5310d8eedb3)

![ls build](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/c9c03ef0-f7d8-4e79-991f-31b23a9e8a6f)

- Setelah terbuat build lakukan install serve dengan command : npm install -g serve, setelah itu jalankan serve -s build untuk menjalankan node.js dan mendapatkan link untuk membuka wayshub-frontend.

![npm install -g serve](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/95ac6a2c-b456-4fda-8b18-878dd4b709fd)

- Berikut tampilan link yang telah dijalankan di web browser.

![success buka wayshub](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/94621da0-5891-4882-9c70-d202f0e97d68)

#3. Deploy Golang dan Python3 untuk menampilkan nama sendiri :

-- Buat folder golang dengan Command : mkdir golang , 
Pastikan apakah sudah terbuat dengan command ls,  
Lalu pindah folder dengan command cd golang , 
Setelahnya install golang dengan command :  wget https://golang.org/dl/go1.16.5.linux-amd64.tar.gz && sudo su sampai selesai.

![download golang](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/752e5c13-6982-49df-ba4d-a6a27d37adcd)

- Setelah terinstall kembali ke main folder dengan cd,
Selanjutnya masukkan Command : sudo nano .bashrc,
Dan tambahkan export didalam .bashrc dengan : export PATH=$PATH:/usr/local/go/bin,
Dan ubah directory ke /usr//local/go/bin lalu check dengan command ls

![cinfug golang](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/f3c642b1-29d3-4264-9fea-9e080babef46)

![tambah export path](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/9cea5a8d-0631-4a9c-ade4-12eb09b86781)

- Lalu gunakan exec bash untuk menjalankan go version dengan check golang

![versi golang](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/a0070eb4-b003-41fe-9455-5757caf3a706)

- Buat file index.go dengan command : touch index.go,
Lalu tambahkan code untuk menambahkan nama pada command :  nano index.go,
Setelahnya run golang dengan command : go run index.go.

![buat index golang](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/b53c306a-83ea-4a7c-9c5c-80a1ed40f08e)

![isi nano index golang](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/f98ccb04-a92f-443d-a73b-89007e51fb64)

![setelah di run golang](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/e1ad8956-d221-44c4-a61a-4ac62bebd7c1)

-- Buat Aplikasi Python3 

- Sebelumnya buat directory python dengan Command : mkdir python,
Selanjutnya ubah directory dari devops17 ke directory python dengan Command : cd python,
Setelh itu Install python3 dengan command : sudo apt install python3-pip,
Lalu install Flask dengan Command : pip install flask.

![mkdir, cd python, install python](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/e9758d9f-7477-47bb-af3a-58ace0bebbf1)

- Buat file python dengan nama tesar.py(bisa dibuat dengan nama bebas),
Selanjutnya pakai Command nano tesar.py untuk mengisi code didalan python.

![buat file tesar python](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/68855184-616a-49a4-9153-783774bd9dc7)

- Berikut isi code dalam nano tesar.py :

![isi dari nano tesar python](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/0ec1243d-f539-4c30-8b74-347dab5b6ec5)

- Setelah diisi dalam nano tesar.py,
Lalu jalankan file python dengan Command : python3 tesar.py

![jalankan python3 untuk generate link](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/6713ee66-6ae8-41a2-9449-d9557b000a59)

- Berikut Hasil setelah link diatas dijalankan di web browser.

![hasil link python di web browser](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/1894e971-5589-4d97-bd26-7b674fa69745)

.:: Terimakasih Telah Berkunjung ::.
