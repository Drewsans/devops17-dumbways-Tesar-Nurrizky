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
- Dikarenakan memakai VM baru, saya memndownload nodejs dengan Command : sudo apt install nodejs
- Setelah itu check apakah nginx sudah aktif atau belum dengan Command : sudo systemctl status nginx
 
- Dan ketika sudah aktif bisa di check pada web browser dengan IP Address yang kita punya saya IP Address nya adalah 192.168.1.145

![instal nginx nodejs check system](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/361a6b3e-079e-42fb-9fc9-857ef25a90e8)

 ![nginx di web](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/749b7916-e3e5-43e4-871c-c6796a5196c5)

- Setelah Download dan aktif, install PM2 dengan command : sudo npm install -g pm2

![instal pm2](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/d4ae4106-1474-458f-b1ff-55da0c0971ef)

- Setelah itu check node dan npm dengan command 
 
  node -v
  
  npm -v
  
- Clone aplikasi dumbflix frontend yang telah ditugaskan dengan command :
  
  git clone https://github.com/dumbwaysdev/dumbflix-frontend
  
tetapi dikarenakan saya sudah punya jadi keterangan menjadi already exists.
  
- Lalu setelah di clone ubah directory ke dumbflix-frontend dengan command :
  cd dumbflix-frontend
  
- Setelah itu install npm dengan command :
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

- Setting juga di /etc/hosts/ di Ubuntu dengan Command :
 
sudo nano /etc/hosts
 
![etc-hosts di ubuntu](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/d86fcb08-e813-40f4-9c61-dd7c260b1562)

- Dan jangan lupa juga setting pada laptop di folder Windows(C):/Windows/System32/drivers/etc/hosts/ :
 
![etc-hosts-drivers](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/989e67a4-e507-435a-b7b0-d306eb2588c8)

- Setelah itu check apakah configuration file di nginx.conf sudah atau belum.
 
- Setelah itu check status nginx apakah aktif atau tidak.
 
![sudo nano etc-nginx-sites-available](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/6a173538-d042-454e-b47e-b4a7dfc8fba2)

- Berikut didalam file etc/nginx/sites-available/dumbflix-tesar.xyz
 
 ![etc-nginx-sites-available](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/86ff7abf-d6c1-4583-b93d-9c763c89021c)

- Setelah itu check PM2 dengan Command :
 
 pm2 list
 
- Setelahnya aktifkan PM2 dengan Command :
 
 pm2 start
 
- Setelah itu aktifkan file ecosystem.config.js dengan Command :
 
 pm2 ecosystem simple

![pm2 list, start, pm2 ecosystem](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/bae6ce6b-0924-4d70-8403-13d1394d1d10)

- Setelah terbuat dan aktif ecosystem.config.js lalu buat code didalamnya sebagai berikut :
 
![image](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/25766b7b-a6c7-48e6-ad78-4e91daa84389)

- Setelah semua tersetting semua lalu tinggal jalankan kembali pm2 start. lalu tinggal lihat di web browser dengan domain :

dumbflix-tesar.xyz
 
 ![aplikasi jalan di web dengan domain](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/f35d0b1a-0c18-439d-b701-8d8d185aed91)

- Dan lihat juga apakah di IP Address yang kita punya di tambah localhost 3000 apakah berjalan juga :
 
192.168.1.145:3000
 
 ![aplikasi jalan di web dengan ip address](https://github.com/Drewsans/devops17-dumbways-Tesar-Nurrizky/assets/118201274/944a1d17-52d0-4579-8447-e0fc0d4e54b1)

.:: Terimakasih telah Berkunjung ::.
