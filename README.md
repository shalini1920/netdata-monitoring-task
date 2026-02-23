# TASK 7: Monitor System Resources Using Netdata

## 📌 Overview

This task demonstrates lightweight real-time system monitoring using **Netdata**, an open-source performance monitoring tool. Netdata provides detailed insights into CPU, memory, disk, network activity, and application metrics through an interactive dashboard.

---

## 🎯 Objective

To install Netdata via Docker and visualize live system performance metrics.

---

## 🛠 Tools Used

* Netdata (Monitoring Tool)
* Docker

---

## ✅ Prerequisites

Before starting, ensure:

✔ Docker is installed
✔ Docker service is running

---

## 🚀 Installation & Execution

Netdata was deployed using Docker with the following command:

```bash
docker run -d --name=netdata -p 19999:19999 netdata/netdata
```

This command:

✔ Pulls the Netdata image
✔ Runs Netdata in detached mode
✔ Exposes dashboard on port **19999**

---

## 🌐 Accessing the Dashboard

After successful container execution, the Netdata dashboard can be accessed via:

```
http://localhost:19999
```

The dashboard provides real-time visualization of system metrics.

---

## 📊 Metrics Observed

Netdata allows monitoring of:

✔ CPU Utilization
✔ Memory Usage
✔ Disk Activity
✔ Network Traffic
✔ System Performance Indicators

The dashboard dynamically updates performance charts.

---

## 🧾 Log Inspection

Netdata logs were explored inside the container:

```bash
docker exec -it netdata /bin/bash
cd /var/log/netdata
ls
```

Available logs:

✔ access.log
✔ error.log
✔ daemon.log
✔ collector.log
✔ health.log

Logs are useful for:

✔ Debugging
✔ Error tracking
✔ Monitoring agent activity

---

## 📸 Screenshots

The following screenshots were captured:

✔ **Dashboard Overview** – Showing CPU & Memory metrics
✔ **System Charts View** – Displaying detailed performance graphs

---

## 🧠 Key Learnings

Through this task, the following concepts were understood:

✔ Lightweight monitoring solutions
✔ Real-time performance visualization
✔ Containerized monitoring tools
✔ Importance of system metrics
✔ Log analysis for troubleshooting

---

## 💻 Commands Used

```bash
docker run -d --name=netdata -p 19999:19999 netdata/netdata
docker ps
docker exec -it netdata /bin/bash
cd /var/log/netdata
tail daemon.log
```

---

## ✅ Conclusion

Netdata provides an efficient and lightweight monitoring solution suitable for:

✔ Servers
✔ Cloud Environments
✔ Docker Containers
✔ DevOps Infrastructure

This task helped in understanding real-time system monitoring and performance analysis.

---
