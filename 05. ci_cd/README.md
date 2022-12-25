![00](../assets/SOAL_FINAL_TASK/5.png)

# CI/CD

## Before you start the task, please read this:
### - Please screenshot the command step-by-step
### - Describe the process in your final task repository

## Requirements
### - install at monitoring server
### - Jenkins / Gitlab CI
### - Pipeline script
  #### - Pull Repository
  #### - Build, test & run the application
  #### - Push to registry

## Instructions
### - Auto-trigger build for every push
### - Push notification for every build
### - Run the pipeline on a multi-branch configuration
### - Push the image into a private registry (*Challenge*)


![01](../assets/jenkins/1.png)

![02](../assets/jenkins/2.png)

![03](../assets/jenkins/3.png)

![04](../assets/jenkins/4.png)

* #### Setelah menginstall Jenkins di server. Kita jalankan dahulu docker logs nama_container.
```
docker logs jenkins
```
![05](../assets/jenkins/5.png)

* #### Secara otomatis jenkins akan men-generate password untuk login sebagai admin.
![06](../assets/jenkins/6.png)

* #### Copy paste pada step 6.
![07](../assets/jenkins/7.png)

![08](../assets/jenkins/8.png)

* #### Pilih select plugin to install.
![09](../assets/jenkins/9.png)

![10](../assets/jenkins/10.png)

![11](../assets/jenkins/11.png)

* #### Disini kita bisa memasukkan username dan password baru.
![12](../assets/jenkins/12.png)

![13](../assets/jenkins/13.png)

![14](../assets/jenkins/14.png)

![15](../assets/jenkins/15.png)

![16](../assets/jenkins/16.png)

* #### Masuk ke dashboard, manage jenkins, credentials, system, global credentials.
![17](../assets/jenkins/17.png)

* #### Masukkan private key ke dalam jenkins.
![18](../assets/jenkins/18.png)

![19](../assets/jenkins/19.png)

* #### Agar akun jenkins dan github terhubung, maka masukkan juga public key ke dalam github.
![20](../assets/jenkins/20.png)

* #### Buat job baru.
![23](../assets/jenkins/23.png)

* #### Pilih multibranch pipeline, dikarenakan kita ingin membuat ci_cd dengan banyak branch.
![24](../assets/jenkins/24.png)

![25](../assets/jenkins/25.png)

* #### Pilih git.
![26](../assets/jenkins/26.png)

* #### Dikarenakan repository yang saya pakai bersifat private maka bisa menggunakan SSH. Copy link SSH di github, lalu paste kedalam git repository di dalam jenkins.
![27](../assets/jenkins/27.png)

* #### Pilih credentials ilhaskam.
![28](../assets/jenkins/28.png)

* #### Untuk mengaktifkan Multibranch Scan Webhook Trigger, install terlebih dahulu plugin bernama Multibranch Scan Webhook Trigger.
![31](../assets/jenkins/31.png)

* #### Untuk mengaktifkan trigger pada saat ada update di repository akun github kita. Maka pada github kita tambahkan di bagian Webhooks. Untuk payload URL yang dimasukkan di github repository bisa melihat pada step sebelumnya.
![32](../assets/jenkins/32.png)

![33](../assets/jenkins/33.png)

![34](../assets/jenkins/34.png)

* #### Pada saat muncul centang dan berwarna hijau, maka trigger sudah berjalan dengan baik.
![35](../assets/jenkins/35.png)

![36](../assets/jenkins/36.png)

* #### Menambahkan notifikasi discord.
* #### Pilih pipeline sintax.
![37](../assets/jenkins/37.png)

* #### Masuk ke dalam channel discord lalu pilih edit channel.
![38](../assets/jenkins/38.png)

* #### Pilih Integrations.
![39](../assets/jenkins/39.png)

* #### Pilih webhooks, lalu create webhook.
![40](../assets/jenkins/40.png)

![41](../assets/jenkins/41.png)

* #### Copy webhook URL.
![42](../assets/jenkins/42.png)

* #### pada kolom Sample Step pilih discordSend. Lalu paste webhook URL tadi.
![43](../assets/jenkins/43.png)

![44](../assets/jenkins/44.png)

* #### Generate pipeline script.
![45](../assets/jenkins/45.png)

* #### Copy paste script ke dalam pipeline yang sudah kita buat.
![46](../assets/jenkins/46.png)

![47](../assets/jenkins/47.png)

![48](../assets/jenkins/48.png)

* #### Maka jika ada update script dari repository github makapembaruan di jenkins juga akan langsung dijalankan secara otomatis..
![49](../assets/jenkins/49.png)

![50](../assets/jenkins/50.png)

![51](../assets/jenkins/51.png)

![52](../assets/jenkins/52.png)

![53](../assets/jenkins/53.png)

![54](../assets/jenkins/54.png)

![55](../assets/jenkins/55.png)

![56](../assets/jenkins/56.png)

![57](../assets/jenkins/57.png)

![58](../assets/jenkins/58.png)

![59](../assets/jenkins/59.png)

![60](../assets/jenkins/60.png)

![61](../assets/jenkins/61.png)

![62](../assets/jenkins/62.png)

* #### Discord notifikasi sudah berhasil muncul.
![63](../assets/jenkins/63.png)

![64](../assets/jenkins/64.png)

* #### Disini sat push private registry saya menggunakan registry dari cloud.canister.io
![65](../assets/jenkins/65.png)

![66](../assets/jenkins/66.png)

![67](../assets/jenkins/67.png)

![68](../assets/jenkins/68.png)

* #### Login ke dalam registry cloud.canister.io
![69](../assets/jenkins/69.png)

* #### Command ini membuat tag dari images ilhaskam/wayshub-frontend-production-jenkins dan mengubahnya menjadi cloud.canister.io:5000/ilhaskam/wayshub-frontend.
![70](../assets/jenkins/70.png)

* #### Maka akan terbuat images baru bernama cloud.canister.io:5000/ilhaskam/wayshub-frontend.
![71](../assets/jenkins/71.png)

![74](../assets/jenkins/74.png)

![75](../assets/jenkins/75.png)

![76](../assets/jenkins/76.png)