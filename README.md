# Netdata Monitoring Setup

## Description
The objective of this task was to set up **Netdata** for real-time monitoring of system resources such as CPU, memory, disk, and Docker containers.  
Netdata provides an interactive web dashboard for metrics visualization and health alerts.  

**Tools Used:**
- Docker
- Netdata
- PowerShell

---

## Commands Used

### Run Netdata Container
```powershell
docker run -d --name=netdata `
-p 19999:19999 `
--cap-add SYS_PTRACE `
--security-opt apparmor=unconfined `
-v netdataconfig:/etc/netdata `
-v netdatalib:/var/lib/netdata `
-v netdatacache:/var/cache/netdata `
-v /etc/passwd:/host/etc/passwd:ro `
-v /etc/group:/host/etc/group:ro `
-v /proc:/host/proc:ro `
-v /sys:/host/proc:ro `
-v /etc/os-release:/host/etc/os-release:ro `
netdata/netdata

---

## Screenshots:

<img width="1919" height="968" alt="Screenshot 2025-08-14 205017" src="https://github.com/user-attachments/assets/e5c3d8e0-38fb-4956-9202-c7e0c8a33b96" />
<img width="1919" height="970" alt="Screenshot 2025-08-14 204948" src="https://github.com/user-attachments/assets/40356046-5e5a-446c-b9f2-e5eab7acedd6" />
<img width="1919" height="973" alt="Screenshot 2025-08-14 204852" src="https://github.com/user-attachments/assets/e663b522-3d0b-4890-b7c3-453e8cf79bc2" />
<img width="1917" height="969" alt="Screenshot 2025-08-14 204654" src="https://github.com/user-attachments/assets/15097b3b-0c29-4452-a588-1c7abf5d2535" />
<img width="1919" height="964" alt="Screenshot 2025-08-14 204636" src="https://github.com/user-attachments/assets/5f0a35d9-99e1-408e-ab9b-343aa472e3e1" />
<img width="1918" height="963" alt="Screenshot 2025-08-14 204621" src="https://github.com/user-attachments/assets/feea4838-cb86-423b-ae24-099308fbb711" />
<img width="1919" height="964" alt="Screenshot 2025-08-14 204556" src="https://github.com/user-attachments/assets/55a801db-2749-4092-adf8-5bf715fb313b" />
<img width="1916" height="973" alt="Screenshot 2025-08-14 203743" src="https://github.com/user-attachments/assets/19974cb4-4670-475d-adec-ad2c2cfedf49" />
<img width="1919" height="968" alt="Screenshot 2025-08-14 205912" src="https://github.com/user-attachments/assets/8b0398a7-f86e-408d-81fc-455c1798ec02" />
<img width="1919" height="1023" alt="Screenshot 2025-08-14 205618" src="https://github.com/user-attachments/assets/d50dd66e-1486-4a2f-bba6-9f2341ab051c" />
<img width="1919" height="966" alt="Screenshot 2025-08-14 205309" src="https://github.com/user-attachments/assets/e1d16b6f-86e2-465a-ac2c-0f56bc351b28" />
<img width="1919" height="972" alt="Screenshot 2025-08-14 205217" src="https://github.com/user-attachments/assets/224c68b2-2a8d-4121-b07b-10a101798a93" />
<img width="1919" height="973" alt="Screenshot 2025-08-14 205151" src="https://github.com/user-attachments/assets/677f470b-dfa8-455f-9b10-895964edb56b" />

  
---

## Observations

- Successfully monitored CPU, memory, and disk usage.  
- Tracked Docker containers in real time.  
- Observed various system metrics with interactive charts.  
- Verified alert system in the dashboard.  

