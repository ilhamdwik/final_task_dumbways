# Web Server

## Before you start the task, please read this:
### - Please screenshot the command step-by-step
### - Describe the process in your final task repository

## Requirements
### - NGINX / Apache
### - SSL Certbot

## Instructions
### - Use these domains :
  #### - <name>.studentdumbways.my.id [Deployment]
  #### - api.<name>.studentdumbways.my.id [Deployment]
  #### - node.<name>.studentdumbways.my.id [Node Exporter]
  #### - dash.<name>.studentdumbways.my.id [Grafana Dashboard]
  #### - prom.<name>.studentdumbways.my.id [Prometheus]
  #### - jenkins.<name>.studentdumbways.my.id [Jenkins]

### - SSL Certificates using wildcard
![16](../assets/web_server/1.png)

![17](../assets/web_server/2.png)

![18](../assets/web_server/3.png)

![19](../assets/web_server/4.png)

### - Deploy the certificate using ansible (*Challenge*)


* #### Install nginx.
![01](../assets/web_server/1.png)

* #### Step ini agar nginx bisa mengetahui bahwa kita membuat configurasi di dalam file final_task dengan membaca semua file dengan format .conf.
![02](../assets/web_server/2.png)

* #### Buat folder final_task.
![03](../assets/web_server/3.png)

![04](../assets/web_server/4.png)

* #### Disini saya sudah membuat configurasi SSL certificate certbot menggunakan wildcard, jadi SSL certbot ini akan secara otomatis menambahkan configurasi tambahan di dalam file configurasi nginx kita.
![05](../assets/web_server/5.png)

![06](../assets/web_server/6.png)

![07](../assets/web_server/7.png)

![08](../assets/web_server/8.png)

![09](../assets/web_server/9.png)

![10](../assets/web_server/10.png)

![11](../assets/web_server/11.png)

![12](../assets/web_server/12.png)

![13](../assets/web_server/13.png)

![14](../assets/web_server/14.png)

![15](../assets/web_server/15.png)