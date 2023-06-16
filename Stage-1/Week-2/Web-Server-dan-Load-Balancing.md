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
 
- Dan ketika sudah di aktif bisa di check pada web browser dengan IP Address yang kita punya saya IP Address nya adalah 192.168.1.145

![instal nginx nodejs check system](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/361a6b3e-079e-42fb-9fc9-857ef25a90e8)

 ![nginx di web](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/749b7916-e3e5-43e4-871c-c6796a5196c5)

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

- Selanjutnya buat PM2 dengan nama kalian sendiri dengan Command :
 
pm2 start npm --name tesar -- start
 
- Setelah itu masukkan code pada file /etc/nginx/sites-available/dumbflix-tesar.xyz dengan code ini :

server {
    
 listen 80;
    
 server_name dumbflix-tesar.xyz; (Isi dengan nama server yang diinginkan)

    location / {
        proxy_pass http://localhost:3000; (isi sendiri ingin di localhost berapa)
        proxy_http_version 1.1;
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection 'upgrade';
        proxy_set_header Host $host;
        proxy_cache_bypass $http_upgrade;
    }
}
 
- Setelah itu check apakah configuration file di nginx.conf sudah atau belum.
 
- setelah itu check status nginx apakah aktif atau tidak.
 
![sudo nano etc-nginx-sites-available](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/6a173538-d042-454e-b47e-b4a7dfc8fba2)

- Berikut didalam file etc/nginx/sites-available/dumbflix-tesar.xyz
 
 ![etc-nginx-sites-available](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/86ff7abf-d6c1-4583-b93d-9c763c89021c)

- Setelah itu check PM2 dengan Command :
 
 pm2 list
 
- Setelahnya aktifkan PM2 dengan Command :
 
 pm2 start
 
- Setelah aktif 
