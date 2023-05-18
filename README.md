# template-blog

Cara menggunakan file-file ini, ketik:  
git clone https://github.com/mawann/template-blog  

Untuk Nginx Server Block, kodenya adalah:
```
server {
  listen      80;
  listen      [::]:80;
  
  root        /var/www/domain.com/template-blog;
  index       index.htm;
  server_name domain.com www.domain.com;  

  error_log   /var/log/nginx/domain.com.error.log error;

  location / {
    try_files $uri $uri/ =404;
  }
}
```
Simpan di `/etc/nginx/conf.d/domain.com.conf`  
Setelah itu reload Nginx dengan perintah `nginx -s reload`  

Dah. Gitu saja.
