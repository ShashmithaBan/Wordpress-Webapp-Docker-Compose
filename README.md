# 🐳 Docker WordPress + MySQL Setup (Cross-Platform)

This project sets up a WordPress environment using Docker Compose, compatible with:

- ✅ Mac (Intel & Apple Silicon - M1/M2/M3)
- ✅ Windows
- ✅ Linux

---

## 📦 Services Included

- **WordPress**: The latest WordPress image
- **MySQL 5.7**: Database backend for WordPress
- **Volumes**: Persistent storage for MySQL

---

## 🚀 Getting Started

### 1. Prerequisites

Make sure you have the following installed:

- [Docker Desktop](https://www.docker.com/products/docker-desktop)
- [Docker Compose](https://docs.docker.com/compose/)

---

### 2. Clone the Project

```bash
git clone https://github.com/your-username/docker-wordpress-project.git
cd docker-wordpress-project
```
---

### 3. Start the Services

```
docker-compose up -d --build
```
🛠️ On M1/M2 Macs: This setup uses platform: linux/amd64 to avoid architecture issues.
---

### 4. Access WordPress

Go to http://localhost:8000 in your browser and follow the WordPress setup steps.

<img width="1680" alt="Screenshot 2025-05-21 at 11 52 23" src="https://github.com/user-attachments/assets/34685fbb-b3a4-499e-8447-2fbd920275b8" />
---


# 🧪 Environment Variables

These are defined inline in docker-compose.yml. We can move them to a .env file if needed:
```
MYSQL_DATABASE=wordpress
MYSQL_USER=wp_user
MYSQL_PASSWORD=wp_pass
MYSQL_ROOT_PASSWORD=root_pass

WORDPRESS_DB_HOST=db:3306
WORDPRESS_DB_USER=wp_user
WORDPRESS_DB_PASSWORD=wp_pass
WORDPRESS_DB_NAME=wordpress
```
---

# 🧹 Stopping and Cleaning Up

To stop the containers:
```
docker-compose down
```

To remove volumes:
```
docker-compose down -v

```
