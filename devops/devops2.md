# 10 Real DevOps Scenario Interview Questions

These are **very common real interview questions**.

### Scenario 1

**Website is not loading. What will you check?**

Expected steps:

1. Check server status
    
2. Check application service
    
3. Check port
    
4. Check firewall
    
5. Check logs
    

---

### Scenario 2

**Server disk is full. What will you do?**

Commands:

df -h  
du -sh *

Then delete:

- old logs
    
- temporary files
    

---

### Scenario 3

**CPU usage is very high. How do you find the issue?**

Commands:

top  
ps aux

Then check which process is consuming CPU.

---

### Scenario 4

**Docker container stopped suddenly. What will you check?**

Commands:

docker ps -a  
docker logs <container_id>

---

### Scenario 5

**Server is reachable but website is not opening.**

Possible checks:

- Application service running?
    
- Port open?
    
- Firewall rules?
    
- Nginx / Apache status?
    

---

### Scenario 6

**You cannot SSH into the server. What could be the issue?**

Possible reasons:

- SSH service down
    
- Firewall blocking port 22
    
- Security group issue (cloud)
    
- Network problem
    

---

### Scenario 7

**Application deployment failed in CI/CD pipeline. What will you do?**

Steps:

1. Check pipeline logs
    
2. Check build errors
    
3. Verify environment variables
    
4. Check server permissions
    

---

### Scenario 8

**Docker image build failed. What will you check?**

- Dockerfile syntax
    
- dependency installation
    
- base image availability
    

---

### Scenario 9

**Server memory usage is very high.**

Commands:

free -m  
top

Then identify process using memory.

---

### Scenario 10

**User cannot access a website hosted on AWS EC2.**

Check:

- EC2 running?
    
- Security group rules
    
- Port open (80 / 443)
    
- Web server running
    

---

# Complete 2-Hour Mock Interview Structure

You can run the class like a **real interview session**.

## 2:30 – 2:45 (15 mins)

## Basic Questions Round

Ask students:

- What is DevOps?
    
- What is CI/CD?
    
- What is Docker?
    
- What is Kubernetes?
    

Let **students answer verbally**.

---

## 2:45 – 3:10 (25 mins)

## Linux + Networking Round

Ask:

Linux:

- How do you check disk usage?
    
- How do you check running processes?
    
- How do you see logs?
    

Networking:

- What is DNS?
    
- What is TCP vs UDP?
    
- What is a port?
    

---

## 3:10 – 3:30 (20 mins)

## Docker + Cloud Round

Ask:

Docker:

- What is Docker?
    
- What is a container?
    
- What is a Dockerfile?
    

Cloud:

- What is EC2?
    
- What is S3?
    
- What is IAM?
    

---

## 3:30 – 4:10 (40 mins)

## Scenario Round (Most Important)

Ask:

- Website not loading → what will you check?
    
- Disk full → what command?
    
- High CPU → how to find process?
    
- Docker container stopped → what will you check?
    

Make **students explain step-by-step thinking**.

---

## 4:10 – 4:25 (15 mins)

## Communication Practice

Call 3–4 students and ask them to explain:

1. Explain **Docker in 1 minute**
    
2. Explain **DevOps**
    
3. Explain **CI/CD pipeline**
    

Interviewers **test communication a lot**.

---

## 4:25 – 4:30 (5 mins)

## Final Interview Tips

Tell them:

✔ Speak clearly  
✔ If you don't know answer → explain what you know  
✔ Give **practical examples**  
✔ Don't panic

Example:

Instead of saying  
❌ "I know Docker"

Say  
✅ "I created Docker images using Dockerfile and ran containers using docker run."

---

# 3 Very Important Interview Question

## What happens when you type **google.com** in a browser?

This is **one of the most famous interview questions**.

Explain it like this:

### Step 1 — DNS Lookup

Browser asks DNS server:

"Where is google.com?"

DNS returns the **IP address**.

Example:

google.com → 142.250.x.x

---

### Step 2 — TCP Connection

Browser establishes a **TCP connection** with the server.

Uses port:

HTTPS → 443

---

### Step 3 — HTTPS Request

Browser sends:

GET / HTTP/1.1

Request goes to **Google server**.

---

### Step 4 — Server Processing

Google server processes request and sends back:

- HTML
    
- CSS
    
- JavaScript
    

---

### Step 5 — Browser Rendering

Browser renders the webpage.

You see **Google homepage**.

---

# Simple 1-Line Interview Answer

Students can say:

> "When we type google.com, DNS converts the domain to an IP address, then the browser establishes a TCP connection with the server, sends an HTTP request, the server responds with webpage data, and the browser renders the page."

Perfect answer for interviews.

---