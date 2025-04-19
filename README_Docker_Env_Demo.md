# 🐳 Docker Environment Variable Demo

This project demonstrates two common ways to manage environment variables inside Docker containers using Docker Compose:

✅ Using a `.env` file  
✅ Using the `environment:` block in `docker-compose.yml`

---

## 📁 Project Structure

```
docker-env-demo/
├── .env                 # Contains environment variables
├── docker-compose.yml   # Defines and runs the container
└── app/
    └── app.sh           # Simple script that prints env values
```

---

## 🚀 How to Run

### Option 1: Using `.env` file

1. Check or update the `.env` file:
    ```env
    USER_NAME=Sathya
    USER_ROLE=DevOps Engineer
    ```

2. Run the container:
    ```bash
    docker-compose up
    ```

3. Output:
    ```
    Welcome, Sathya!
    Your role is: DevOps Engineer
    ```

---

### Option 2: Using `environment:` block in Compose

Update your `docker-compose.yml`:
```yaml
environment:
  - USER_NAME=Sathya
  - USER_ROLE=Docker Explorer
```

Then re-run:
```bash
docker-compose up --force-recreate
```

---

## 💡 What You Learn

- How to securely inject config into Docker containers
- Difference between `.env` files and inline `environment:` blocks
- Best practices for separating code and configuration

---

## 🧠 Ideal For

- Beginners learning Docker Compose  
- DevOps learners preparing for real-world deployments  
- Practicing `.env` management before using Kubernetes ConfigMaps & Secrets

---

🔒 Secrets. Clean Code. DevOps Ready.

Made with ❤️ by [Sathya](https://github.com/PillaiSathya)
