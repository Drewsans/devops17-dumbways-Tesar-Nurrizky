#Day 7 - Web Server dan Load Balancing

Task :
1. Instalasi nginx melalui apt
2. menjalankan aplikasi dumbflix menggunakan PM2
3. buatlah konfigurasi reverse proxy!
(Gunakan 2 server untuk memenuhi challenge, tidak wajib)

Referensi :
- Nama Domain - dumbflix-<nama panggilan>.xyz
- Dumbflix-FE - ```https://github.com/dumbwaysdev/dumbflix-frontend```


#1. 
- Instalasi NGINX memakai Command : sudo apt install nginx
- dikarenakan memakai VM baru, saya memndownload nodejs dengan Command : sudo apt install nodejs
- setelahnya check apakah nginx sudah aktif atau belum dengan Command : sudo systemctl status nginx

![instal nginx nodejs check system](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/361a6b3e-079e-42fb-9fc9-857ef25a90e8)

- Setelah Download dan aktif, install PM2 dengan command : sudo npm install -g pm2

![instal pm2](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/d4ae4106-1474-458f-b1ff-55da0c0971ef)

- setelah itu check node dan npm dengan command 
 
  node -v
  
  npm -v
  
- clone aplikasi dumbflix frontend yang telah ditugaskan dengan command :
  
  git clone https://github.com/dumbwaysdev/dumbflix-frontend
  
tetapi dikarenakan saya sudah punya jadi keterangan menjadi already exists.
  
- Lalu setelah di clone ubah directory ke dumbflix-frontend dengan command :
  cd dumbflix-frontend
  
- setelah itu install npm dengan command :
  npm install
  
![git clone dumbflix](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/87803a18-1df6-4e37-bddd-8f038b74033f)

- 
