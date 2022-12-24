# SSH

## Before you start the task, please read this:

### - Please screenshot the command step-by-step
### - Describe the process in your final task repository

## Requirements

### - Create a pair of SSH key

* #### - Buat private key dan public key.
   ```
   ssh-keygen
   ```
   ![01](../assets/cloud_computing/6.png)

* #### - Saya menggunakan ansible untuk mengirim public key ke dalam server appserver, gateway, dan monitoring.
   ![02](../assets/cloud_computing/7.png)

   ![03](../assets/cloud_computing/8.png)

   ![04](../assets/cloud_computing/9.png)

   ![05](../assets/cloud_computing/10.png)

* #### - Lalu cek di dalam ketiga server tadi apakah sudah ada public key di dalam file authorized_keys.
   ![06](../assets/cloud_computing/11.png)

   ![07](../assets/cloud_computing/12.png)

   ![08](../assets/cloud_computing/13.png)

   ![09](../assets/cloud_computing/14.png)


## Instructions

### - Only use 1 key for all features
### - Configure your SSH in 1 configuration file

* #### - Buat file config di dalam direktory .ssh
   ![10](../assets/ssh/6.png)

   ![11](../assets/ssh/2.png)

* #### - Dengan membuat file configurasi di dalam direktory .ssh, kita bisa me-remote server tanpa menggunakan ip dari server yang dituju, dikarenakan di dalam file config kita sudah membuat konfigurasi bahwa saat "ssh appserver", berarti kita ssh ke user bernama ilham dengan ip yang ada di dalam file config dengan Hostname appserver.
   ![10](../assets/ssh/6.png)

   ![11](../assets/ssh/2.png)

   ![12](../assets/ssh/3.png)

   ![13](../assets/ssh/4.png)

   ![14](../assets/ssh/5.png)

### - For CI/CD, **use the only 1 same key**