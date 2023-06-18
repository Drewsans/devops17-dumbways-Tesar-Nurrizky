#Day 1 - Introduction to DevOps

* Definisi DevOps?
DevOps adalah singkatan dari Development dan Operations, yang merupakan prinsip atau pola pikir yang digunakan di dunia IT. DevOps bertujuan untuk meningkatkan kolaborasi antara tim development dan tim operation dari mulai perencanaan hingga aplikasi dan fitur ter-deliver atau tersampaikan ke pengguna. 
DevOps juga dirancang agar dapat meningkatkan kemampuan sebuah perusahaan untuk proses delivery aplikasi dengan kecepatan tinggi.

* Lifecycle DevOps terdiri dari beberapa tahapan. Yaitu :
1. Continuous Development : Tahap ini melibatkan pengembangan kode secara terus-menerus untuk memperbaiki dan meningkatkan aplikasi.
2. Continuous Integration : Tahap ini melibatkan penggabungan kode dari beberapa pengembang ke dalam satu repositori, dan melakukan build dan pengujian otomatis secara terus-menerus.
3. Continuous Testing : Tahap ini melibatkan pengujian otomatis secara terus-menerus untuk memastikan bahwa aplikasi berfungsi dengan baik dan memenuhi persyaratan bisnis.
4. Continuous Deployment : Tahap ini melibatkan pengiriman kode ke lingkungan produksi secara otomatis setelah melalui tahap pengujian.
5. Continuous Monitoring : Tahap ini melibatkan pemantauan aplikasi secara terus-menerus untuk memastikan bahwa aplikasi berjalan dengan baik dan memenuhi persyaratan bisnis.

* Install Ubuntu 
Pertama-tama untuk Windows membutuhkan Virtual Machine Software yaitu VMWare, ----Pertama Download VMWare
- Setelah VMWare Terdownload lanjutkan untuk menginstal Ubuntu dengan pertama tama Create a New Virtual Machine seperti dibawah ini :

![image](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/f125772d-3a6a-40a6-8337-9877ed355751)

- Setelah Memilih create a new virtual machine lanjutkan dengan memilih installer disc image file (iso) : Ubuntu yang sudah di download

![instal iso ubuntu](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/640a71f5-140f-4f60-b094-389d10eaadee)

- Lanjutkan dengan Mengisi Instal Information seperti Nama, Username, Dan Password

![Easy Instal Information](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/1383b858-21e8-41c6-8cd9-56a119fdaa64)

- Selanjutnya Tentukan Maximum Disk untuk VM Ubuntu server disini saya sedikit Improvisasi dikarenakan sedikit error jika di set 10GB jadi saya mengambil 12 GB Untuk Maximum Disk :

![Tentukan Directory](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/a606183a-5d10-46fd-b5db-fe5c2f1901f6)

- Selanjutnya Custom Hardware untuk Ubuntu di set dengan Memory 1-2 GB, Proccesor Core 1-2, dan Network Adapter NAT menjadi Bridged :

![configurasi network](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/d441d8d7-29d3-45b6-8c19-b5d3013bc5f4)

![setelah di configurasi](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/6d4e3879-0898-4350-81f6-c2a7f2ad7394)

- Setelah itu Lanjut dengan Pilih Finish setelah finish akan menjalankan VMWare untuk instal Ubuntu

- Sampai ada tampilan Pilihan bahasa sudah memasuki untuk instal Ubuntu :

![pilih bahasa](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/191d34f8-8ef4-4cb6-bd84-8fee9c077eaf)

- setelah itu memilih bahasa yang telah disediakan :

![pilih bahasa](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/6f188cac-540b-47cf-8b87-e9ef1802553b)

- Setelah itu mengganti IP Address dari Dynamic ke Static :

![configurasi Subnet](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/05719c9d-87b3-4e03-8b14-f3d06478c3ef)

- setelah itu pilih Custom Storage layout :

![Pilih Custom space penyimpanan](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/2199cd70-9ed9-4ae9-b591-96c031bfd1d7)

- Setelah itu buat partisi berisi 9GB untuk Data 1,5 GB untuk SWAP atau Cadangan

![penentuan data](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/3808003f-d46a-400c-b04f-40d64be6c09a)

- Selanjutnya Memasukan data untuk profile setup :

![Profile setup](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/16d1189c-cbbe-4af5-b69e-e52fe44df41e)

- Setelah memasukan data lanjut untuk apply untuk instal openSSH server :

![image](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/13cdd720-dab0-41c2-98df-8a3c0e0c6be0)

- Setelah menunggu lumayan lama untuk menginstal seluruh rangkaian penginstalan. selanjutnya reboot terlebih dahulu virtual machinenya :

 ![image](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/8637f0e4-9dc8-4b1d-b102-3e64b8dd036a)


- Setelah membuka kembali VM Ubuntu dan tampilan awal seperti ini berati penginstalan telah selesai.

![setelah berhasil terinstal ubuntu](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/bed303b9-2a6f-4279-bd25-06a7bc533f63)

- Check apakah VM Ubuntu sudah bisa di gunakan dengan menggunakan Command PING contohnya ping google.com :

![ping google](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/bf45541a-ddfd-4b5a-959e-a9648b552a70)


                                                  .::Terimakasih Telah Berkunjung::.
