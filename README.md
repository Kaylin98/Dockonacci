# 🐳 Dockonacci 📈

Welcome to **Dockonacci** — the world's most *over-engineered* Fibonacci calculator... on purpose! 😎

This app takes a ridiculously simple math function and wraps it in a full microservice architecture to help you **master Docker** and understand how real-world containerized systems are built.

Why? Because nothing says "learning" like using **Nginx, React, Node.js, Redis, Postgres, and a background worker** to calculate the 6th Fibonacci number.

---

## 🚧 What's the Point?

> 🧠 **This is intentionally over the top.**

Dockonacci exists to help you practice:

- Spinning up multi-container Docker apps
- Using reverse proxies
- Managing async jobs with queues
- Working with persistent databases
- Wiring everything together in dev with `docker-compose`

---

## 🧱 Architecture

```
Browser
   ↓
Nginx (reverse proxy)
   ↓
React Client + Express API
        ↓
     Postgres + Redis
             ↓
          Worker
```

### 🧩 Services Breakdown

| Service         | Role                                                    |
|----------------|----------------------------------------------------------|
| **Nginx**       | Routes traffic to React & Express                        |
| **React Client**| User interface to submit Fibonacci indices               |
| **Express API** | Accepts input, stores it, sends it to Redis              |
| **Redis**       | Acts as a queue and cache for calculated values         |
| **Worker**      | Listens to Redis, crunches Fibonacci, stores result      |
| **Postgres**    | Saves all submitted indices for long-term storage        |

---

## 🚀 Running Locally

### 1. Clone this genius:

```bash
git clone https://github.com/Kaylin98/Dockonacci.git
cd Dockonacci
```

### 2. Add `.env` files (optional for DB creds, etc.)

### 3. Launch all the things

```bash
docker-compose up --build
```

### 4. Open your browser

```txt
http://localhost
```

Input an index. Watch the magic (and maybe cry at the absurdity of it all).

---

## 💾 Tech Stack

- **Frontend:** React
- **Backend:** Node.js + Express
- **Worker:** Node.js, Redis pub/sub
- **Database:** Postgres
- **Queue:** Redis
- **Proxy:** Nginx
- **Orchestration:** Docker Compose

---

## 🛠️ TODOs (Level Up)

- [ ] Split dev/prod Docker configs
- [ ] CI/CD with GitHub Actions
- [ ] Push containers to Docker Hub
- [ ] Deploy to the cloud like a boss

---

## 🧪 Why Fibonacci?

Because it's simple enough to understand but complicated enough to pretend we need Redis and a worker.

---

## 🪪 License

MIT — Go forth and containerize your future.

---

Built with love, Docker, and way too many containers.  
✨ *Learning by overengineering FTW.*
