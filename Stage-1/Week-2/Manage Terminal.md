#Day 6 - Manage Terminal

Task :
1. Penjelasan text manipulation beserta step by step
2. Penjelasan tool htop atau nmon

#1. Text manipulation atau manipulasi teks adalah proses mengubah atau memodifikasi data teks menggunakan berbagai perintah dan alat yang tersedia di Linux. Hal ini melibatkan melakukan operasi seperti pencarian, penyaringan, penggantian, pemformatan, dan ekstraksi bagian tertentu dari data teks. 

Berikut beberapa Command yang digunakan untuk Text Manipulation :

- echo
Untuk membuat kalimat atau kata didalam file. Seperti pada gambar berikut :

![echo](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/74516b72-446e-4b89-9009-253f0e93ef25)

- cat (catch)
Untuk mengambil atau membuka apa isi di dalam file, dan bisa juga untuk menggabungkan isi file 1 dan file 2 menjadi isi gabungan dari file 1 dan file 2 berada di file 4. Seperti di gambar berikut :

![cat](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/d6a57cf6-1595-48e2-80a5-e1d7bb39eccb)

- grep
untuk mengambil salah satu kata yang berada di dalam isi file. Seperti gambar berikut :

![grep](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/17800add-bfac-4318-a5aa-b7eb9c53bb1a)

- paste
untuk menggabungkan kalimat atau kata yang berada di dua file. Seperti gambar berikut :

![paste](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/54084daa-3f3d-4112-bcb1-f9ae36c08a00)

- sort
untuk menyortir atau mengurutkan kalimat atau kata yang berada dialam file. seperti gambar berikut :

![sort](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/f4f3ef75-a0d9-4dfd-b047-741c2f55a53f)

- tr
mengubah isi kalimat atau kata menjadi seluruh isi Kapital atau seluruh isi menjadi huruf kecil. Seperti gambar berikut :

![tr](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/7f4f2e8d-dba6-45d5-8198-8fd617759050)

- awk
mengambil salah satu kata dalam sebuah kalimat pada isi file. Seperti gambar berikut :

![awk](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/46c5a070-76e6-41d7-b46d-f3cf5c5f2a3f)

#2. Penjelasan Nmon (Nigel's Performance Monitor)
Nmon adalah Sebuah utilitas sistem operasi Linux yang digunakan untuk memantau kinerja sistem secara real-time. Nmon dapat menampilkan informasi tentang penggunaan CPU, memori, disk, jaringan, dan sumber daya sistem lainnya dalam bentuk tabel dan grafik.

- dikarenakan pada Sistem Operasi yang baru terdownload hanya htop maka jika menginginkan Nmon perlu mendownload terlebih dahulu.
-Dengan Command berikut : sudo apt install nmon

![download nmon](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/6ee97ae1-8236-4fea-8227-588ceb6b3e4a)

- Seperti ini tampilan awal ketika membuka nmon

![tampilan nmon](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/133905ed-cb73-4b1f-8e0f-bb2286ed4b19)

Berikut adalah gabungan tampilan dari mengambil informasi :
- CPU dengan = c
- Memory dengan = m
- disks dengan = d
Hasil nya seperti gambar berikut :

![tampilan CPU, Memory, dan Disk](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/bb13006a-d765-477f-8c1d-c7cc4521201b)

- Berikut adalah gabungan tampilan dari mengambil informasi :
- Resources linux dan Processor dengan = r
Hasil nya seperti gambar berikut :

![tampilan Resources linux dan processor](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/e36f338a-1fee-4f7a-90f7-122da5b301b9)

Berikut adalah gabungan tampilan dari mengambil informasi :
- Verbose dengan = V
- Kernel dengan = k
- Network dengan = n
- Top Proccesses dengan = t
Hasil nya seperti gambar berikut :

![tampilan Verbose Mode, Kernel, Network, Dan Top Processor](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/1e78159b-f826-4ba9-813e-74bb673ef1df)

.:: Terimakasih Telah Berkunjung::.
