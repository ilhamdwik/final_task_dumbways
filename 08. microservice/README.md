![00](../assets/SOAL_FINAL_TASK/8.png)

# Microservices

## Before you start the task, please read this:
### - Please screenshot the command step-by-step
### - Describe the process in your final task repository

## Requirements
### - Docker Swarm / Minikube / Kind Cluster
### - Kubernetes Engine (*Challenge*)

## Instructions
### - Deploy leader on *CI/CD Server*, then apply worker in *Appserver*
### - Use front-end app in Microservices
### - Set 2 replicas inside the service
### - Front-end integrated with Back-end


* #### - Menginisialisasi docker swarm init sebagai leader.
![01](../assets/microservices/1.png)

![02](../assets/microservices/2.png)

* #### - Menginisialisasi docker swarm join untuk menambah worker.
![03](../assets/microservices/3.png)

![04](../assets/microservices/4.png)

* #### - Pull images dari docker hub.
![05](../assets/microservices/5.png)

* #### - Membuat dan menjalankan service. Docker swarm secara otomatis akan memberikan port kepada service yang dijalankan.
![06](../assets/microservices/6.png)

![07](../assets/microservices/7.png)

* #### - Scale untuk membuat replica aplikasi. Jadi kita mempunyai satu aplikasi dan ingin memperbanyak aplikasi kita agar jika mengalami down di salah satu server, maka client masih bisa mengakses aplikasi kita di server yang lain yang masih berjalan dengan normal.
![08](../assets/microservices/8.png)

* #### - Bisa dilihat disini bahwa setelah melakukan scale, aplikasi kita bisa berjalan di dua server berbeda monitoring dan appserver.
![09](../assets/microservices/9.png)

* #### - Bisa dilihat bahwa saya menggunakan ip berbeda saat mengakses aplikasi wayshub.
![10](../assets/microservices/10.png)

![11](../assets/microservices/11.png)

* #### - Saya sudah membuat load balance yang berguna bila mengalami down di salah satu server, maka client masih bisa mengakses aplikasi kita di server yang lain yang masih berjalan dengan normal.
![12](../assets/microservices/12.png)

![13](../assets/microservices/13.png)

![14](../assets/microservices/14.png)