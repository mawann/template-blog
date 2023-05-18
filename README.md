# template-blog

Cara menggunakan file-file ini, ketik:  
git clone https://github.com/mawann/template-blog  

Untuk Nginx Server Block, kodenya adalah:
```
server {  
  listen      80;  
  listen      [::]:80;  
  root        /var/www/domain.com/html;  
  index       index.php index.html index.htm;  
  server_name domain.com www.domain.com;  

  error_log   /var/log/nginx/error.domain.com.log error;  
}
```
Dah. Gitu saja.
