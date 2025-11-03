# 🧱 MERN NoteBoard

A **Full-Stack Notes Application** built with the **MERN stack (MongoDB, Express, React, Node)**.  
Create, update, and delete notes with a clean React UI and a secure Express API — production-deployable and beginner-friendly.

---

## ✨ About the App

- 🧩 **Full-Stack Architecture** — MERN end-to-end (frontend + backend + DB)
- 🛠️ **REST API** — CRUD for notes (title & description), status codes, error handling
- ⚙️ **Rate Limiting (Upstash Redis)** — real-world protection for APIs
- 💡 **`.env` Setup** — secure config for local & production
- 📱 **Responsive UI** — works on mobile and desktop

---

## 🧰 Tech Stack

| Layer      | Tech                          |
| ---------- | ----------------------------- |
| Frontend   | React (Vite), HTML, CSS       |
| Backend    | Node.js, Express.js           |
| Database   | MongoDB (Atlas)               |
| Caching/RL | Upstash Redis (REST)          |
| Deployment | Render (API), Vercel (Web)    |

---
## 📝 .env Setup

### 🔗 Backend (`/backend`)
```env
MONGO_URI=<your_mongo_uri>

UPSTASH_REDIS_REST_URL=<your_redis_rest_url>
UPSTASH_REDIS_REST_TOKEN=<your_redis_rest_token>

NODE_ENV=development
PORT=5001
## 🛠️ Run the Backend (Local)
```bash
cd backend
npm install
# .env must contain: MONGO_URI, UPSTASH_REDIS_REST_URL, UPSTASH_REDIS_REST_TOKEN, PORT=5001
npm run dev

## Run the Frontend
cd frontend
npm install
# optional: if your client reads API URL from env
echo "VITE_API_URL=http://localhost:5001" > .env
npm run dev
