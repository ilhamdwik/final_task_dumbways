# Monitoring

## Before you start the task, please read this:
### - Please screenshot the command step-by-step
### - Describe the process in your final task repository

## Requirements
### - Prometheus
### - Grafana Dashboard
### - Alertmanager / Grafana Alert

## Instructions
### - Monitor the *Appserver* and *Gateway*
### - Create 2 Dashboards
  #### - Use template for the first dashboard
  #### - Second dashboard for alerting
### - Use alerting to notify
  #### - CPU usage over 75%
  #### - RAM usage over 1.25 GiB


![01](../assets/monitoring/1.png)

![02](../assets/monitoring/2.png)

* #### Masukkan volumes untuk config prometheus.
![03](../assets/monitoring/3.png)

* #### Buat directory config, lalu di dalam direktory config buat file prometheus.yml. File ini bermaksud bahwa prometheus membaca data metrics dari node exporter di dalam ip yang dimaksudkan. Seperti memberi tahu bahwa target yang ingin di monitoring.
![04](../assets/monitoring/4.png)

![05](../assets/monitoring/5.png)

![06](../assets/monitoring/6.png)

* #### Node Exporter.
![07](../assets/monitoring/7.png)

* #### Status target yang telah dimasukkan di file prometheus.yml, jika state "DOWN" maka server dari target belum tersambung atau server dari target masih mati atau kita salah dalam meng-configurasi target yang kita masukkan di dalam file prometheus.yml. 
![08](../assets/monitoring/8.png)

![09](../assets/monitoring/9.png)

![10](../assets/monitoring/10.png)

![11](../assets/monitoring/11.png)

* #### Jika state "UP" maka target sudah terhubung dan kita sudah bisa memonitoring target.
![12](../assets/monitoring/12.png)

* #### Membuat alerting. klik new alert rule.
![13](../assets/monitoring/13.png)

![14](../assets/monitoring/14.png)

![15](../assets/monitoring/15.png)

![16](../assets/monitoring/16.png)

![17](../assets/monitoring/17.png)

![18](../assets/monitoring/18.png)

* #### Membuat template di grafana.
![19](../assets/monitoring/19.png)

![20](../assets/monitoring/20.png)

![21](../assets/monitoring/21.png)

![22](../assets/monitoring/22.png)

![23](../assets/monitoring/23.png)