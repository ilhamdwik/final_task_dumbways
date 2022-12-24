# Deployment

## Before you start the task, please read this:
### - Please screenshot the command step-by-step
### - Describe the process in your final task repository

## Requirements
### - Docker
### - Docker Hub Credentials
### - PostgreSQL (*Database*)


## Instructions


### - Build for 2 branches

#### - *Staging*

* #### - Pindah ke branch Staging. - Frontend
```
git checkout Staging
```
![01](../assets/deployment/1.png)

* #### - Buat Dockerfile. Di branch Staging saya men-deploy tanpa docker multi stage builds, untuk mengetahui perbedaan antara tanpa menggunakan multi stage dan dengan menggunakan multi stage.
![02](../assets/deployment/5.png)

* #### - Buat docker-sompose.yml.
![03](../assets/deployment/6.png)

* #### - Lalu build aplikasi wayshub-frontend.
```
docker build -t [nama_images] .
```
![04](../assets/deployment/2.png)

![05](../assets/deployment/3.png)

* #### - "docker images" untuk mengecek apakah images sudah terbuat. "docker compose up -d" untuk menjalankan apa yang sudah kita konfigurasi di dalam file docker-compose.yml. "docker ps -a" untuk mengecekapakah container sudah berjalan diport yang sudah kita tentukan di dalam file docker-compose.yml.
```
docker nama_images

docker compose up -d

docker ps -a
```
![06](../assets/deployment/4.png)


* #### - Pindah ke branch Staging. - Backend

* #### - Untuk step-stepnya kurang lebih sama seperti deploy frontend.
![07](../assets/deployment/7.png)

![08](../assets/deployment/8.png)

![09](../assets/deployment/9.png)

![10](../assets/deployment/10.png)

![14](../assets/deployment/14.png)

![15](../assets/deployment/15.png)


* #### - Aplikasi wayshub - Staging

![11](../assets/deployment/11.png)

![12](../assets/deployment/12.png)

![13](../assets/deployment/13.png)

![47](../assets/deployment/47.png)

![48](../assets/deployment/48.png)

![49](../assets/deployment/49.png)

![50](../assets/deployment/50.png)

![51](../assets/deployment/51.png)

![52](../assets/deployment/52.png)

![53](../assets/deployment/53.png)

![54](../assets/deployment/54.png)

![55](../assets/deployment/55.png)


#### - *Production*

* #### - Pindah ke branch Production. - Database
![17](../assets/deployment/17.png)

* #### - docker-compose.yml database branch Production menggunakan PostgreSQL.
![18](../assets/deployment/18.png)


* #### - Pindah ke branch Production. - Backend
![23](../assets/deployment/23.png)

![24](../assets/deployment/24.png)

![19](../assets/deployment/19.png)

![20](../assets/deployment/20.png)

![21](../assets/deployment/21.png)

![22](../assets/deployment/22.png)

![25](../assets/deployment/25.png)


* #### - Pindah ke branch Production. - Frontend
![26](../assets/deployment/26.png)

![27](../assets/deployment/27.png)

![28](../assets/deployment/28.png)

![29](../assets/deployment/29.png)

![30](../assets/deployment/30.png)

![31](../assets/deployment/31.png)

![32](../assets/deployment/32.png)

* #### - Aplikasi wayshub - Production

![34](../assets/deployment/34.png)

![35](../assets/deployment/35.png)

![37](../assets/deployment/37.png)

![38](../assets/deployment/38.png)

![39](../assets/deployment/39.png)

![40](../assets/deployment/40.png)

![41](../assets/deployment/41.png)

![42](../assets/deployment/42.png)

![43](../assets/deployment/43.png)

![44](../assets/deployment/44.png)

![45](../assets/deployment/45.png)

![46](../assets/deployment/46.png)

### - Dockerize image as small as possible

* #### Disini saya bisa mendapat size terkecil 130MB di Frontend dan 122MB di Backend.
![56](../assets/deployment/56.png)

![58](../assets/deployment/58.png)

![59](../assets/deployment/59.png)

### - Front-end + Back-end + Database Integration

* #### Disaat aplikasi bisa login dan register, maka secara otomatis integrasi frontend, backend, dan database sudah berjalan baik.
![60](../assets/deployment/39.png)

![61](../assets/deployment/40.png)

![62](../assets/deployment/41.png)

![63](../assets/deployment/42.png)

![64](../assets/deployment/43.png)

![65](../assets/deployment/44.png)

![66](../assets/deployment/45.png)

![67](../assets/deployment/46.png)


### - Use different enviroment for *Production*
### - For *Production*, do not use *npm run*

* #### Disini saya menggunakan serve, -s, build, -l untuk environtment untuk production.
![68](../assets/deployment/29.png)


### - Use **distroless** for *Production* (*Crucial Challenge*)