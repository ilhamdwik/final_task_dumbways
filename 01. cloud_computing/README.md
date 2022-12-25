![00](../assets/SOAL_FINAL_TASK/1.png)

# Cloud Computing

## Before you start the task, please read this:
### - Please screenshot the command step-by-step
### - Describe the process in your final task repository

## Requirements
### - Setup 3 VMs with the following specs
   #### - Appserver - 2 vCPU, 2GB RAM - 20GB Storage
   ![01](../assets/vm/1.png)

   #### - Gateway - 1 vCPU, 1GB RAM - 20GB Storage
   ![02](../assets/vm/2.png)

   #### - Monitoring - 2 vCPU, 2GB RAM - 20GB Storage
   ![03](../assets/vm/3.png)


## Instructions
### - User login without password authentication

* #### - Untuk step ini saya jabarkan di dalam tugas ssh.

### - Remove password login method

* #### - Masuk ke dalam file /etc/ssh/sshd_config. Ubah PasswordAuthentication yang semula yes menjadi no. Ini akan membuat server kita saat diremote tidak perlu memasukkan password. Catatan : perlu diingat sebelum menjalankan step ini pastikan sudah menambahkan public key ke dalam file authorized_keys di dalam server yang ingin kita remote, jika belum menambahkan public key, maka kita tidak bisa masuk ke dalam server.
   ```
   sudo nano /etc/ssh/sshd_config
   ```
   ![04](../assets/cloud_computing/1.png)

   ![05](../assets/cloud_computing/2.png)

   ![06](../assets/cloud_computing/3.png)

   ![07](../assets/cloud_computing/4.png)

* #### - Jangan lupa untuk me-restart ssh.
   ```
   sudo systemctl restart ssh
   ```
   ![08](../assets/cloud_computing/5.png)

### - All servers are **not allowed** to use *Public IP* (except Gateway)