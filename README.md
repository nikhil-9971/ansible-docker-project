# 🚀 Ansible Docker Nginx Setup

This project demonstrates a complete DevOps workflow to automate
infrastructure configuration using Ansible, deploy a Dockerized
application, and expose it via an Nginx reverse proxy.

------------------------------------------------------------------------

## 📌 Features

-   🔧 Automated server configuration using Ansible
-   🐳 Docker installation and container deployment
-   🌐 Nginx reverse proxy setup
-   🔁 Idempotent infrastructure (safe re-runs)
-   🔐 Secure handling of sensitive data (best practices)

------------------------------------------------------------------------

## 🏗️ Project Structure

ansible-docker-project/ ├── roles/ │ ├── docker/ │ └── nginx/ ├──
group_vars/ ├── inventory.ini ├── site.yml ├── ansible.cfg └── README.md

------------------------------------------------------------------------

## ⚙️ Technologies Used

-   Ansible
-   Docker
-   Nginx
-   AWS EC2 (Linux)

------------------------------------------------------------------------

## 🚀 How It Works

1.  Ansible connects to the EC2 instance
2.  Installs Docker and runs the container
3.  Installs and configures Nginx
4.  Sets up reverse proxy:
    -   Port 80 → Nginx
    -   Port 8080 → Docker container
5.  Nginx forwards requests to the container

------------------------------------------------------------------------

## 🧪 Verification

``` bash
# Check container directly
curl http://localhost:8080

# Check via Nginx
curl http://localhost
```

------------------------------------------------------------------------

## 🔐 Security Note

Sensitive files like: - `.vault_pass` - `vault.yml` - `.pem` keys

are excluded using `.gitignore`.

------------------------------------------------------------------------

## 📈 Future Improvements

-   HTTPS (Let's Encrypt SSL)
-   Load balancing (multiple containers)
-   CI/CD pipeline integration
-   Auto-scaling infrastructure

------------------------------------------------------------------------

## 🙌 Author

Nikhil Trivedi\
Aspiring DevOps Engineer 🚀

