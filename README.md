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

## Screenshots

<img width="1919" height="968" alt="Screenshot 2025-08-14 205912" src="https://github.com/user-attachments/assets/1d038d45-f76c-451b-9452-a5b0a06bfa27" />
<img width="1919" height="1023" alt="Screenshot 2025-08-14 205618" src="https://github.com/user-attachments/assets/b617c443-6286-4a30-8034-a55a30f997a2" />
<img width="1919" height="966" alt="Screenshot 2025-08-14 205309" src="https://github.com/user-attachments/assets/b9865f97-dd68-4118-a8b2-501b41e2a39e" />
<img width="1919" height="972" alt="Screenshot 2025-08-14 205217" src="https://github.com/user-attachments/assets/daa9e841-31d3-454a-9607-450817779356" />
<img width="1919" height="973" alt="Screenshot 2025-08-14 205151" src="https://github.com/user-attachments/assets/1cae35eb-4cc4-46e7-8db9-432dcd403ae5" />
<img width="1919" height="968" alt="Screenshot 2025-08-14 205017" src="https://github.com/user-attachments/assets/55923068-ba78-40fd-b5e1-a63b6e6c0b5e" />
<img width="1919" height="970" alt="Screenshot 2025-08-14 204948" src="https://github.com/user-attachments/assets/c611892c-7333-4dc4-9a93-32327b1b14ec" />
<img width="1919" height="973" alt="Screenshot 2025-08-14 204852" src="https://github.com/user-attachments/assets/dfc8d89c-dd37-4e6b-8494-1b1bf98e0a1c" />
<img width="1917" height="969" alt="Screenshot 2025-08-14 204654" src="https://github.com/user-attachments/assets/0c4061f9-2598-4fba-8bfa-89c935547b58" />
<img width="1919" height="964" alt="Screenshot 2025-08-14 204636" src="https://github.com/user-attachments/assets/365aaffd-1324-40dd-8803-dd50d86a2835" />
<img width="1918" height="963" alt="Screenshot 2025-08-14 204621" src="https://github.com/user-attachments/assets/becf0d78-9d94-4946-abf5-c33890dede2a" />
<img width="1919" height="964" alt="Screenshot 2025-08-14 204556" src="https://github.com/user-attachments/assets/9cb85849-9e5c-4960-8355-8b4251a08eac" />
<img width="1916" height="973" alt="Screenshot 2025-08-14 203743" src="https://github.com/user-attachments/assets/a56d7048-88cb-4f8c-ba33-3c02186a9974" />


  
---

## Observations

- Successfully monitored CPU, memory, and disk usage.  
- Tracked Docker containers in real time.  
- Observed various system metrics with interactive charts.  
- Verified alert system in the dashboard.  


