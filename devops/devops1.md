
---

# 1️ Linux / Server Administration Questions

Ask students these first.

**1. What is Linux? Why is it widely used in servers?**

**2. What are some common Linux commands you use daily?**

Expected answers:

- `ls`
    
- `cd`
    
- `cp`
    
- `mv`
    
- `rm`
    

**3. How do you check disk usage in Linux?**

Expected:

```
df -h
du -sh
```

**4. How do you check running processes?**

Expected:

```
ps
top
htop
```

**5. How do you check memory usage?**

Expected:

```
free -m
```

**6. How do you check system logs?**

Expected:

```
/var/log
tail -f
journalctl
```

---

# 2️ Networking Questions (Very Common)

**7. What is DNS?**

Expected:  
DNS converts **domain names to IP addresses**.

**8. What is TCP/IP?**

Expected:  
A protocol used for **communication between devices on a network**.

**9. What is the difference between TCP and UDP?**

TCP  
✔ Reliable  
✔ Connection-oriented

UDP  
✔ Faster  
✔ Connectionless

**10. What is a firewall?**

Expected:  
A firewall **controls incoming and outgoing network traffic based on rules**.

**11. What is a port?**

Expected:  
A **communication endpoint** used by services.

Examples:

- HTTP → 80
    
- HTTPS → 443
    
- SSH → 22
    

---

# 3️ Virtualization Questions

**12. What is virtualization?**

Expected:  
Running **multiple virtual machines on a single physical server**.

**13. What is the difference between a Virtual Machine and a Container?**

VM

- Full OS
    
- Heavy
    

Container

- Shares host OS
    
- Lightweight
    

---

# 4️ Monitoring / Storage Questions

**14. Why do we use monitoring tools?**

Expected:

- Track server health
    
- Monitor CPU
    
- Monitor memory
    
- Detect failures
    

Example tools:

- Prometheus
    
- Grafana
    
- Nagios
    

**15. Why are backups important?**

Expected:

- Data recovery
    
- Disaster recovery
    
- Prevent data loss
    

---

	# 5️ Scripting Questions

**16. What is scripting?**

Expected:  
Automating tasks using scripts.

Examples:

- Bash
    
- Python
    
- PowerShell
    

**17. What tasks can be automated using scripts?**

Examples:

- Backup
    
- Deployment
    
- Log cleanup
    
- Server setup
    

---

# 6️ Cloud Questions

**18. What is cloud computing?**

Expected:  
Delivering computing services **over the internet instead of local servers**.

**19. What is AWS EC2?**

Expected:  
A **virtual server in AWS cloud**.

**20. What is object storage?**

Expected:  
Storage for files and data.

Example:  
AWS **S3**

---

# 7️ Containers / Kubernetes Questions

**21. What is Docker?**

Expected:  
A platform used to **create and run containers**.

**22. What is a Docker image?**

Expected:  
A **template used to create containers**.

**23. What is Kubernetes used for?**

Expected:  
To **manage and orchestrate containers at scale**.

---

# 8️ Automation Tools Questions

**24. What is Ansible used for?**

Expected:  
Configuration management and automation.

**25. What is Terraform used for?**

Expected:  
Infrastructure as Code (IaC).

Used to create:

- Servers
    
- Networks
    
- Cloud resources
    

---

# 9️ Troubleshooting Questions (VERY IMPORTANT)

Ask these **scenario questions**.

**26. Server CPU is very high. What will you check?**

Expected:

1. `top`
    
2. `ps`
    
3. Logs
    
4. Running services
    

---

**27. Website is not loading. What will you check?**

Expected steps:

1. Check server status
    
2. Check port
    
3. Check firewall
    
4. Check application service
    
5. Check logs
    

---

**28. Disk is full. What will you do?**

Expected:

- `df -h`
    
- `du -sh`
    
- Remove old logs
    

---

# 10️ Communication Question

Ask them:

**29. Explain DevOps in simple words.**

Expected idea:

DevOps is a **culture that combines development and operations to deliver software faster and more reliably**.

---

# Best Activity for Your Class (Highly Recommended)

Do **mock interviews**.

Call one student and ask:

- What is DNS?
    
- What is Docker?
    
- Difference between VM and container?
    
- What will you do if a website is down?
    

This helps students **gain confidence before tomorrow's interview**.

---

