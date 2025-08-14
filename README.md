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

## Screenshots:

![Database](Screenshots/Screenshot%202025-08-14%20203743.png)  
![Main Dashboard](Screenshots/Screenshot%202025-08-14%20204556.png)  
![System](Screenshots/Screenshot%202025-08-14%20204621.png)  
![Modules](Screenshots/Screenshot%202025-08-14%20204636.png)  
![Directories](Screenshots/Screenshot%202025-08-14%20204654.png)  
![Metrics](Screenshots/Screenshot%202025-08-14%20204852.png)  
![CPU Metrics](Screenshots/Screenshot%202025-08-14%20204948.png)  
![Disk Metrics](Screenshots/Screenshot%202025-08-14%20205017.png)  
![Alerts](Screenshots/Screenshot%202025-08-14%20205151.png)  
![Alert](Screenshots/Screenshot%202025-08-14%20205217.png)  
![Alert Graph](Screenshots/Screenshot%202025-08-14%20205309.png)  
![Docker Containers](Screenshots/Screenshot%202025-08-14%20205618.png)  
![Dashboard](Screenshots/Screenshot%202025-08-14%20205912.png)  


## Observations

- Successfully monitored CPU, memory, and disk usage.  
- Tracked Docker containers in real time.  
- Observed various system metrics with interactive charts.  
- Verified alert system in the dashboard.  
