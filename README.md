# 🚀 Greenbone Auto-Deploy Script

This project provides a **fully automated shell script** to install and launch the **Greenbone Community Edition (GCE)** using Docker on Ubuntu systems.

> 🔒 The script configures a ready-to-use local vulnerability scanning environment with a predefined admin password — ideal for learning, testing, or personal use.

---

## 💡 What the Script Does

The `greenbone-setup.sh` script performs the following actions step-by-step:

1. **Installs Required Packages**  
   Installs `curl`, `gnupg`, and `ca-certificates`, which are essential for downloading and verifying Docker components.

2. **Removes Conflicting Docker Packages**  
   Cleans up older Docker-related packages that may cause conflicts.

3. **Adds Docker’s Official Repository**  
   Adds Docker’s GPG key and APT repository for stable releases.

4. **Installs Docker and Docker Compose Plugin**  
   Installs all necessary Docker components for container management.

5. **Adds Current User to Docker Group**  
   Allows the user to run Docker commands without `sudo`.

6. **Creates Download Directory**  
   Creates a dedicated folder in the user's home directory to store Greenbone files.

7. **Downloads Official `docker-compose.yml`**  
   Fetches the latest Greenbone Community Docker Compose file directly from Greenbone’s website.

8. **Pulls Required Container Images**  
   Downloads all necessary Docker images specified in the Compose file.

9. **Starts the Containers in Background**  
   Spins up the full Greenbone stack using Docker Compose.

10. **Waits for Initialization**  
    Allows time for Greenbone services to initialize properly.

11. **Sets Default Admin Password**  
    Automatically updates the default `admin` user's password to `admin123`.

12. **Opens the Web Interface**  
    Launches the Greenbone Security Assistant (GSA) web UI at:  
    **http://127.0.0.1:9392**

---

## 🔐 Login Details

- **Username:** `admin`  
- **Password:** `admin123`

> You can change the password later using the GSA interface or Greenbone CLI.

---

## ✅ Requirements

- Ubuntu 20.04 or 22.04 (recommended)
- Sudo privileges
- Internet access

---

## 📎 How to Use

Once you upload `greenbone-setup.sh` to this repo:

```bash
chmod +x greenbone-setup.sh
./greenbone-setup.sh
